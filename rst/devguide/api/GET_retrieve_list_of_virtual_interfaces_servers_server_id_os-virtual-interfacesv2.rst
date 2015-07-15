=============================================================================
Retrieve List Of Virtual Interfaces -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Retrieve List Of Virtual Interfaces
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <GET_retrieve_list_of_virtual_interfaces_servers_server_id_os-virtual-interfacesv2.rst#request>`__
`Response <GET_retrieve_list_of_virtual_interfaces_servers_server_id_os-virtual-interfacesv2.rst#response>`__

.. code-block:: javascript

    GET /servers/{server_id}/os-virtual-interfacesv2

Retrieves list of the virtual interfaces configured for a server instance.

This operation lists the virtual interfaces configured for a server instance.



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








Response
^^^^^^^^^^^^^^^^^^


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|virtual_interfaces        |array                    |The array of virtual     |
|                          |                         |interfaces.              |
+--------------------------+-------------------------+-------------------------+
|id                        |xsd:string               |The virtual interface ID.|
+--------------------------+-------------------------+-------------------------+
|ip_addresses              |array                    |The array of interface   |
|                          |                         |IP address details.      |
+--------------------------+-------------------------+-------------------------+
|address                   |xsd:string               |The interface IP address.|
+--------------------------+-------------------------+-------------------------+
|network_id                |xsd:UUID                 |The interface network ID.|
+--------------------------+-------------------------+-------------------------+
|network_label             |xsd:string               |The interface network    |
|                          |                         |label.                   |
+--------------------------+-------------------------+-------------------------+
|mac_address               |xsd:string               |The Media Access Control |
|                          |                         |(MAC) address for the    |
|                          |                         |virtual interface. A MAC |
|                          |                         |address is a unique      |
|                          |                         |identifier assigned to   |
|                          |                         |network interfaces for   |
|                          |                         |communications on the    |
|                          |                         |physical network segment.|
+--------------------------+-------------------------+-------------------------+





**Example Retrieve List Of Virtual Interfaces: JSON request**


.. code::

    Status Code: 200 OKContent-Length: 585Content-Type: application/jsonDate: Wed, 08 Apr 2015 14:24:10 GMT, Wed, 08 Apr 2015 14:24:11 GMTServer: Jetty(9.2.z-SNAPSHOT)Via: 1.1 Repose (Repose/6.2.1.2)X-Compute-Request-Id: req-3c46ba6b-36c6-42cd-a813-df476b396161

