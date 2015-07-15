=============================================================================
Show Server Metadata Item Details -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Show Server Metadata Item Details
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <GET_show_server_metadata_item_details_servers_server_id_metadata_key_.rst#request>`__
`Response <GET_show_server_metadata_item_details_servers_server_id_metadata_key_.rst#response>`__

.. code-block:: javascript

    GET /servers/{server_id}/metadata/{key}

Retrieve metadata item by key for a specified server.

In the URI, specify the target server ID and the target metadata key.



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
|{key}                     |csapi:MetadataKey        |The name of the target   |
|                          |                         |key in a metadata key    |
|                          |                         |pair. A string with      |
|                          |                         |maximum length of 255    |
|                          |                         |characters.              |
+--------------------------+-------------------------+-------------------------+
|{server_id}               |csapi:UUID               |The UUID for the server. |
+--------------------------+-------------------------+-------------------------+








**Example Show Server Metadata Item Details: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|meta                      |object *(Required)*      |Container for a metadata |
|                          |                         |keypair for the          |
|                          |                         |specified server. This   |
|                          |                         |container holds a single |
|                          |                         |keypair using format of  |
|                          |                         |"metadata key" :         |
|                          |                         |"metadata value".        |
+--------------------------+-------------------------+-------------------------+
|keyname                   |keypair *(Required)*     |Keypair describing the   |
|                          |                         |metadata using format of |
|                          |                         |"keyname" : "keyvalue".  |
+--------------------------+-------------------------+-------------------------+





**Example Show Server Metadata Item Details: JSON request**


.. code::

    Status Code: 200 OKContent-Length: 32Content-Type: application/jsonDate: Tue, 20 Jan 2015 14:07:57 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)x-compute-request-id: req-85a2fdf4-a6d9-42ce-91bb-2cea8eb5e14e

