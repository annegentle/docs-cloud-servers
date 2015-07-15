=============================================================================
Delete Server Metadata Item -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Delete Server Metadata Item
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <DELETE_delete_server_metadata_item_servers_server_id_metadata_key_.rst#request>`__
`Response <DELETE_delete_server_metadata_item_servers_server_id_metadata_key_.rst#response>`__

.. code-block:: javascript

    DELETE /servers/{server_id}/metadata/{key}

Deletes a metadata item by key from the specified server.

If the operation succeeds, it returns an ``HTTP 202`` status code with no response body.

In the URI, specify the target server ID and the target metadata key.



This table shows the possible response codes for this operation:


+--------------------------+-------------------------+-------------------------+
|Response Code             |Name                     |Description              |
+==========================+=========================+=========================+
|204                       |Delete Successful        |Delete request succeeded.|
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
|{key}                     |csapi:MetadataKey        |The name of the target   |
|                          |                         |key in a metadata key    |
|                          |                         |pair. A string with      |
|                          |                         |maximum length of 255    |
|                          |                         |characters.              |
+--------------------------+-------------------------+-------------------------+
|{server_id}               |csapi:UUID               |The UUID for the server. |
+--------------------------+-------------------------+-------------------------+








**Example Delete Server Metadata Item: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^





**Example Delete Server Metadata Item: JSON request**


.. code::

    Status Code: 204 OKContent-Length: 120Content-Type: application/jsonDate: Mon, 19 Jan 2015 23:19:30 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)x-compute-request-id: req-406a007a-9dfe-4ac4-b819-d64a74244506

