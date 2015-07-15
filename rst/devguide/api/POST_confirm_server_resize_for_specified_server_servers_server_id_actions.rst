=============================================================================
Confirm Server Resize For Specified Server -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Confirm Server Resize For Specified Server
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <POST_confirm_server_resize_for_specified_server_servers_server_id_actions.rst#request>`__
`Response <POST_confirm_server_resize_for_specified_server_servers_server_id_actions.rst#response>`__

.. code-block:: javascript

    POST /servers/{server_id}/actions

Confirm the server resize for the specified server.

During a resize operation, the original server is saved for a period of time to allow roll back if a problem occurs. After you verify that the newly resized server works properly, use this operation to confirm the resize. After you confirm the resize, the original server is removed, and you cannot roll back to that server. All resizes are automatically confirmed after 24 hours, if you do not explicitly confirm, or revert, the resize.

This operation is not available for OnMetal servers.

Specify the target server ID in the URI.

In the request body, specify the ``confirmResize`` action.



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
|confirmResize             |object *(Required)*      |Specification of the     |
|                          |                         |confirmResize action for |
|                          |                         |the specified server.    |
+--------------------------+-------------------------+-------------------------+





**Example Confirm Server Resize For Specified Server: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^





**Example Confirm Server Resize For Specified Server: JSON request**


.. code::

    Status Code: 202 No ContentContent-Length: 0Content-Type: application/jsonDate: Thu, 04 Dec 2014 21:45:47 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)x-compute-request-id

