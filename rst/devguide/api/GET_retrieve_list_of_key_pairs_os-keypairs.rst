=============================================================================
Retrieve List Of Key Pairs -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Retrieve List Of Key Pairs
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <GET_retrieve_list_of_key_pairs_os-keypairs.rst#request>`__
`Response <GET_retrieve_list_of_key_pairs_os-keypairs.rst#response>`__

.. code-block:: javascript

    GET /os-keypairs

Retrieves the current rate limits and absolute limits for your account.

This operation retrieves a list of server key pairs.



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









Response
^^^^^^^^^^^^^^^^^^


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|keypairs                  |array *(Required)*       |An array of key pairs.   |
+--------------------------+-------------------------+-------------------------+
|keypairs                  |object *(Required)*      |A container of key pair  |
|                          |                         |details.                 |
+--------------------------+-------------------------+-------------------------+
|fingerprint               |string *(Required)*      |A short sequence of      |
|                          |                         |bytes used to            |
|                          |                         |authenticate, or look    |
|                          |                         |up, a longer public key. |
+--------------------------+-------------------------+-------------------------+
|name                      |string *(Required)*      |The name of the key pair.|
+--------------------------+-------------------------+-------------------------+
|public_key                |string *(Required)*      |The public ssh key value.|
+--------------------------+-------------------------+-------------------------+





**Example Retrieve List Of Key Pairs: JSON request**


.. code::

    Status Code: 200 OKContent-Length: 540Content-Type: application/jsonDate: Thu, 02 Apr 2015 18:09:36 GMT, Thu, 02 Apr 2015 18:09:36 GMTServer: Jetty(9.2.z-SNAPSHOT)Via: 1.1 Repose (Repose/6.2.1.2)X-Compute-Request-Id: req-5a9c3b9d-67cf-4b7f-b31d-0670e1c667a0

