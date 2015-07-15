=============================================================================
Create Network -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Create Network
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <POST_create_network_os-networksv2.rst#request>`__
`Response <POST_create_network_os-networksv2.rst#response>`__

.. code-block:: javascript

    POST /os-networksv2

Creates a network for the specified tenant ID.

This operation creates a network for the tenant ID specified in the request URI.



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






This table shows the body parameters for the request:

+--------+-------------+----------------------------------------------------------+
|Name    |Type         |Description                                               |
+========+=============+==========================================================+
|network |object       |A container of network details.                           |
|        |*(Required)* |                                                          |
+--------+-------------+----------------------------------------------------------+
|cidr    |csapi:UUID   |The IP block from which to allocate the network. For      |
|        |*(Required)* |example, 172.16.0.0/24 or 2001:DB8::/64. For more         |
|        |             |information about CIDR notation, see `Using CIDR Notation |
|        |             |in Cloud Networks                                         |
|        |             |<http://www.rackspace.com/knowledge_center/article/using- |
|        |             |cidr-notation>`__ in the Knowledge Center.                |
+--------+-------------+----------------------------------------------------------+
|label   |xsd:string   |The name of the new network. For example, my_new_network. |
|        |*(Required)* |                                                          |
+--------+-------------+----------------------------------------------------------+





**Example Create Network: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|network                   |object *(Required)*      |A container of network   |
|                          |                         |details.                 |
+--------------------------+-------------------------+-------------------------+
|cidr                      |xsd:string *(Required)*  |The CIDR for an isolated |
|                          |                         |network.                 |
+--------------------------+-------------------------+-------------------------+
|id                        |xsd:string *(Required)*  |The network ID.          |
+--------------------------+-------------------------+-------------------------+
|label                     |xsd:string *(Required)*  |The name of the network. |
|                          |                         |ServiceNet is labeled as |
|                          |                         |private and PublicNet is |
|                          |                         |labeled as public in the |
|                          |                         |network list.            |
+--------------------------+-------------------------+-------------------------+





**Example Create Network: JSON request**


.. code::

    Status Code: 200 OKContent-Length: 110Content-Type: application/jsonDate: Mon, 13 Apr 2015 19:04:21 GMT, Mon, 13 Apr 2015 19:04:24 GMTServer: Jetty(9.2.z-SNAPSHOT)Via: 1.1 Repose (Repose/6.2.1.2)X-Compute-Request-Id: req-175c37e9-60a7-42de-9922-5bf95644dad2

