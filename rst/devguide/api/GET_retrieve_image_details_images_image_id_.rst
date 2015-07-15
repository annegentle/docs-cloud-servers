=============================================================================
Retrieve Image Details -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Retrieve Image Details
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <GET_retrieve_image_details_images_image_id_.rst#request>`__
`Response <GET_retrieve_image_details_images_image_id_.rst#response>`__

.. code-block:: javascript

    GET /images/{image_id}

Retrieves details of a specified image.

Specify the image ID as id in the URI.

This operation returns details of the specified image in the response body. The image_type field in the response indicates whether the image is built-in ``(base)`` or custom ``(snapshot)``.

The response body does not include the serverId field. To retrieve the serverId field, get details for all images.



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
|{image_id}                |csapi:UUID               |The UUID for the image.  |
+--------------------------+-------------------------+-------------------------+








**Example Retrieve Image Details: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^





**Example Retrieve Image Details: JSON request**


.. code::

    {"image": {"OS-DCF:diskConfig": "AUTO","created": "2012-02-28T19:38:57Z","id": "3afe97b2-26dc-49c5-a2cc-a2fc8d80c001","links": [{"href": "https://dfw.servers.api.rackspacecloud.com/v2/010101/images/3afe97b2-26dc-49c5-a2cc-a2fc8d80c001","rel": "self"},{"href": "https://dfw.servers.api.rackspacecloud.com/010101/images/3afe97b2-26dc-49c5-a2cc-a2fc8d80c001","rel": "bookmark"},{"href": "https://dfw.servers.api.rackspacecloud.com/010101/images/3afe97b2-26dc-49c5-a2cc-a2fc8d80c001","rel": "alternate","type": "application/vnd.openstack.image"}],"metadata": {"arch": "x86-64","auto_disk_config": "True","com.rackspace__1__build_core": "1","com.rackspace__1__build_managed": "0","com.rackspace__1__build_rackconnect": "0","com.rackspace__1__options": "0","com.rackspace__1__visible_core": "1","com.rackspace__1__visible_managed": "0","com.rackspace__1__visible_rackconnect": "0","image_type": "base","org.openstack__1__architecture": "x64","org.openstack__1__os_distro": "org.ubuntu","org.openstack__1__os_version": "11.10","os_distro": "ubuntu","os_type": "linux","os_version": "11.10","rax_managed": "false","rax_options": "0"},"minDisk": 10,"minRam": 256,"name": "Ubuntu 11.10","progress": 100,"status": "ACTIVE","updated": "2012-02-28T19:39:05Z"}}

