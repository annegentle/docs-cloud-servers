=============================================================================
Retrieve List Of Images -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Retrieve List Of Images
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <GET_retrieve_list_of_images_images.rst#request>`__
`Response <GET_retrieve_list_of_images_images.rst#response>`__

.. code-block:: javascript

    GET /images

Retrieves IDs, names, and links for all available images.

This operation lists all images visible by the account.

The optional minDisk and minRam attributes set the minimum disk and RAM required to create a server with the image.

The image_type field in the response indicates whether the image is built-in ``(base)`` or custom ``(snapshot)``.



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




This table shows the query parameters for the request:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|server                    |object *(Required)*      |Filters the list of      |
|                          |                         |images by server.        |
|                          |                         |Specify the server       |
|                          |                         |reference by ID or by    |
|                          |                         |full URL.                |
+--------------------------+-------------------------+-------------------------+
|name                      |string *(Required)*      |Filters the list of      |
|                          |                         |images by image name.    |
+--------------------------+-------------------------+-------------------------+
|status                    |csapi:ImageStatus        |Filters the list of      |
|                          |*(Required)*             |images by status. In-    |
|                          |                         |flight images have a     |
|                          |                         |status of SAVING and the |
|                          |                         |conditional progress     |
|                          |                         |element contains a value |
|                          |                         |from 0 to 100, which     |
|                          |                         |indicates the percentage |
|                          |                         |completion. Other        |
|                          |                         |possible values for the  |
|                          |                         |status attribute include |
|                          |                         |ACTIVE, DELETED, ERROR,  |
|                          |                         |SAVING, and UNKNOWN.     |
|                          |                         |Images with an ACTIVE    |
|                          |                         |status are available for |
|                          |                         |use.                     |
+--------------------------+-------------------------+-------------------------+
|changes-since             |xsd:dateTime *(Required)*|Filters the list of      |
|                          |                         |images to those that     |
|                          |                         |have changed since the   |
|                          |                         |changes-since time.      |
+--------------------------+-------------------------+-------------------------+
|marker                    |csapi:UUID *(Required)*  |The ID of the last item  |
|                          |                         |in the previous list.    |
+--------------------------+-------------------------+-------------------------+
|limit                     |xsd:int *(Required)*     |Sets the page size.      |
+--------------------------+-------------------------+-------------------------+
|type                      |object *(Required)*      |Filters base Rackspace   |
|                          |                         |images or any custom     |
|                          |                         |server images that you   |
|                          |                         |have created.            |
+--------------------------+-------------------------+-------------------------+







**Example Retrieve List Of Images: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^





**Example Retrieve List Of Images: JSON request**


.. code::

    {"images":[{"status": "ACTIVE","updated": "2014-03-26T14:05:59Z","links":[{"href": "https://dfw.servers.api.rackspacecloud.com/v2/661145/images/6110edfe-8589-4bb1-aa27-385f12242627","rel": "self"},{"href": "https://dfw.servers.api.rackspacecloud.com/661145/images/6110edfe-8589-4bb1-aa27-385f12242627","rel": "bookmark"},{"href": "https://dfw.servers.api.rackspacecloud.com/661145/images/6110edfe-8589-4bb1-aa27-385f12242627","type": "application/vnd.openstack.image","rel": "alternate"}],"OS-DCF:diskConfig": "MANUAL","id": "6110edfe-8589-4bb1-aa27-385f12242627","OS-EXT-IMG-SIZE:size": 689810519,"name": "Ubuntu 13.10 (Saucy Salamander) (PVHVM)","created": "2014-03-25T17:00:15Z","minDisk": 20,"progress": 100,"minRam": 512,"metadata":{"vm_mode": "hvm","os_distro": "ubuntu","com.rackspace__1__visible_core": "1","com.rackspace__1__release_id": "1006","com.rackspace__1__options": "0","image_type": "base","cache_in_nova": "True","com.rackspace__1__source": "kickstart","org.openstack__1__os_distro": "com.ubuntu","com.rackspace__1__release_build_date": "2014-03-25_11-38-40","os_type": "linux","auto_disk_config": "disabled","com.rackspace__1__release_version": "3","com.rackspace__1__platform_target": "PublicCloud","com.rackspace__1__visible_rackconnect": "1","com.rackspace__1__build_rackconnect": "1","com.rackspace__1__visible_managed": "1","com.rackspace__1__build_core": "1","org.openstack__1__os_version": "13.10","org.openstack__1__architecture": "x64","com.rackspace__1__build_managed": "1"}}]}

