=============================================================================
Disable Scheduled Images -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Disable Scheduled Images
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <DELETE_disable_scheduled_images_servers_server_id_rax-si-scheduled-image.rst#request>`__
`Response <DELETE_disable_scheduled_images_servers_server_id_rax-si-scheduled-image.rst#response>`__

.. code-block:: javascript

    DELETE /servers/{server_id}/rax-si-scheduled-image

Disable scheduled images for the specified server.

This operation disables scheduled images by deleting the image_schedule resource that indicates the scheduled image service should create snapshots of this server. Thus scheduled images will no longer be created.



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
|{server_id}               |csapi:UUID               |The UUID for the server. |
+--------------------------+-------------------------+-------------------------+








**Example Disable Scheduled Images: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^





**Example Disable Scheduled Images: JSON request**


.. code::

    Status Code: 202 AcceptedContent-Length: 0Content-Type: text/html;charset=UTF-8Date: Thu, 29 Jan 2015 18:51:38 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)x-compute-request-id: req-2e8174d0-414d-4609-863c-f538ca1cae83

