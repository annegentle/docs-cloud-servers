=============================================================================
Show Volume Attachment Details -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Show Volume Attachment Details
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <PUT_show_volume_attachment_details_servers_server_id_os-volume_attachments_attachment_id_.rst#request>`__
`Response <PUT_show_volume_attachment_details_servers_server_id_os-volume_attachments_attachment_id_.rst#response>`__

.. code-block:: javascript

    PUT /servers/{server_id}/os-volume_attachments/{attachment_id}

Retrieve volume details for the specified server ID and volume attachment ID

In the URI, specify the target server ID and the target attached volume ID to see details for that volume.



This table shows the possible response codes for this operation:


+--------------------------+-------------------------+-------------------------+
|Response Code             |Name                     |Description              |
+==========================+=========================+=========================+
|200                       |Success                  |Request succeeded.       |
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
|{attachment_id}           |xsd:UUID                 |The volume attachment ID.|
+--------------------------+-------------------------+-------------------------+
|{server_id}               |csapi:UUID               |The UUID for the server. |
+--------------------------+-------------------------+-------------------------+








**Example Show Volume Attachment Details: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|volumeAttachemnt          |object                   |The container for the    |
|                          |                         |volume attachemnt        |
|                          |                         |specifications.          |
+--------------------------+-------------------------+-------------------------+
|device                    |xsd:string               |The name of the device,  |
|                          |                         |such as /dev/xvdb.       |
|                          |                         |Specify ``null`` for     |
|                          |                         |auto-assignment.         |
+--------------------------+-------------------------+-------------------------+
|Id                        |xsd:string               |The ID of the volume     |
|                          |                         |that you attached to the |
|                          |                         |server instance.         |
+--------------------------+-------------------------+-------------------------+
|serverId                  |xsd:string               |The ID of the server     |
|                          |                         |instance to which you    |
|                          |                         |attached the volume.     |
+--------------------------+-------------------------+-------------------------+
|volumeId                  |xsd:string               |The ID of the volume     |
|                          |                         |that you attached to the |
|                          |                         |server instance.         |
+--------------------------+-------------------------+-------------------------+





**Example Show Volume Attachment Details: JSON request**


.. code::

    Status Code: 200 OKContent-Length: 32Content-Type: application/jsonDate: Tue, 20 Jan 2015 14:25:02 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)x-compute-request-id: req-96b3fdf4-a6d9-42ce-91bb-2cea8eb5e14e

