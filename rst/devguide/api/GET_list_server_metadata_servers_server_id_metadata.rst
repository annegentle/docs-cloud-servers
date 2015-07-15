=============================================================================
List Server Metadata -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

List Server Metadata
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <GET_list_server_metadata_servers_server_id_metadata.rst#request>`__
`Response <GET_list_server_metadata_servers_server_id_metadata.rst#response>`__

.. code-block:: javascript

    GET /servers/{server_id}/metadata

Retrieve list of all metadata for a specified server.

In the URI, specify the target server ID.



This table shows the possible response codes for this operation:


+--------------------------+-------------------------+-------------------------+
|Response Code             |Name                     |Description              |
+==========================+=========================+=========================+
|200 203                   |Success                  |Request succeeded.       |
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





**Example List Server Metadata: JSON request**


.. code::

    Status Code: 200 OKContent-Length: 120Content-Type: application/jsonDate: Mon, 19 Jan 2015 19:22:30 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)x-compute-request-id: req-206e007a-9dfe-4ac4-b819-d64a74244506

