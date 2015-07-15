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
|minDisk                   |xsd:int *(Required)*     |Filters the list of      |
|                          |                         |flavors to those with    |
|                          |                         |the specified minimum    |
|                          |                         |number of gigabytes of   |
|                          |                         |disk storage.            |
+--------------------------+-------------------------+-------------------------+
|minRam                    |xsd:int *(Required)*     |Filters the list of      |
|                          |                         |flavors to those with    |
|                          |                         |the specified minimum    |
|                          |                         |amount of RAM in         |
|                          |                         |megabytes.               |
+--------------------------+-------------------------+-------------------------+
|marker                    |xsd:string *(Required)*  |The ID of the last item  |
|                          |                         |in the previous list.    |
+--------------------------+-------------------------+-------------------------+
|limit                     |xsd:int *(Required)*     |Sets the page size.      |
+--------------------------+-------------------------+-------------------------+







**Example Retrieve Of List Flavors: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|flavors                   |array                    |The array of flavors.    |
+--------------------------+-------------------------+-------------------------+
|id                        |xsd:string               |The flavor ID.           |
+--------------------------+-------------------------+-------------------------+
|links                     |xsd:string               |The array of flavor      |
|                          |                         |links for self and       |
|                          |                         |bookmark.                |
+--------------------------+-------------------------+-------------------------+
|href                      |csapi:UUID               |The URL for the flavor   |
|                          |                         |and the associated       |
|                          |                         |``rel``.                 |
+--------------------------+-------------------------+-------------------------+
|rel                       |csapi:UUID               |The descriptive field    |
|                          |                         |for the associated       |
|                          |                         |``href``, which is       |
|                          |                         |either ``self`` or       |
|                          |                         |``bookmark``.            |
+--------------------------+-------------------------+-------------------------+
|name                      |xsd:string               |The flavor name.         |
+--------------------------+-------------------------+-------------------------+





**Example Retrieve Of List Flavors: JSON request**


.. code::

    Status Code: 200 OKContent-Length: 9132Content-Type: application/jsonDate: Wed, 08 Jul 2015 21:33:49 GMT, Wed, 08 Jul 2015 21:33:49 GMTServer: Jetty(9.2.z-SNAPSHOT)Via: 1.1 Repose (Repose/6.2.1.2)X-Compute-Request-Id: req-dbb15502-9620-450b-a05e-63e291595a89

