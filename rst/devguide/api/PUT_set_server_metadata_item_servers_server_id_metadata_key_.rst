=============================================================================
Set Server Metadata Item -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Set Server Metadata Item
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <PUT_set_server_metadata_item_servers_server_id_metadata_key_.rst#request>`__
`Response <PUT_set_server_metadata_item_servers_server_id_metadata_key_.rst#response>`__

.. code-block:: javascript

    PUT /servers/{server_id}/metadata/{key}

Create or replace metadata item by key for a specified server

In the URI, specify the target server ID and the target metadata key.

In the request body, specify the ``meta`` element, followed by the metadata key, for example ``version``, with the new value for that key.

The key specified in the request body must match the key specified in the URI request.



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
|{key}                     |csapi:MetadataKey        |The name of the target   |
|                          |                         |key in a metadata key    |
|                          |                         |pair. A string with      |
|                          |                         |maximum length of 255    |
|                          |                         |characters.              |
+--------------------------+-------------------------+-------------------------+
|{server_id}               |csapi:UUID               |The UUID for the server. |
+--------------------------+-------------------------+-------------------------+





This table shows the body parameters for the request:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|meta                      |object                   |Container for a metadata |
|                          |                         |keypair for the          |
|                          |                         |specified server. This   |
|                          |                         |container holds a single |
|                          |                         |keypair using format of  |
|                          |                         |"metadata key" :         |
|                          |                         |"metadata value".        |
+--------------------------+-------------------------+-------------------------+
|keyname                   |keypair                  |Keypair describing the   |
|                          |                         |metadata using format of |
|                          |                         |"keyname" : "keyvalue".  |
+--------------------------+-------------------------+-------------------------+





**Example Set Server Metadata Item: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|metadata                  |object                   |Container for a metadata |
|                          |                         |keypair for the          |
|                          |                         |specified server. This   |
|                          |                         |container holds one or   |
|                          |                         |more keypairs using      |
|                          |                         |format of "metadata key" |
|                          |                         |: "metadata value".      |
+--------------------------+-------------------------+-------------------------+
|keyname                   |keypair                  |Keypairs edcribing the   |
|                          |                         |metadata using format of |
|                          |                         |"keyname" : "keyvalue".  |
+--------------------------+-------------------------+-------------------------+





**Example Set Server Metadata Item: JSON request**


.. code::

    Status Code: 200 OKContent-Length: 32Content-Type: application/jsonDate: Tue, 20 Jan 2015 14:25:02 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)x-compute-request-id: req-96b3fdf4-a6d9-42ce-91bb-2cea8eb5e14e

