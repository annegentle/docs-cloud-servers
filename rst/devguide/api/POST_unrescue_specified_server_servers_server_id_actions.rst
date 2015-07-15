=============================================================================
Unrescue Specified Server -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Unrescue Specified Server
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <POST_unrescue_specified_server_servers_server_id_actions.rst#request>`__
`Response <POST_unrescue_specified_server_servers_server_id_actions.rst#response>`__

.. code-block:: javascript

    POST /servers/{server_id}/actions

Takes the specified server out of rescue mode.

After you resolve any problems and reboot a rescued server, you can unrescue the server. Specify the ``unrescue`` action in the request body. When you unrescue the server, the repaired image is restored to its running state with your original password.

You can exit rescue mode at any time.

Specify the target server ID in the URI.

In the request body, specify the ``unrescue`` action.



This table shows the possible response codes for this operation:


+--------------------------+-------------------------+-------------------------+
|Response Code             |Name                     |Description              |
+==========================+=========================+=========================+
|202                       |Successful               |Request succeeded.       |
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
|unrescue                  |object *(Required)*      |Specification of the     |
|                          |                         |unrescue action for the  |
|                          |                         |specified server.        |
+--------------------------+-------------------------+-------------------------+





**Example Unrescue Specified Server: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^





**Example Unrescue Specified Server: JSON request**


.. code::

    Status Code: 202 No ContentContent-Length: 0Content-Type: application/jsonDate: Thu, 04 Dec 2014 21:45:47 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)x-compute-request-id

