=============================================================================
Get Console -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Get Console
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <POST_get_console_servers_servers_action.rst#request>`__
`Response <POST_get_console_servers_servers_action.rst#response>`__

.. code-block:: javascript

    POST /servers/servers/action

Retrieve console output for a specified server.

This operation returns a URL which you use in a browser to open a console connection to your server.

In the URI, specify the server ID.



This table shows the possible response codes for this operation:

None

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
|os-getVNCConsole          |object *(Required)*      |A container for console  |
|                          |                         |request.                 |
+--------------------------+-------------------------+-------------------------+
|type                      |csapi:string *(Required)*|A key pair with the type |
|                          |                         |of vnc console,          |
|                          |                         |containing the value     |
|                          |                         |``"xvpvnc"``.            |
+--------------------------+-------------------------+-------------------------+





**Example Get Console: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^




