=============================================================================
Retrieve List Of Rate And Absolute Limits -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Retrieve List Of Rate And Absolute Limits
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <GET_retrieve_list_of_rate_and_absolute_limits_limits.rst#request>`__
`Response <GET_retrieve_list_of_rate_and_absolute_limits_limits.rst#response>`__

.. code-block:: javascript

    GET /limits

Retrieves the current rate limits and absolute limits for your account.

Applications can programmatically determine current account limits by using this API operation.



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









**Example Retrieve List Of Rate And Absolute Limits: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|limits                    |object                   |The container of limits  |
|                          |                         |attributes.              |
+--------------------------+-------------------------+-------------------------+
|absolute                  |object                   |The container of         |
|                          |                         |absolute limits          |
|                          |                         |attributes.              |
+--------------------------+-------------------------+-------------------------+
|maxTotalSnapshots         |xsd:int                  |The maximum number of    |
|                          |                         |snapshots.               |
+--------------------------+-------------------------+-------------------------+
|totalSnapshotsUsed        |xsd:int                  |The total number of      |
|                          |                         |snapshots used.          |
+--------------------------+-------------------------+-------------------------+
|maxTotalVolumeGigabytes   |xsd:int                  |The maximum total size   |
|                          |                         |of volumes, in gibibytes |
|                          |                         |(GiB).                   |
+--------------------------+-------------------------+-------------------------+
|totalGigabytesUsed        |xsd:int                  |The total number of      |
|                          |                         |gibibytes (GiB) used.    |
+--------------------------+-------------------------+-------------------------+
|maxTotalVolumes           |xsd:int                  |The maximum number of    |
|                          |                         |volumes.                 |
+--------------------------+-------------------------+-------------------------+
|totalVolumessUsed         |xsd:int                  |The total number of      |
|                          |                         |volumes used.            |
+--------------------------+-------------------------+-------------------------+
|rate                      |array                    |The array of rate        |
|                          |                         |objects.                 |
+--------------------------+-------------------------+-------------------------+
|limit                     |array                    |The array of rate limit  |
|                          |                         |objects.                 |
+--------------------------+-------------------------+-------------------------+
|next-available            |date                     |The next available rate  |
|                          |                         |limit date and time.     |
+--------------------------+-------------------------+-------------------------+
|remaining                 |date                     |The time remaining for   |
|                          |                         |the rate limit in units. |
+--------------------------+-------------------------+-------------------------+
|unit                      |date                     |The type of unit for the |
|                          |                         |rate limit. For example, |
|                          |                         |``DAY`` or ``MINUTE``.   |
+--------------------------+-------------------------+-------------------------+





**Example Retrieve List Of Rate And Absolute Limits: JSON request**


.. code::

    Status Code: 200 OKContent-Length: 3010Content-Type: application/jsonDate: Wed, 18 Mar 2015 20:23:18 GMT, Wed, 18 Mar 2015 20:23:19 GMTServer: Jetty(9.2.z-SNAPSHOT)Via: 1.1 Repose (Repose/6.2.1.2)X-Compute-Request-Id: req-48d05db0-dd97-4aef-87f2-11177ab8c262

