=============================================================================
Import A Server Key Pair -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Import A Server Key Pair
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <POST_import_a_server_key_pair_os-keypairs.rst#request>`__
`Response <POST_import_a_server_key_pair_os-keypairs.rst#response>`__

.. code-block:: javascript

    POST /os-keypairs

Import a server key pair

Imports, or uploads, a key pair, with the name and public key specified in the request body, to associate with a new server instance.



This table shows the possible response codes for this operation:


+--------------------------+-------------------------+-------------------------+
|Response Code             |Name                     |Description              |
+==========================+=========================+=========================+
|200                       |Success                  |Request accepted.        |
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






This table shows the body parameters for the request:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|keypair                   |object *(Required)*      |The container for the    |
|                          |                         |key pair request.        |
+--------------------------+-------------------------+-------------------------+
|name                      |string *(Required)*      |The name to associate    |
|                          |                         |with the key pair.       |
+--------------------------+-------------------------+-------------------------+
|public_key                |string *(Required)*      |The public ssh key value.|
+--------------------------+-------------------------+-------------------------+





**Example Import A Server Key Pair: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|keypair                   |object *(Required)*      |The container for the    |
|                          |                         |key pair details.        |
+--------------------------+-------------------------+-------------------------+
|fingerprint               |string *(Required)*      |A short sequence of      |
|                          |                         |bytes used to            |
|                          |                         |authenticate, or look    |
|                          |                         |up, a longer public key. |
+--------------------------+-------------------------+-------------------------+
|name                      |string *(Required)*      |The name of the key pair.|
+--------------------------+-------------------------+-------------------------+
|private_key               |string *(Required)*      |The private ssh key      |
|                          |                         |value.                   |
+--------------------------+-------------------------+-------------------------+
|public_key                |string *(Required)*      |The public ssh key value.|
+--------------------------+-------------------------+-------------------------+
|user_id                   |string *(Required)*      |The ID of the user.      |
+--------------------------+-------------------------+-------------------------+





**Example Import A Server Key Pair: JSON request**


.. code::

    Status Code: 200 OKContent-Length: 545Content-Type: application/jsonDate: Thu, 02 Apr 2015 18:08:19 GMT, Thu, 02 Apr 2015 18:08:19 GMTServer: Jetty(9.2.z-SNAPSHOT)Via: 1.1 Repose (Repose/6.2.1.2)X-Compute-Request-Id: req-9efa9191-4f08-4d65-92c7-acd934e5c5b0

