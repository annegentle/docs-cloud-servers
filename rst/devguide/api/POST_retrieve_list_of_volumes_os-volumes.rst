=============================================================================
Retrieve List Of Volumes -  Rackspace Cloud Servers Developer Guide - API v2.0
=============================================================================

Retrieve List Of Volumes
~~~~~~~~~~~~~~~~~~~~~~~~~

`Request <POST_retrieve_list_of_volumes_os-volumes.rst#request>`__
`Response <POST_retrieve_list_of_volumes_os-volumes.rst#response>`__

.. code-block:: javascript

    POST /os-volumes

Retrieve list of volumes for your account.

Retrieves the list of volumes for your account.



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









**Example Retrieve List Of Volumes: JSON request**


.. code::

    X-Auth-Token: f064c46a782c444cb4ba4b6434288f7cContent-Type: application/jsonAccept: application/json


Response
^^^^^^^^^^^^^^^^^^


This table shows the body parameters for the response:

+--------------------------+-------------------------+-------------------------+
|Name                      |Type                     |Description              |
+==========================+=========================+=========================+
|volumes                   |object                   |An array of volumes.     |
+--------------------------+-------------------------+-------------------------+
|status                    |csapi:string             |The stae of the volume.  |
|                          |                         |This will be             |
|                          |                         |``available`` when       |
|                          |                         |volume is created and    |
|                          |                         |ready for use.           |
+--------------------------+-------------------------+-------------------------+
|display_name              |csapi:string             |The name assigned to the |
|                          |                         |volume.                  |
+--------------------------+-------------------------+-------------------------+
|attachments               |array                    |An array of volume       |
|                          |                         |attachments.             |
+--------------------------+-------------------------+-------------------------+
|availabity_zone           |csapi:string             |This parameter is no     |
|                          |                         |longer used and is       |
|                          |                         |always set to ``nova``.  |
+--------------------------+-------------------------+-------------------------+
|created_at                |csapi:date               |The date and time of     |
|                          |                         |volume creation.         |
+--------------------------+-------------------------+-------------------------+
|display_description       |csapi:string             |The description for the  |
|                          |                         |volume.                  |
+--------------------------+-------------------------+-------------------------+
|image_id                  |csapi:string             |The image_id use for the |
|                          |                         |volume. If no image was  |
|                          |                         |specified, this will be  |
|                          |                         |``null``.                |
+--------------------------+-------------------------+-------------------------+
|volume_type               |csapi:string             |The type of volume,      |
|                          |                         |either ``SATA`` or       |
|                          |                         |``SSD``. Alternaltely,   |
|                          |                         |you can use the UUID     |
|                          |                         |volume id for the volume |
|                          |                         |instead of the name. The |
|                          |                         |default is ``SATA``.     |
+--------------------------+-------------------------+-------------------------+
|snapshot_id               |UUID                     |The snapshot from which  |
|                          |                         |to create a volume, if   |
|                          |                         |any.                     |
+--------------------------+-------------------------+-------------------------+
|metadata                  |csapi:string             |Any metadata for the     |
|                          |                         |volume.                  |
+--------------------------+-------------------------+-------------------------+
|id                        |csapi:string             |The volume id.           |
+--------------------------+-------------------------+-------------------------+
|size                      |csapi:integer            |The size of the volume   |
|                          |                         |in gibibytes (GiB). The  |
|                          |                         |valid range for ``SATA`` |
|                          |                         |is 75-1024. The valid    |
|                          |                         |range for ``SSD`` is 50- |
|                          |                         |1024.                    |
+--------------------------+-------------------------+-------------------------+





**Example Retrieve List Of Volumes: JSON request**


.. code::

    Status Code: 200 OKConnection: keep-aliveContent-Length: 435Content-Type: application/jsonDate: Wed, 10 Jun 2015 16:48:59 GMTX-Compute-Request-Id: req-292d0b03-6a35-4397-ac14-86081a7136c9

