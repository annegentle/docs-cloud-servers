=============================================================================
Delete Virtual Interface -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Delete Virtual Interface
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <DELETE_delete_virtual_interface_servers_server_id_os-virtual-interfacesv2_interface_id_.rst#request>`__
`Response <DELETE_delete_virtual_interface_servers_server_id_os-virtual-interfacesv2_interface_id_.rst#response>`__

.. code-block:: javascript

    DELETE /servers/{server_id}/os-virtual-interfacesv2/{interface_id}

Deletes a virtual interface from a server instance.

This operation deletes the specified virtual interface from the specified server instance.



This table shows the possible response codes for this operation:


+--------------------------+-------------------------+-------------------------+
|Response Code             |Name                     |Description              |
+==========================+=========================+=========================+
|200                       |Delete Successful        |Delete request succeeded.|
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
|{interface_id}            |csapi:UUID               |The interface ID.        |
+--------------------------+-------------------------+-------------------------+
|{server_id}               |csapi:UUID               |The UUID for the server. |
+--------------------------+-------------------------+-------------------------+








**Example Delete Virtual Interface: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^





**Example Delete Virtual Interface: JSON request**


.. code::

    Status Code: 200 OKContent-Length: 0Content-Type: application/jsonDate: Wed, 08 Apr 2015 17:09:53 GMT, Wed, 08 Apr 2015 17:09:59 GMTServer: Jetty(9.2.z-SNAPSHOT)Via: 1.1 Repose (Repose/6.2.1.2)X-Compute-Request-Id: req-12a961ef-4cf3-419e-9ea5-b7afeb184691

