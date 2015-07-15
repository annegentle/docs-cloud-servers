=============================================================================
Retrieve List Of Server Addresses -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Retrieve List Of Server Addresses
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <GET_retrieve_list_of_server_addresses_servers_server_id_ips.rst#request>`__
`Response <GET_retrieve_list_of_server_addresses_servers_server_id_ips.rst#response>`__

.. code-block:: javascript

    GET /servers/{server_id}/ips

Retrieve list of all server and network addresses associated with the specified server.

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








**Example Retrieve List Of Server Addresses: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|addresses                 |object *(Required)*      |A container for one or   |
|                          |                         |more server details to   |
|                          |                         |be updated.              |
+--------------------------+-------------------------+-------------------------+
|nettype                   |object *(Required)*      |An array of ``private``  |
|                          |                         |or ``public`` network    |
|                          |                         |address containers.      |
+--------------------------+-------------------------+-------------------------+
|addr                      |object *(Required)*      |The IP address.          |
+--------------------------+-------------------------+-------------------------+
|version                   |object *(Required)*      |The IP address version,  |
|                          |                         |either ``4`` or ``6``.   |
+--------------------------+-------------------------+-------------------------+





**Example Retrieve List Of Server Addresses: JSON request**


.. code::

    Status Code: 200 OKContent-Length: 191Content-Type: application/jsonDate: Fri, 12 Dec 2014 16:37:29 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)X-Compute-Request-Id: req-624fa036-8f73-4ca9-aa22-428df756c578

