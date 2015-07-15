=============================================================================
Rebuild Specified Server -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Rebuild Specified Server
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <POST_rebuild_specified_server_servers_server_id_actions.rst#request>`__
`Response <POST_rebuild_specified_server_servers_server_id_actions.rst#response>`__

.. code-block:: javascript

    POST /servers/{server_id}/actions

Rebuild the specified server.

The rebuild operation removes all data on the server and replaces it with the specified image. The serverID and all IP addresses remain the same. If you specify name, metadata, accessIPv4, or accessIPv6 in the rebuild request, new values replace existing values. Otherwise, these values do not change. You can inject data into the file system during the rebuild.

This operation is not available for OnMetal servers.

Specify the target server ID in the URI.

In the request body, specify the rebuild action followed by various attributes, listed in the following parameters section.



This table shows the possible response codes for this operation:


+--------------------------+-------------------------+-------------------------+
|Response Code             |Name                     |Description              |
+==========================+=========================+=========================+
|202                       |Success                  |Request succeeded.       |
+--------------------------+-------------------------+-------------------------+
|400                       |Error                    |A general error has      |
|                          |                         |occured.                 |
+--------------------------+-------------------------+-------------------------+
|401                       |Unauthorized             |Unauthorized.            |
+--------------------------+-------------------------+-------------------------+
|403                       |Forbidden                |Forbidden.               |
+--------------------------+-------------------------+-------------------------+
|405                       |Bad Method               |Bad method.              |
+--------------------------+-------------------------+-------------------------+
|409                       |Conflicting Reqest       |Conflicting request.     |
+--------------------------+-------------------------+-------------------------+
|413                       |Over Limit               |The number of items      |
|                          |                         |returned is above the    |
|                          |                         |allowed limit.           |
+--------------------------+-------------------------+-------------------------+
|503                       |Service Unavailable      |The requested service is |
|                          |                         |unavailable.             |
+--------------------------+-------------------------+-------------------------+
|500                       |API Fault                |API fault.               |
+--------------------------+-------------------------+-------------------------+


Request
^^^^^^^^^^^^^^^^^

This table shows the URI parameters for the request:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|{server_id}               |csapi:UUID               |The UUID for the server. |
+--------------------------+-------------------------+-------------------------+





This table shows the body parameters for the request:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|rebuild                   |object *(Required)*      |Specification of the     |
|                          |                         |rebuild action for the   |
|                          |                         |specified server.        |
+--------------------------+-------------------------+-------------------------+
|name                      |object *(Required)*      |The new name for the     |
|                          |                         |server.                  |
+--------------------------+-------------------------+-------------------------+
|imageRef                  |object *(Required)*      |The image ID.            |
+--------------------------+-------------------------+-------------------------+
|accessIPv4                |object *(Required)*      |The IP version 4 address.|
+--------------------------+-------------------------+-------------------------+
|accessIPv6                |object *(Required)*      |The IP version 6 address.|
+--------------------------+-------------------------+-------------------------+
|adminPass                 |csapi:string *(Required)*|The password assigned to |
|                          |                         |provide login access to  |
|                          |                         |the server.              |
+--------------------------+-------------------------+-------------------------+
|metadata                  |csapi:string *(Required)*|A metadata key and value |
|                          |                         |pair.                    |
+--------------------------+-------------------------+-------------------------+
|personality               |csapi:string *(Required)*|The file path and file   |
|                          |                         |contents.                |
+--------------------------+-------------------------+-------------------------+
|OS-DCF:diskConfig         |csapi:string *(Required)*|The disk configuration   |
|                          |                         |value. Valid values are: |
|                          |                         |AUTO:The server is built |
|                          |                         |with a single partition  |
|                          |                         |which is the size of the |
|                          |                         |target flavor disk. The  |
|                          |                         |file system is           |
|                          |                         |automatically adjusted   |
|                          |                         |to fit the entire        |
|                          |                         |partition. This keeps    |
|                          |                         |things simple and        |
|                          |                         |automated. AUTO is valid |
|                          |                         |only for images and      |
|                          |                         |servers with a single    |
|                          |                         |partition that use the   |
|                          |                         |EXT3 file system. This   |
|                          |                         |is the default setting   |
|                          |                         |for applicable Rackspace |
|                          |                         |base images. MANUAL:The  |
|                          |                         |server is built using    |
|                          |                         |the partition scheme and |
|                          |                         |file system of the       |
|                          |                         |source image. If the     |
|                          |                         |target flavor disk is    |
|                          |                         |larger, the remaining    |
|                          |                         |disk space is left       |
|                          |                         |unpartitioned. This      |
|                          |                         |enables images to have   |
|                          |                         |non-EXT3 file systems,   |
|                          |                         |multiple partitions, and |
|                          |                         |so on, and it enables    |
|                          |                         |you to manage the disk   |
|                          |                         |configuration.           |
+--------------------------+-------------------------+-------------------------+





**Example Rebuild Specified Server: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|server                    |csapi:object *(Required)*|The container for server |
|                          |                         |data.                    |
+--------------------------+-------------------------+-------------------------+
|id                        |csapi:UUID *(Required)*  |The ID of the server.    |
+--------------------------+-------------------------+-------------------------+
|links                     |csapi:UUID *(Required)*  |An array of the self and |
|                          |                         |bookmark links to the    |
|                          |                         |server.                  |
+--------------------------+-------------------------+-------------------------+
|href                      |csapi:UUID *(Required)*  |The URL for the server   |
|                          |                         |and the associated       |
|                          |                         |``rel``.                 |
+--------------------------+-------------------------+-------------------------+
|rel                       |csapi:UUID *(Required)*  |The descriptive field    |
|                          |                         |for the associated       |
|                          |                         |``href``, which is       |
|                          |                         |either ``self`` or       |
|                          |                         |``bookmark``.            |
+--------------------------+-------------------------+-------------------------+
|adminPass                 |csapi:string *(Required)*|The password assigned to |
|                          |                         |provide login access to  |
|                          |                         |the server.              |
+--------------------------+-------------------------+-------------------------+
|OS-DCF:diskConfig         |csapi:string *(Required)*|The disk configuration   |
|                          |                         |value. Valid values are  |
|                          |                         |``AUTO`` and ``MANUAL``. |
+--------------------------+-------------------------+-------------------------+





**Example Rebuild Specified Server: JSON request**


.. code::

    Status Code: 202 OKContent-Length: 1250Content-Type: application/jsonDate: Thu, 04 Dec 2014 19:41:58 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)x-compute-request-id: req-8c905dfe-2c9a-42d9-8e53-4478e2813c75

