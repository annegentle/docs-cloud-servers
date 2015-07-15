=============================================================================
Retrieve Flavor Details -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Retrieve Flavor Details
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <GET_retrieve_flavor_details_flavors.rst#request>`__
`Response <GET_retrieve_flavor_details_flavors.rst#response>`__

.. code-block:: javascript

    GET /flavors

Retrieves details of the specified flavor.

Specify the flavor ID as id in the URI.

This operation returns details of the specified flavor in the response body.



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









**Example Retrieve Flavor Details: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^





**Example Retrieve Flavor Details: JSON request**


.. code::

    {"flavor": {"OS-FLV-EXT-DATA:ephemeral": 0,"OS-FLV-WITH-EXT-SPECS:extra_specs": {"class": "compute1","disk_io_index": "-1","number_of_data_disks": "0","policy_class": "compute_flavor"},"disk": 0,"id": "compute1-15","links": [{"href": "https://dfw.servers.api.rackspacecloud.com/v2/820712/flavors/compute1-15","rel": "self"},{"href": "https://dfw.servers.api.rackspacecloud.com/820712/flavors/compute1-15","rel": "bookmark"}],"name": "15 GB Compute v1","ram": 15360,"rxtx_factor": 1250.0,"swap": "","vcpus": 8}}

