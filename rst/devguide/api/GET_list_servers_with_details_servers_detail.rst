=============================================================================
List Servers With Details -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

List Servers With Details
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <GET_list_servers_with_details_servers_detail.rst#request>`__
`Response <GET_list_servers_with_details_servers_detail.rst#response>`__

.. code-block:: javascript

    GET /servers/detail

Retrieves a detailed list of all servers in the tenant's account.

Servers contain a status attribute that indicates the current server state. You can filter on the server status when you complete a list servers request. The server status is returned in the response body. For a full list of possible server status values, see.

The following extensions provide additional information when viewing server details:

Config Drive:

Scheduled Images:

Extended Status ( ``OS-EXT-STS:power_state``, ``OS-EXT-STS:vm_state``, and ``OS-EXT-STS:task_state`` ):

Block Device Mapping:

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







**Example List Servers With Details: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|servers                   |array                    |An array of servers.     |
+--------------------------+-------------------------+-------------------------+
|accessIPv4                |csapi:IP                 |The public IP version 4  |
|                          |                         |access address.          |
+--------------------------+-------------------------+-------------------------+
|accessIPv6                |csapi:IP                 |The public IP version 6  |
|                          |                         |access address.          |
+--------------------------+-------------------------+-------------------------+
|addresses                 |array                    |An array of addresses    |
|                          |                         |for public, private, and |
|                          |                         |isolated networks        |
|                          |                         |attached to the server.  |
+--------------------------+-------------------------+-------------------------+
|addr                      |array                    |The IP address of the    |
|                          |                         |network.                 |
+--------------------------+-------------------------+-------------------------+
|version                   |array                    |The version of the IP    |
|                          |                         |address of the network.  |
+--------------------------+-------------------------+-------------------------+
|id                        |csapi:UUID               |The ID of the server.    |
+--------------------------+-------------------------+-------------------------+
|created                   |csapi:UUID               |The time stamp           |
|                          |                         |indicating the creation  |
|                          |                         |date of the server.      |
+--------------------------+-------------------------+-------------------------+
|flavor                    |csapi:UUID               |The flavor ID..          |
+--------------------------+-------------------------+-------------------------+
|image                     |csapi:UUID               |The image ID..           |
+--------------------------+-------------------------+-------------------------+
|hostId                    |csapi:UUID               |The host ID. The compute |
|                          |                         |provisioning algorithm   |
|                          |                         |has an anti-affinity     |
|                          |                         |property that attempts   |
|                          |                         |to spread customer VMs   |
|                          |                         |across hosts. Under      |
|                          |                         |certain situations, VMs  |
|                          |                         |from the same customer   |
|                          |                         |might be placed on the   |
|                          |                         |same host. hostId        |
|                          |                         |represents the host your |
|                          |                         |server runs on and can   |
|                          |                         |be used to determine     |
|                          |                         |this scenario if it is   |
|                          |                         |relevant to your         |
|                          |                         |application. HostId is   |
|                          |                         |unique only for an       |
|                          |                         |account and is not       |
|                          |                         |globally unique.         |
+--------------------------+-------------------------+-------------------------+
|links                     |csapi:UUID               |An array of the self and |
|                          |                         |bookmark links to the    |
|                          |                         |server.                  |
+--------------------------+-------------------------+-------------------------+
|href                      |csapi:UUID               |The URL for the server   |
|                          |                         |and the associated       |
|                          |                         |``rel``.                 |
+--------------------------+-------------------------+-------------------------+
|rel                       |csapi:UUID               |The descriptive field    |
|                          |                         |for the associated       |
|                          |                         |``href``, which is       |
|                          |                         |either ``self`` or       |
|                          |                         |``bookmark``.            |
+--------------------------+-------------------------+-------------------------+
|metadata                  |csapi:string             |Any metadata key and     |
|                          |                         |value pairs.             |
+--------------------------+-------------------------+-------------------------+
|name                      |csapi:string             |The server name.         |
+--------------------------+-------------------------+-------------------------+
|progress                  |csapi:string             |The build completion     |
|                          |                         |progress, as a           |
|                          |                         |percentage. Value ranges |
|                          |                         |from 0 to 100.           |
+--------------------------+-------------------------+-------------------------+
|status                    |csapi:string             |The status of the        |
|                          |                         |server. For a full list  |
|                          |                         |of possible status       |
|                          |                         |values, see.             |
+--------------------------+-------------------------+-------------------------+
|tenant_id                 |csapi:string             |The tenant ID.           |
+--------------------------+-------------------------+-------------------------+
|updated                   |csapi:string             |The time stamp of the    |
|                          |                         |last update.             |
+--------------------------+-------------------------+-------------------------+
|user_id                   |csapi:string             |The user ID.             |
+--------------------------+-------------------------+-------------------------+
|OS-DCF:diskConfig         |csapi:string             |Extended attribute: The  |
|                          |                         |disk configuration       |
|                          |                         |value.. Valid values are |
|                          |                         |``AUTO`` and ``MANUAL``. |
+--------------------------+-------------------------+-------------------------+
|RAX-SI:image_schedule     |csapi:string             |Extended attribute: The  |
|                          |                         |image schedule reference |
|                          |                         |is included only if      |
|                          |                         |scheduled images has     |
|                          |                         |been enabled for this    |
|                          |                         |server..                 |
+--------------------------+-------------------------+-------------------------+
|OS-EXT-STS                |csapi:string             |Extended attribute.      |
|                          |                         |Shows the extended       |
|                          |                         |statuses for the server, |
|                          |                         |including the VM, task,  |
|                          |                         |and power states..       |
+--------------------------+-------------------------+-------------------------+
|RAX-PUBLIC-IP-ZONE-       |xsd:UUID                 |Extended attribute.      |
|ID:publicIPZoneId         |                         |Enables booting the      |
|                          |                         |server from a volume     |
|                          |                         |when additional          |
|                          |                         |parameters are given. If |
|                          |                         |specified, the volume    |
|                          |                         |status must be           |
|                          |                         |``available``, and the   |
|                          |                         |volume attach_status     |
|                          |                         |must be ``detached``.    |
+--------------------------+-------------------------+-------------------------+
|next                      |xsd:anyURI               |Moves to the next        |
|                          |                         |metadata item.           |
+--------------------------+-------------------------+-------------------------+
|previous                  |xsd:anyURI               |Moves to the previous    |
|                          |                         |metadata item.           |
+--------------------------+-------------------------+-------------------------+





**Example List Servers With Details: JSON request**


.. code::

    Status Code: 200 OKContent-Length: 4543Content-Type: application/jsonDate: Wed, 03 Dec 2014 17:13:30 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)x-compute-request-id: req-7b7ffed2-9b1f-46a8-a478-315518d35387

