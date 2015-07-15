=============================================================================
Resize Specified Server -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Resize Specified Server
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <POST_resize_specified_server_servers_server_id_actions.rst#request>`__
`Response <POST_resize_specified_server_servers_server_id_actions.rst#response>`__

.. code-block:: javascript

    POST /servers/{server_id}/actions

Resize the specified server.

This operation converts an existing Standard server to a different flavor, which scales the server up or down. The original server is saved for a period of time to allow roll back if a problem occurs. You should test and explicitly confirm all resizes. When you do so, the original server is removed. All resizes are automatically confirmed after 24 hours if you do not explicitly confirm or revert the resize.

This operation is not available for OnMetal servers.

``Resize is only available for Standard flavors. If you have a Compute, Memory, or IO flavor server, and you need to change the size of your data disk(s), you will need to: Image your system disk. Back-up your data disk(s), using Cloud Backup or Cloud Block Storage. Create a new server with the desired size and flavor class, using your image. Add your backed-up data to the new data disk(s). Delete the old server, once you are satisfied with the new server.

 For General Purpose servers, use steps 1, 3, and 5 from the preceding list.

``Specify the target server ID in the URI.

In the request body, specify the ``resize`` action followed by attributes.



This table shows the possible response codes for this operation:


+--------------------------+-------------------------+-------------------------+
|Response Code             |Name                     |Description              |
+==========================+=========================+=========================+
|202                       |Successful               |Request succeeded.       |
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
|resize                    |object *(Required)*      |Specification of the     |
|                          |                         |resize action for the    |
|                          |                         |specified server.        |
+--------------------------+-------------------------+-------------------------+
|flavorRef                 |object *(Required)*      |The flavorRef for the    |
|                          |                         |new server.              |
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





**Example Resize Specified Server: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^





**Example Resize Specified Server: JSON request**


.. code::

    Status Code: 202 No ContentContent-Length: 0Content-Type: application/jsonDate: Thu, 04 Dec 2014 21:45:47 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)x-compute-request-id

