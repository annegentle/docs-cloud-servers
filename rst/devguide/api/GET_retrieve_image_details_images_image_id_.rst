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

Specify the image ID in the URI.

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


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|image                     |object                   |The container of image   |
|                          |                         |details.                 |
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
|server                    |object                   |The container of server  |
|                          |                         |attributes for the image.|
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





**Example Retrieve Image Details: JSON request**


.. code::

    Status Code: 200 OKContent-Length: 2230Content-Type: application/jsonDate: Thu, 09 Jul 2015 18:24:01 GMT, Thu, 09 Jul 2015 18:24:02 GMTServer: Jetty(9.2.z-SNAPSHOT)Via: 1.1 Repose (Repose/6.2.1.2)X-Compute-Request-Id: req-5ba3fae8-5daf-48c7-9be1-6de842e50ca9

