=============================================================================
Delete Image -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Delete Image
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <DELETE_delete_image_images_image_id_.rst#request>`__
`Response <DELETE_delete_image_images_image_id_.rst#response>`__

.. code-block:: javascript

    DELETE /images/{image_id}

Deletes the specified image.

This operation deletes the specified image from the system. Images are immediately removed.

Specify the image ID in the URI.



This table shows the possible response codes for this operation:


+--------------------------+-------------------------+-------------------------+
|Response Code             |Name                     |Description              |
+==========================+=========================+=========================+
|204                       |Delete Successful        |Delete request succeeded.|
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








**Example Delete Image: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^





**Example Delete Image: JSON request**


.. code::

    Status Code: 204 No ContentContent-Type: text/html; charset=UTF-8Date: Thu, 09 Jul 2015 18:52:29 GMT, Thu, 09 Jul 2015 18:52:30 GMTServer: Jetty(9.2.z-SNAPSHOT)Via: 1.1 Repose (Repose/6.2.1.2)X-Compute-Request-Id: req-e1b75723-1027-48c0-aeea-008a9b038370

