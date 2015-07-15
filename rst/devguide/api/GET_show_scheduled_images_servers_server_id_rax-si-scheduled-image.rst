=============================================================================
Show Scheduled Images -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Show Scheduled Images
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <GET_show_scheduled_images_servers_server_id_rax-si-scheduled-image.rst#request>`__
`Response <GET_show_scheduled_images_servers_server_id_rax-si-scheduled-image.rst#response>`__

.. code-block:: javascript

    GET /servers/{server_id}/rax-si-scheduled-image

Show scheduled images for the specified server.

This operation returns the retention value if the server has scheduled images enabled. For weekly images, the response also includes the scheduled day of the week for the image. If the server has scheduled images disabled, an HTTP 404 is returned.

In the URI, specify the server ID.



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
|{server_id}               |csapi:UUID               |The UUID for the server. |
+--------------------------+-------------------------+-------------------------+








**Example Show Scheduled Images: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|image_schedule            |object *(Required)*      |The container for the    |
|                          |                         |image schedule.          |
+--------------------------+-------------------------+-------------------------+
|retention                 |int *(Required)*         |The number of days that  |
|                          |                         |an Image should be       |
|                          |                         |retained.                |
+--------------------------+-------------------------+-------------------------+
|day_of_week               |string *(Required)*      |The chosen day of the    |
|                          |                         |week for the image       |
|                          |                         |creation. The allowed    |
|                          |                         |values for this field    |
|                          |                         |are: ``SUNDAY``,         |
|                          |                         |``MONDAY``, ``TUESDAY``, |
|                          |                         |``WEDNESDAY``,           |
|                          |                         |``THURSDAY``,            |
|                          |                         |``FRIDAY``, and          |
|                          |                         |``SATURDAY``.            |
+--------------------------+-------------------------+-------------------------+





**Example Show scheduled images (daily - success): JSON response**


.. code::

    Status Code: 200 OKContent-Length: 36Content-Type: application/jsonDate: Thu, 29 Jan 2015 22:53:45 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)x-compute-request-id: req-5d33237d-0f96-4d13-a057-5ab2b1b46f71


**Example Show scheduled images (weekly - success): JSON response**


.. code::

    Status Code: 200 OKContent-Length: 63Content-Type: application/jsonDate: Thu, 29 Jan 2015 18:25:01 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)x-compute-request-id: req-f90ae0d1-e0d8-407b-9af0-f4ed79935991


**Example Show scheduled images (not found): JSON response**


.. code::

    Status Code: 404 Not FoundContent-Length: 123Content-Type: application/json; charset=UTF-8Date: Thu, 29 Jan 2015 22:24:11 GMTServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)x-compute-request-id: req-e20a9646-e225-403b-9e81-53c22728cbaf

