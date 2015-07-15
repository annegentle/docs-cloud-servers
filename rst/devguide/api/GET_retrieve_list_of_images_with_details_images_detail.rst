=============================================================================
Retrieve List Of Images With Details -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Retrieve List Of Images With Details
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <GET_retrieve_list_of_images_with_details_images_detail.rst#request>`__
`Response <GET_retrieve_list_of_images_with_details_images_detail.rst#response>`__

.. code-block:: javascript

    GET /images/detail

Retrieves all details for all available images.

This operation returns details of all images in the response body.



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
|type                      |xsd:string *(Required)*  |Filters Rackspace base   |
|                          |                         |images or any custom     |
|                          |                         |server images that you   |
|                          |                         |have created.            |
+--------------------------+-------------------------+-------------------------+







**Example Retrieve List Of Images With Details: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|images                    |array                    |The array of images.     |
+--------------------------+-------------------------+-------------------------+
|status                    |xsd:string               |The image status, like   |
|                          |                         |``ACTIVE``.              |
+--------------------------+-------------------------+-------------------------+
|updated                   |xsd:date                 |The date and time that   |
|                          |                         |the image was last       |
|                          |                         |updated.                 |
+--------------------------+-------------------------+-------------------------+
|links                     |xsd:string               |The array of image links |
|                          |                         |for self and bookmark.   |
+--------------------------+-------------------------+-------------------------+
|href                      |csapi:UUID               |The URL for the image    |
|                          |                         |and the associated       |
|                          |                         |``rel``.                 |
+--------------------------+-------------------------+-------------------------+
|rel                       |csapi:UUID               |The descriptive field    |
|                          |                         |for the associated       |
|                          |                         |``href``, which is       |
|                          |                         |either ``self``,         |
|                          |                         |``bookmark``, or         |
|                          |                         |``alternate``.           |
+--------------------------+-------------------------+-------------------------+
|type                      |csapi:UUID               |The alternate image type.|
+--------------------------+-------------------------+-------------------------+
|OS-DCF:diskConfig         |xsd:string               |The disk configuration   |
|                          |                         |value. Valid values are  |
|                          |                         |``AUTO`` and ``MANUAL``. |
+--------------------------+-------------------------+-------------------------+
|id                        |csapi:UUID               |The image ID.            |
+--------------------------+-------------------------+-------------------------+
|updated                   |xsd:date                 |The date and time that   |
|                          |                         |the image was last       |
|                          |                         |updated.                 |
+--------------------------+-------------------------+-------------------------+
|OS-EXT-IMG-SIZE:size      |xsd:string               |The image size.          |
+--------------------------+-------------------------+-------------------------+
|name                      |xsd:string               |The image name.          |
+--------------------------+-------------------------+-------------------------+
|created                   |xsd:date                 |The date and time that   |
|                          |                         |the image was created.   |
+--------------------------+-------------------------+-------------------------+
|minDisk                   |xsd:int                  |The minimum number of    |
|                          |                         |gigabytes of disk        |
|                          |                         |storage.                 |
+--------------------------+-------------------------+-------------------------+
|progress                  |xsd:int                  |The completion           |
|                          |                         |percentage for an image. |
|                          |                         |``100`` indicates the    |
|                          |                         |image build is completed.|
+--------------------------+-------------------------+-------------------------+
|minRam                    |xsd:int                  |The specified minimum    |
|                          |                         |amount of RAM in         |
|                          |                         |megabytes.               |
+--------------------------+-------------------------+-------------------------+
|metadata                  |array                    |Array of metadata key    |
|                          |                         |pairs containing         |
|                          |                         |information about the    |
|                          |                         |image.                   |
+--------------------------+-------------------------+-------------------------+





**Example Retrieve List Of Images With Details: JSON request**


.. code::

    Status Code: 200 OKContent-Length: 91825Content-Type: application/jsonDate: Thu, 09 Jul 2015 16:16:03 GMT, Thu, 09 Jul 2015 16:16:06 GMTServer: Jetty(9.2.z-SNAPSHOT)Via: 1.1 Repose (Repose/6.2.1.2)X-Compute-Request-Id: req-5e110eed-c310-4e8a-806f-313865f189bd

