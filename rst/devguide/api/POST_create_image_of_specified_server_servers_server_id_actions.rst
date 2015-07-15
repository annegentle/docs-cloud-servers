=============================================================================
Create Image Of Specified Server -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Create Image Of Specified Server
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <POST_create_image_of_specified_server_servers_server_id_actions.rst#request>`__
`Response <POST_create_image_of_specified_server_servers_server_id_actions.rst#response>`__

.. code-block:: javascript

    POST /servers/{server_id}/actions

Create an image of the specified server.

This operation creates a new image for a specified server. Once complete, you can use your new image to rebuild or create servers. The full URL to the newly created image is returned through the ``Location`` header. You can retrieve additional attributes for the image including its creation status by issuing a subsequent ``GET`` on that URL.

Image creation is an asynchronous operation, so coordinating the creation with data quiescence, and so on, is currently not possible.

This operation is not available for OnMetal servers.

In addition to creating images manually, you may also schedule images of your server automatically.

Specify the target server ID in the URI.

In the request body, specify the ``createImage`` action, followed by attributes.



This table shows the possible response codes for this operation:


+--------------------------+-------------------------+-------------------------+
|Response Code             |Name                     |Description              |
+==========================+=========================+=========================+
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
|createImage               |object *(Required)*      |Specification of the     |
|                          |                         |createImage action for   |
|                          |                         |the specified server.    |
+--------------------------+-------------------------+-------------------------+
|name                      |string *(Required)*      |The name of the new      |
|                          |                         |image.                   |
+--------------------------+-------------------------+-------------------------+
|metadata                  |object *(Required)*      |The container of the     |
|                          |                         |metadata for the new     |
|                          |                         |image.                   |
+--------------------------+-------------------------+-------------------------+
|meta                      |object *(Required)*      |A metadata keypair,      |
|                          |                         |specifying ImageType or  |
|                          |                         |ImageVersion, for        |
|                          |                         |example.                 |
+--------------------------+-------------------------+-------------------------+





**Example Create Image Of Specified Server: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^





**Example Create Image Of Specified Server: JSON request**


.. code::

    Status Code: 202 No ContentContent-Length: 0Content-Type: application/jsonDate: Thu, 04 Dec 2014 21:45:47 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)x-compute-request-id

