=============================================================================
Delete Volume -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Delete Volume
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <POST_delete_volume_os-volumes_id_.rst#request>`__
`Response <POST_delete_volume_os-volumes_id_.rst#response>`__

.. code-block:: javascript

    POST /os-volumes/{id}

Delete volume.

Delete volume.

In the URI, specify the volume ID.



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
|{volume_id}               |csapi:UUID               |The UUID for the volume. |
+--------------------------+-------------------------+-------------------------+








**Example Delete Volume: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^





**Example Delete Volume: JSON request**


.. code::

    Status Code: 202 AcceptedConnection: keep-aliveContent-Length: 0Content-Type: text/html; charset=UTF-8Date: Wed, 10 Jun 2015 17:13:20 GMT

