=============================================================================
Retrieve List Of Network Addresses For Server And Network -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Retrieve List Of Network Addresses For Server And Network
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <GET_retrieve_list_of_network_addresses_for_server_and_network_servers_server_id_ips_network_label_.rst#request>`__
`Response <GET_retrieve_list_of_network_addresses_for_server_and_network_servers_server_id_ips_network_label_.rst#response>`__

.. code-block:: javascript

    GET /servers/{server_id}/ips/{network_label}

Retrieve list of all server and network addresses associated with the specified server and network.

In the URI, specify the target server ID and target network type ( ``public`` or ``private`` ).



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
|{network_label}           |xsd:string               |The network label, such  |
|                          |                         |as ``public`` or         |
|                          |                         |``private``.             |
+--------------------------+-------------------------+-------------------------+
|{server_id}               |csapi:UUID               |The UUID for the server. |
+--------------------------+-------------------------+-------------------------+








**Example Retrieve List Of Network Addresses For Server And Network: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|nettype                   |object                   |An array of ``private``  |
|                          |                         |or ``public`` network    |
|                          |                         |address containers.      |
+--------------------------+-------------------------+-------------------------+
|addr                      |object                   |The IP address.          |
+--------------------------+-------------------------+-------------------------+
|version                   |object                   |The IP address version,  |
|                          |                         |either ``4`` or ``6``.   |
+--------------------------+-------------------------+-------------------------+





**Example Retrieve List Of Network Addresses For Server And Network: JSON request**


.. code::

    Status Code: 200 OKContent-Length: 121Content-Type: application/jsonDate: Fri, 12 Dec 2014 16:59:57 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)X-Compute-Request-Id: req-00daae97-384b-4a57-806c-dd8d2d635287

