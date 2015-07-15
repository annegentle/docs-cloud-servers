=============================================================================
List Networks -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

List Networks
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <GET_list_networks_os-networksv2.rst#request>`__
`Response <GET_list_networks_os-networksv2.rst#response>`__

.. code-block:: javascript

    GET /os-networksv2

Lists the networks configured for the specified tenant ID.

This operation lists the networks configured for the tenant ID specified in the request URI.

To list the networks that are associated with servers, see `List Servers <http://docs.rackspace.com/servers/api/v2/cs-devguide/content/List_Servers-d1e2078.html>`__ in the Next Generation Cloud Servers Developer Guide.



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









Response
^^^^^^^^^^^^^^^^^^


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|networks                  |array                    |An array of networks.    |
+--------------------------+-------------------------+-------------------------+
|cidr                      |xsd:string               |The CIDR for an isolated |
|                          |                         |network. This parameter  |
|                          |                         |is not included for      |
|                          |                         |PublicNet and ServiceNet.|
+--------------------------+-------------------------+-------------------------+
|id                        |xsd:string               |The network ID.          |
+--------------------------+-------------------------+-------------------------+
|label                     |xsd:string               |The name of the network. |
|                          |                         |ServiceNet is labeled as |
|                          |                         |private, and PublicNet   |
|                          |                         |is labeled as public in  |
|                          |                         |the network list.        |
+--------------------------+-------------------------+-------------------------+





**Example List Networks: JSON request**


.. code::

    Status Code: 200 OKContent-Length: 474Content-Type: application/jsonDate: Mon, 13 Apr 2015 18:41:07 GMT, Mon, 13 Apr 2015 18:41:08 GMTServer: Jetty(9.2.z-SNAPSHOT)Via: 1.1 Repose (Repose/6.2.1.2)X-Compute-Request-Id: req-889f3f67-e02e-416c-9d91-9e3bb33e766d

