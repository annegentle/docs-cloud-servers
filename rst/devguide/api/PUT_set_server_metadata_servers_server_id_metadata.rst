=============================================================================
Set Server Metadata -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Set Server Metadata
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <PUT_set_server_metadata_servers_server_id_metadata.rst#request>`__
`Response <PUT_set_server_metadata_servers_server_id_metadata.rst#response>`__

.. code-block:: javascript

    PUT /servers/{server_id}/metadata

Create or replace metadata items for a specified server

You can add or update one or more new metadata items in a single request.

If metadata items in the request body do not exist, they are created. If they do exist, they are replaced.

Existing metadata items are replaced with the ones provided in the request regardless of the names of the original metadata items.

If you exceed the maximum number of metadata items in the request, the call throws an ``overLimit (413)`` fault. To find the maximum number of key-value pairs that can be supplied for each server, use the maxServerMeta absolute limit query.

In the URI, specify the target server ID.

In the request body, specify the ``metadata`` element, followed by the new metadata key, for example ``version``, with the value for that key.



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
|{server_id}               |csapi:UUID               |The UUID for the server. |
+--------------------------+-------------------------+-------------------------+





This table shows the body parameters for the request:

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





**Example Set Server Metadata: JSON request**


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





**Example Set Server Metadata: JSON request**


.. code::

    Status Code: 200 OKContent-Length: 120Content-Type: application/jsonDate: Mon, 19 Jan 2015 19:22:30 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)x-compute-request-id: req-206e007a-9dfe-4ac4-b819-d64a74244506

