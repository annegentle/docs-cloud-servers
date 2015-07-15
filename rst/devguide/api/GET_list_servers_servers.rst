=============================================================================
List Servers -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

List Servers
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <GET_list_servers_servers.rst#request>`__
`Response <GET_list_servers_servers.rst#response>`__

.. code-block:: javascript

    GET /servers

Retrieve list of all servers (only IDs, names, and links).

Servers contain a status attribute that indicates the current server state. You can filter on the server status when you complete a list servers request. The server status is returned in the response body.

For a full list of possible server status values, see.

For more information on the extended status extension ( ``OS-EXT-STS:power_state``, ``OS-EXT-STS:vm_state``, and ``OS-EXT-STS:task_state`` see.



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




This table shows the query parameters for the request:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|changes-since             |xsd:dateTime *(Required)*|A time/date stamp for    |
|                          |                         |when the server last     |
|                          |                         |changed status.          |
+--------------------------+-------------------------+-------------------------+
|image                     |csapi:UUID *(Required)*  |The image reference for  |
|                          |                         |the desired image for    |
|                          |                         |your server instance.    |
+--------------------------+-------------------------+-------------------------+
|flavor                    |csapi:UUID *(Required)*  |The flavor reference for |
|                          |                         |the desired flavor for   |
|                          |                         |your server instance.    |
+--------------------------+-------------------------+-------------------------+
|name                      |regexp *(Required)*      |The name of the server,  |
|                          |                         |which can be queried     |
|                          |                         |with regular             |
|                          |                         |expressions. Notice that |
|                          |                         |?name=bob returns both   |
|                          |                         |"bob" and "bobbin". If   |
|                          |                         |you need to match only   |
|                          |                         |"bob", use a regular     |
|                          |                         |expression matching the  |
|                          |                         |syntax of the underlying |
|                          |                         |database server          |
|                          |                         |implemented for Cloud    |
|                          |                         |Servers (such as MySQL   |
|                          |                         |or PostgreSQL).          |
+--------------------------+-------------------------+-------------------------+
|marker                    |csapi:UUID *(Required)*  |The UUID of the server   |
|                          |                         |at which you want to set |
|                          |                         |a marker.                |
+--------------------------+-------------------------+-------------------------+
|limit                     |xsd:int *(Required)*     |The integer value used   |
|                          |                         |to limit the number of   |
|                          |                         |values which will be     |
|                          |                         |returned.                |
+--------------------------+-------------------------+-------------------------+
|status                    |csapi:ServerStatus       |The status of the        |
|                          |*(Required)*             |server. For example, you |
|                          |                         |can filter on "ACTIVE".  |
|                          |                         |For a full list of       |
|                          |                         |possible status values,  |
|                          |                         |see                      |
+--------------------------+-------------------------+-------------------------+
|host                      |xsd:string *(Required)*  |The name of the host.    |
+--------------------------+-------------------------+-------------------------+







**Example List Servers: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|id                        |csapi:UUID *(Required)*  |The ID of the server.    |
+--------------------------+-------------------------+-------------------------+
|links                     |csapi:UUID *(Required)*  |An array of the self and |
|                          |                         |bookmark links to the    |
|                          |                         |server.                  |
+--------------------------+-------------------------+-------------------------+
|href                      |csapi:UUID *(Required)*  |The URL for the server   |
|                          |                         |and the associated       |
|                          |                         |``rel``.                 |
+--------------------------+-------------------------+-------------------------+
|rel                       |csapi:UUID *(Required)*  |The descriptive field    |
|                          |                         |for the associated       |
|                          |                         |``href``, which is       |
|                          |                         |either ``self`` or       |
|                          |                         |``bookmark``.            |
+--------------------------+-------------------------+-------------------------+
|name                      |csapi:string *(Required)*|The server name.         |
+--------------------------+-------------------------+-------------------------+
|next                      |xsd:anyURI *(Required)*  |Moves to the next        |
|                          |                         |metadata item.           |
+--------------------------+-------------------------+-------------------------+
|previous                  |xsd:anyURI *(Required)*  |Moves to the previous    |
|                          |                         |metadata item.           |
+--------------------------+-------------------------+-------------------------+





**Example List Servers: JSON request**


.. code::

    Status Code: 200 OKContent-Length: 1024Content-Type: application/jsonDate: Wed, 03 Dec 2014 14:40:57 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)x-compute-request-id: req-fda78f69-d934-4ed3-a5b8-255894baa6aa

