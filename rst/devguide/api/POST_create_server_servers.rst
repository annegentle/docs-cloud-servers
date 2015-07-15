=============================================================================
Create Server -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Create Server
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <POST_create_server_servers.rst#request>`__
`Response <POST_create_server_servers.rst#response>`__

.. code-block:: javascript

    POST /servers

Provisions a server asynchronously.

The full URL to the newly created server is returned through the ``Location`` header and is available as a ``self`` and ``bookmark`` link in the server representation.

The progress of the server build depends on factors including location of the requested image, network i/o, host load, and the selected flavor. You can check the progress of the build request by issuing a call to retrieve the details of the server. Once the build is complete, the server's ``status`` is ``ACTIVE``.

For OnMetal server builds, even after the ``status`` is ACTIVE, wait a few additional moments for the network configuration to complete. Once the new OnMetal server pings successfully, you can begin to use it.

OnMetal servers must be created using an ssh key pair. Thus you should ignore the administrator password returned by a Create Server operation because it does not allow access to the OnMetal server.

The following extensions allow you to use other options when creating a new server:

Config Drive

Boot from volume

Networks for nova and for neutron



This table shows the possible response codes for this operation:


+--------------------------+-------------------------+-------------------------+
|Response Code             |Name                     |Description              |
+==========================+=========================+=========================+
|202                       |Success                  |Request succeeded.       |
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






This table shows the body parameters for the request:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|name                      |csapi:string *(Required)*|The server name.         |
+--------------------------+-------------------------+-------------------------+
|imageRef                  |csapi:UUID *(Required)*  |The image reference for  |
|                          |                         |the desired image for    |
|                          |                         |your server instance.    |
+--------------------------+-------------------------+-------------------------+
|flavorRef                 |csapi:UUID *(Required)*  |The flavor reference for |
|                          |                         |the desired flavor for   |
|                          |                         |your server instance.    |
+--------------------------+-------------------------+-------------------------+
|config_drive              |csapi:string *(Required)*|Enables metadata         |
|                          |                         |injection in a server    |
|                          |                         |through a configuration  |
|                          |                         |drive. To enable a       |
|                          |                         |configuration drive,     |
|                          |                         |specify ``true``.        |
|                          |                         |Otherwise, specify       |
|                          |                         |``false``.               |
+--------------------------+-------------------------+-------------------------+
|key_name                  |csapi:string *(Required)*|The name of the key pair |
|                          |                         |used to authenticate by  |
|                          |                         |using key-based          |
|                          |                         |authentication instead   |
|                          |                         |of password-based        |
|                          |                         |authentication.          |
+--------------------------+-------------------------+-------------------------+
|OS-DCF:diskConfig         |csapi:string *(Required)*|The disk configuration   |
|                          |                         |value. Valid values are: |
|                          |                         |AUTO:The server is built |
|                          |                         |with a single partition  |
|                          |                         |which is the size of the |
|                          |                         |target flavor disk. The  |
|                          |                         |file system is           |
|                          |                         |automatically adjusted   |
|                          |                         |to fit the entire        |
|                          |                         |partition. This keeps    |
|                          |                         |things simple and        |
|                          |                         |automated. AUTO is valid |
|                          |                         |only for images and      |
|                          |                         |servers with a single    |
|                          |                         |partition that use the   |
|                          |                         |EXT3 file system. This   |
|                          |                         |is the default setting   |
|                          |                         |for applicable Rackspace |
|                          |                         |base images. MANUAL:The  |
|                          |                         |server is built using    |
|                          |                         |the partition scheme and |
|                          |                         |file system of the       |
|                          |                         |source image. If the     |
|                          |                         |target flavor disk is    |
|                          |                         |larger, the remaining    |
|                          |                         |disk space is left       |
|                          |                         |unpartitioned. This      |
|                          |                         |enables images to have   |
|                          |                         |non-EXT3 file systems,   |
|                          |                         |multiple partitions, and |
|                          |                         |so on, and it enables    |
|                          |                         |you to manage the disk   |
|                          |                         |configuration.           |
+--------------------------+-------------------------+-------------------------+
|metadata                  |csapi:string *(Required)*|Metadata key and value   |
|                          |                         |pairs. The maximum size  |
|                          |                         |of each metadata key and |
|                          |                         |value is 255 bytes each. |
+--------------------------+-------------------------+-------------------------+
|personality               |csapi:array *(Required)* |The array of personality |
|                          |                         |files for the server.    |
+--------------------------+-------------------------+-------------------------+
|path                      |csapi:string *(Required)*|The path of the          |
|                          |                         |personality file.        |
+--------------------------+-------------------------+-------------------------+
|contents                  |csapi:string *(Required)*|The contents od the      |
|                          |                         |personality file.        |
+--------------------------+-------------------------+-------------------------+
|networks                  |csapi:array *(Required)* |The array of networks    |
|                          |                         |attached to the server.  |
|                          |                         |By default, the server   |
|                          |                         |instance is provisioned  |
|                          |                         |with all isolated        |
|                          |                         |networks for the tenant. |
|                          |                         |You can specify multiple |
|                          |                         |NICs on the server.      |
|                          |                         |Optionally, you can      |
|                          |                         |create one or more NICs  |
|                          |                         |on the server. To        |
|                          |                         |provision the server     |
|                          |                         |instance with a NIC for  |
|                          |                         |a ``Nova-network``       |
|                          |                         |network, specify the     |
|                          |                         |UUID in the ``uuid``     |
|                          |                         |attribute in a           |
|                          |                         |``networks`` object. To  |
|                          |                         |provision the server     |
|                          |                         |instance with a NIC for  |
|                          |                         |a ``Neutron`` network,   |
|                          |                         |specify the UUID in the  |
|                          |                         |``port`` attribute in a  |
|                          |                         |``networks`` object.     |
+--------------------------+-------------------------+-------------------------+
|uuid                      |csapi:UUID *(Required)*  |The UUID of the ``Nova-  |
|                          |                         |network`` network        |
|                          |                         |attached to the server.  |
+--------------------------+-------------------------+-------------------------+
|port                      |csapi:UUID *(Required)*  |The UUID of the          |
|                          |                         |``Neutron`` port         |
|                          |                         |attached to the server.  |
+--------------------------+-------------------------+-------------------------+





