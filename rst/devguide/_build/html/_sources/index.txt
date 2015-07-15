=============
Cloud Servers
=============

Preface
--------

.. toctree::
   :maxdepth: 2

   preface
   pricing-and-service-level

General API Information
-----------------------

API v2 is defined as a RESTful HTTP service that uses all aspects of the HTTP protocol, including methods, URIs, media types, and response codes. To request next generation Cloud Servers services, you must first issue an authentication request to the Rackspace Cloud Identity Service, which is an implementation of the OpenStack Keystone Identity Service v2.0.

API v2 supports JSON request and response formats.

.. toctree::
   :maxdepth: 2

   cloud-servers-concepts
   how-curl-commands-work
   authenticate-through-the-rackspace-cloud-identity-service
   request-response-types
   links-and-references
   paginated-collections
   efficient-polling-with-the-changes-since-parameter
   quotas
   limits
   extensions
   faults
   role-based-access-control
   flavors
   service-access-endpoints

API Operations
--------------

.. toctree::
   :maxdepth: 2
   :glob:

   api/DELETE_delete_image_images_image_id_
   api/DELETE_delete_key_pair_os-keypairs_keypair_name_
   api/DELETE_delete_network_os-networksv2_id_
   api/DELETE_delete_server_metadata_item_servers_server_id_metadata_key_
   api/DELETE_delete_server_servers_server_id_
   api/DELETE_delete_virtual_interface_servers_server_id_os-virtual-interfacesv2_interface_id_
   api/DELETE_delete_volume_attachment_from_server_servers_server_id_os-volume_attachments_attachment_id_
   api/DELETE_disable_scheduled_images_servers_server_id_rax-si-scheduled-image
   api/GET_create_server_with_disk_config_servers
   api/GET_list_networks_os-networksv2
   api/GET_list_server_metadata_servers_server_id_metadata
   api/GET_list_server_metadata_servers_server_id_os-volume_attachments
   api/GET_list_servers_servers
   api/GET_list_servers_with_details_servers_detail
   api/GET_retrieve_flavor_details_flavors
   api/GET_retrieve_image_details_images_image_id_
   api/GET_retrieve_list_of_images_images
   api/GET_retrieve_list_of_images_with_details_images_detail
   api/GET_retrieve_list_of_key_pairs_os-keypairs
   api/GET_retrieve_list_of_network_addresses_for_server_and_network_servers_server_id_ips_network_label_
   api/GET_retrieve_list_of_rate_and_absolute_limits_limits
   api/GET_retrieve_list_of_server_addresses_servers_server_id_ips
   api/GET_retrieve_list_of_virtual_interfaces_servers_server_id_os-virtual-interfacesv2
   api/GET_retrieve_of_list_flavors_flavors
   api/GET_retrieve_server_details_servers_server_id_
   api/GET_show_flavor_extra_specs_flavors_flavor_id_
   api/GET_show_network_os-networksv2_id_
   api/GET_show_scheduled_images_servers_server_id_rax-si-scheduled-image
   api/GET_show_server_metadata_item_details_servers_server_id_metadata_key_
   api/POST_change_password_for_specified_server_servers_server_id_actions
   api/POST_confirm_server_resize_for_specified_server_servers_server_id_actions
   api/POST_create_a_server_key_pair_os-keypairs
   api/POST_create_image_of_specified_server_servers_server_id_actions
   api/POST_create_network_os-networksv2
   api/POST_create_server_servers
   api/POST_create_virtual_interface_and_attach_to_server_servers_server_id_os-virtual-interfacesv2
   api/POST_create_volume_os-volumes
   api/POST_delete_volume_os-volumes_id_
   api/POST_enable_scheduled_images_servers_server_id_rax-si-scheduled-image
   api/POST_get_console_servers_servers_action
   api/POST_import_a_server_key_pair_os-keypairs
   api/POST_reboot_specified_server_servers_server_id_actions
   api/POST_rebuild_specified_server_servers_server_id_actions
   api/POST_rescue_specified_server_servers_server_id_actions
   api/POST_resize_specified_server_servers_server_id_actions
   api/POST_retrieve_list_of_volumes_os-volumes
   api/POST_revert_server_resize_for_specified_server_servers_server_id_actions
   api/POST_show_volume_details_os-volumes_id_
   api/POST_unrescue_specified_server_servers_server_id_actions
   api/POST_update_server_metadata_servers_server_id_metadata
   api/PUT_attach_voume_to_server_servers_server_id_os-volume_attachments
   api/PUT_set_server_metadata_item_servers_server_id_metadata_key_
   api/PUT_set_server_metadata_servers_server_id_metadata
   api/PUT_show_volume_attachment_details_servers_server_id_os-volume_attachments_attachment_id_
   api/PUT_update_server_servers_server_id_

Rackspace Extensions
--------------------

.. toctree::
   :maxdepth: 2

   rackspace-extensions
   disk-configuration-extension
   extended-status-extension
   rescue-mode-extension
   used-limits-extension
   scheduled-images-extension
   flavors-extra-specs-extension
   instance-actions-extension
   config-drive-extension
   launch-an-instance-from-a-volume
   network-extension

