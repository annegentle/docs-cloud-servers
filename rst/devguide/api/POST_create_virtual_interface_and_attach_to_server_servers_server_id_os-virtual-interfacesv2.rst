=============================================================================
Create Virtual Interface And Attach To Server -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Create Virtual Interface And Attach To Server
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <POST_create_virtual_interface_and_attach_to_server_servers_server_id_os-virtual-interfacesv2.rst#request>`__
`Response <POST_create_virtual_interface_and_attach_to_server_servers_server_id_os-virtual-interfacesv2.rst#response>`__

.. code-block:: javascript

    POST /servers/{server_id}/os-virtual-interfacesv2

Creates a virtual interface for a network and attaches it to a server.

This operation creates a virtual interface for a network and attaches the network to a server instance.

You can create a maximum of one virtual interface per instance per network.



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
|virtual_interface         |object                   |A container with virtual |
|                          |                         |interface information.   |
+--------------------------+-------------------------+-------------------------+
|network_id                |xsd:UUID                 |The interface network ID.|
+--------------------------+-------------------------+-------------------------+





**Example Create Virtual Interface And Attach To Server: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


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





**Example Create Virtual Interface And Attach To Server: JSON request**


.. code::

    Status Code: 200 OKContent-Length: 247Content-Type: application/jsonDate: Wed, 08 Apr 2015 18:03:16 GMT, Wed, 08 Apr 2015 18:03:23 GMTServer: Jetty(9.2.z-SNAPSHOT)Via: 1.1 Repose (Repose/6.2.1.2)X-Compute-Request-Id: req-f28cbcae-fe5e-4318-908a-dd6a9cb23122

