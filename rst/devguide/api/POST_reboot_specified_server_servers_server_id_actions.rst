=============================================================================
Reboot Specified Server -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Reboot Specified Server
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <POST_reboot_specified_server_servers_server_id_actions.rst#request>`__
`Response <POST_reboot_specified_server_servers_server_id_actions.rst#response>`__

.. code-block:: javascript

    POST /servers/{server_id}/actions

Reboot the specified server.

This operation performs a soft or hard reboot of the specified server. A soft reboot is a graceful shutdown and restart of your server's operating system. A hard reboot power cycles your server, which performs an immediate shutdown and restart.

Specify the target server ID in the URI.

In the request body, specify the action ``reboot``, optionally followed by the ``type`` attribute, either ``HARD`` or ``SOFT``.

If you do not include the type attribute, a soft reboot is performed by default.



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
|reboot                    |object *(Required)*      |Specification of the     |
|                          |                         |reboot action for the    |
|                          |                         |specified server.        |
+--------------------------+-------------------------+-------------------------+
|type                      |object *(Required)*      |The type of reboot.      |
|                          |                         |Valid reboot types are:  |
|                          |                         |SOFTThe operating system |
|                          |                         |is signaled to restart,  |
|                          |                         |which allows for a       |
|                          |                         |graceful shutdown and    |
|                          |                         |restart of all           |
|                          |                         |processes. HARDPower     |
|                          |                         |cycles your server,      |
|                          |                         |which performs an        |
|                          |                         |immediate shutdown and   |
|                          |                         |restart.                 |
+--------------------------+-------------------------+-------------------------+





**Example Reboot Specified Server: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^





**Example Reboot Specified Server: JSON request**


.. code::

    Status Code: 202 No ContentContent-Length: 0Content-Type: application/jsonDate: Thu, 04 Dec 2014 21:45:47 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)x-compute-request-id

