=============================================================================
Attach Voume To Server -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Attach Voume To Server
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <PUT_attach_voume_to_server_servers_server_id_os-volume_attachments.rst#request>`__
`Response <PUT_attach_voume_to_server_servers_server_id_os-volume_attachments.rst#response>`__

.. code-block:: javascript

    PUT /servers/{server_id}/os-volume_attachments

Attaches volume to a specified server

You can attach one or more volumes in a single request.

For information about creating volumes, see `Rackspace Cloud Block Storage Developer Guide <http://docs.rackspace.com/cbs/api/v1.0/cbs-devguide/content/index.html>`__.



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
|volumeAttachemnt          |object *(Required)*      |The container for the    |
|                          |                         |volume attachemnt        |
|                          |                         |specifications.          |
+--------------------------+-------------------------+-------------------------+
|device                    |xsd:string *(Required)*  |The name of the device,  |
|                          |                         |such as /dev/xvdb.       |
|                          |                         |Specify ``null`` for     |
|                          |                         |auto-assignment.         |
+--------------------------+-------------------------+-------------------------+
|volumeId                  |object *(Required)*      |The ID of the volume     |
|                          |                         |that you want to attach  |
|                          |                         |to the server instance.  |
+--------------------------+-------------------------+-------------------------+





**Example Attach Voume To Server: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|volumeAttachemnt          |object *(Required)*      |The container for the    |
|                          |                         |volume attachemnt        |
|                          |                         |specifications.          |
+--------------------------+-------------------------+-------------------------+
|device                    |xsd:string *(Required)*  |The name of the device,  |
|                          |                         |such as /dev/xvdb.       |
|                          |                         |Specify ``null`` for     |
|                          |                         |auto-assignment.         |
+--------------------------+-------------------------+-------------------------+
|Id                        |xsd:string *(Required)*  |The ID of the volume     |
|                          |                         |that you attached to the |
|                          |                         |server instance.         |
+--------------------------+-------------------------+-------------------------+
|serverId                  |xsd:string *(Required)*  |The ID of the server     |
|                          |                         |instance to which you    |
|                          |                         |attached the volume.     |
+--------------------------+-------------------------+-------------------------+
|volumeId                  |xsd:string *(Required)*  |The ID of the volume     |
|                          |                         |that you attached to the |
|                          |                         |server instance.         |
+--------------------------+-------------------------+-------------------------+





**Example Attach Voume To Server: JSON request**


.. code::

    Status Code: 202 OKContent-Length: 120Content-Type: application/jsonDate: Mon, 19 Jan 2015 19:22:30 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)x-compute-request-id: req-206e007a-9dfe-4ac4-b819-d64a74244506

