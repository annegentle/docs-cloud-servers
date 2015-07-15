=============================================================================
Delete Volume Attachment From Server -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Delete Volume Attachment From Server
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <DELETE_delete_volume_attachment_from_server_servers_server_id_os-volume_attachments_attachment_id_.rst#request>`__
`Response <DELETE_delete_volume_attachment_from_server_servers_server_id_os-volume_attachments_attachment_id_.rst#response>`__

.. code-block:: javascript

    DELETE /servers/{server_id}/os-volume_attachments/{attachment_id}

Deletes the specified volume attachment from the specified server.

If the operation succeeds, it returns an ``HTTP 202`` status code with no response body.

In the URI, specify the target server ID and the target attached volume ID.



This table shows the possible response codes for this operation:


+--------------------------+-------------------------+-------------------------+
|Response Code             |Name                     |Description              |
+==========================+=========================+=========================+
|202                       |Delete Successful        |Delete request succeeded.|
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








**Example Delete Volume Attachment From Server: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^





**Example Delete Volume Attachment From Server: JSON request**


.. code::

    Status Code: 202 OKContent-Length: 120Content-Type: application/jsonDate: Mon, 19 Jan 2015 23:19:30 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)x-compute-request-id: req-406a007a-9dfe-4ac4-b819-d64a74244506

