=============================================================================
Show Flavor Extra Specs -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Show Flavor Extra Specs
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <GET_show_flavor_extra_specs_flavors_flavor_id_.rst#request>`__
`Response <GET_show_flavor_extra_specs_flavors_flavor_id_.rst#response>`__

.. code-block:: javascript

    GET /flavors/{flavor_id}

Retrieve the extra specs for a specified flavor.

This operation shows extra specifications for the flavor, such as identifying the policy class.

In the URI, specify the flavor ID.



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

This table shows the URI parameters for the request:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|{flavor_id}               |string                   |The flavor id.           |
+--------------------------+-------------------------+-------------------------+








**Example Show Flavor Extra Specs: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|extra_specs               |object *(Required)*      |The container for flavor |
|                          |                         |extra specification      |
|                          |                         |details.                 |
+--------------------------+-------------------------+-------------------------+
|policy_class              |string *(Required)*      |The policy class for the |
|                          |                         |flavor.                  |
+--------------------------+-------------------------+-------------------------+
|class                     |string *(Required)*      |The class for the flavor.|
+--------------------------+-------------------------+-------------------------+
|keyname                   |xsd:int *(Required)*     |Depending on the         |
|                          |                         |specified flavor, there  |
|                          |                         |may be other             |
|                          |                         |specifications shown     |
|                          |                         |using format of          |
|                          |                         |"keyname" : "keyvalue".  |
|                          |                         |These might include      |
|                          |                         |information like the     |
|                          |                         |number of data disks or  |
|                          |                         |the disk_io index.       |
+--------------------------+-------------------------+-------------------------+





**Example Show Flavor Extra Specs: JSON request**


.. code::

    Status Code: 200 OKContent-Length: 124Content-Type: application/jsonDate: Tue, 27 Jan 2015 13:46:52 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)x-compute-request-id: req-7c63f55b-9b16-49d2-854c-dfecfc362116

