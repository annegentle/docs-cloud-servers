=============================================================================
Delete Key Pair -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Delete Key Pair
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <DELETE_delete_key_pair_os-keypairs_keypair_name_.rst#request>`__
`Response <DELETE_delete_key_pair_os-keypairs_keypair_name_.rst#response>`__

.. code-block:: javascript

    DELETE /os-keypairs/{keypair_name}

Deletes the specified key pair.

This operation deletes the specified key pair. A return code of 202 indicates success.



This table shows the possible response codes for this operation:


+--------------------------+-------------------------+-------------------------+
|Response Code             |Name                     |Description              |
+==========================+=========================+=========================+
|202                       |Delete Successful        |Delete request succeeded.|
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
|{keypair_name}            |string                   |The name of the key pair |
|                          |                         |to be deleted.           |
+--------------------------+-------------------------+-------------------------+








**Example Delete Key Pair: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^





**Example Delete Key Pair: JSON request**


.. code::

    Status Code: 202 AcceptedContent-Length: 0Content-Type: text/html; charset=UTF-8Date: Thu, 02 Apr 2015 18:06:52 GMT, Thu, 02 Apr 2015 18:06:52 GMTServer: Jetty(9.2.z-SNAPSHOT)Via: 1.1 Repose (Repose/6.2.1.2)X-Compute-Request-Id: req-6b1bbebc-5b70-4775-9b1d-0e69db552b31

