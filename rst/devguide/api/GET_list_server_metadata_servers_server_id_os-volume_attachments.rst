=============================================================================
List Server Metadata -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

List Server Metadata
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <GET_list_server_metadata_servers_server_id_os-volume_attachments.rst#request>`__
`Response <GET_list_server_metadata_servers_server_id_os-volume_attachments.rst#response>`__

.. code-block:: javascript

    GET /servers/{server_id}/os-volume_attachments

Retrieve list of all attached volumes for a specified server.

In the URI, specify the target server ID.

For information about creating volumes, see `Rackspace Cloud Block Storage Developer Guide <http://docs.rackspace.com/cbs/api/v1.0/cbs-devguide/content/index.html>`__.



This table shows the possible response codes for this operation:


+--------------------------+-------------------------+-------------------------+
|Response Code             |Name                     |Description              |
+==========================+=========================+=========================+
|200 203 300               |Success                  |Request succeeded.       |
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








**Example List Server Metadata: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|volumeAttachemnts         |array                    |The array of attached    |
|                          |                         |volumes.                 |
+--------------------------+-------------------------+-------------------------+
|device                    |xsd:string               |The name of the device,  |
|                          |                         |such as /dev/xvdb.       |
+--------------------------+-------------------------+-------------------------+
|Id                        |xsd:string               |The ID of the volume     |
|                          |                         |attached to the server   |
|                          |                         |instance.                |
+--------------------------+-------------------------+-------------------------+
|serverId                  |xsd:string               |The ID of the server     |
|                          |                         |instance to which the    |
|                          |                         |volume is attached.      |
+--------------------------+-------------------------+-------------------------+
|volumeId                  |xsd:string               |The ID of the volume     |
|                          |                         |attached to the server   |
|                          |                         |instance.                |
+--------------------------+-------------------------+-------------------------+





**Example List Server Metadata: JSON request**


.. code::

    Status Code: 200 OKContent-Length: 120Content-Type: application/jsonDate: Mon, 19 Jan 2015 19:22:30 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)x-compute-request-id: req-206e007a-9dfe-4ac4-b819-d64a74244506

