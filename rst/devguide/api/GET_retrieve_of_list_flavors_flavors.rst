=============================================================================
Retrieve Of List Flavors -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Retrieve Of List Flavors
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <GET_retrieve_of_list_flavors_flavors.rst#request>`__
`Response <GET_retrieve_of_list_flavors_flavors.rst#response>`__

.. code-block:: javascript

    GET /flavors

Retrieves IDs, names, and links for all available flavors.

This operation lists information for all available flavors.

To filter the list of flavors returned in the response body, you can specify the following optional URI parameters:

``minDisk=minDiskInGB``

Filters the list of flavors to those with the specified minimum number of gigabytes of disk storage.

``minRam=minRamInMB``

Filters the list of flavors to those with the specified minimum amount of RAM in megabytes.

``marker=markerID``

``limit=int``

Sets the page size. See `Section 1.3, Paginated Collections" <None>`__ / >



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









**Example Retrieve Of List Flavors: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^





**Example Retrieve Of List Flavors: JSON request**


.. code::

    {"flavors": [{"id": "2","links": [{"href": "https://dfw.servers.api.rackspacecloud.com/v2/453265/flavors/2","rel": "self"},{"href": "https://dfw.servers.api.rackspacecloud.com/453265/flavors/2","rel": "bookmark"}],"name": "512MB Standard Instance"},{"id": "3","links": [{"href": "https://dfw.servers.api.rackspacecloud.com/v2/453265/flavors/3","rel": "self"},{"href": "https://dfw.servers.api.rackspacecloud.com/453265/flavors/3","rel": "bookmark"}],"name": "1GB Standard Instance"},{"id": "4","links": [{"href": "https://dfw.servers.api.rackspacecloud.com/v2/453265/flavors/4","rel": "self"},{"href": "https://dfw.servers.api.rackspacecloud.com/453265/flavors/4","rel": "bookmark"}],"name": "2GB Standard Instance"},{"id": "5","links": [{"href": "https://dfw.servers.api.rackspacecloud.com/v2/453265/flavors/5","rel": "self"},{"href": "https://dfw.servers.api.rackspacecloud.com/453265/flavors/5","rel": "bookmark"}],"name": "4GB Standard Instance"},{"id": "6","links": [{"href": "https://dfw.servers.api.rackspacecloud.com/v2/453265/flavors/6","rel": "self"},{"href": "https://dfw.servers.api.rackspacecloud.com/453265/flavors/6","rel": "bookmark"}],"name": "8GB Standard Instance"},{"id": "7","links": [{"href": "https://dfw.servers.api.rackspacecloud.com/v2/453265/flavors/7","rel": "self"},{"href": "https://dfw.servers.api.rackspacecloud.com/453265/flavors/7","rel": "bookmark"}],"name": "15GB Standard Instance"},{"id": "8","links": [{"href": "https://dfw.servers.api.rackspacecloud.com/v2/453265/flavors/8","rel": "self"},{"href": "https://dfw.servers.api.rackspacecloud.com/453265/flavors/8","rel": "bookmark"}],"name": "30GB Standard Instance"}]}