**Example Create Server: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|server                    |csapi:object *(Required)*|The container for server |
|                          |                         |data.                    |
+--------------------------+-------------------------+-------------------------+
|id                        |csapi:UUID *(Required)*  |The ID of the server.    |
+--------------------------+-------------------------+-------------------------+
|links                     |csapi:UUID *(Required)*  |An array of the self and |
|                          |                         |bookmark links to the    |
|                          |                         |server.                  |
+--------------------------+-------------------------+-------------------------+
|href                      |csapi:UUID *(Required)*  |The URL for the server   |
|                          |                         |and the associated       |
|                          |                         |``rel``.                 |
+--------------------------+-------------------------+-------------------------+
|rel                       |csapi:UUID *(Required)*  |The descriptive field    |
|                          |                         |for the associated       |
|                          |                         |``href``, which is       |
|                          |                         |either ``self`` or       |
|                          |                         |``bookmark``.            |
+--------------------------+-------------------------+-------------------------+
|adminPass                 |csapi:string *(Required)*|The password assigned to |
|                          |                         |provide login access to  |
|                          |                         |the server.              |
+--------------------------+-------------------------+-------------------------+
|OS-DCF:diskConfig         |csapi:string *(Required)*|The disk configuration   |
|                          |                         |value. Valid values are  |
|                          |                         |``AUTO`` and ``MANUAL``. |
+--------------------------+-------------------------+-------------------------+





**Example Create Server: JSON request**


.. code::

    Status Code: 202 AcceptedContent-Length: 380Content-Type: application/jsonDate: Thu, 04 Dec 2014 18:47:30 GMTLocation: https://dfw.servers.api.rackspacecloud.com/v2/820712/servers/4b963871-f591-4b7d-b05f-7c0286e3c50fServer: Jetty(8.0.y.z-SNAPSHOT)Via: 1.1 Repose (Repose/2.12)x-compute-request-id: req-b8b54344-41a9-4d6a-a92f-60f3dcab4b1f

