..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _manila-share:

.. list-table:: Description of Share configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[DEFAULT]**
     -
   * - ``automatic_share_server_cleanup`` = ``True``
     - (BoolOpt) If set to True, then Manila will delete all share servers which were unused more than specified time .If set to False - automatic deletion of share servers will be disabled.
   * - ``backlog`` = ``4096``
     - (IntOpt) Number of backlog requests to configure the socket with.
   * - ``default_share_type`` = ``None``
     - (StrOpt) Default share type to use.
   * - ``delete_share_server_with_last_share`` = ``False``
     - (BoolOpt) Whether share servers will be deleted on deletion of the last share.
   * - ``driver_handles_share_servers`` = ``None``
     - (BoolOpt) There are two possible approaches for share drivers in Manila. First is when share driver is able to handle share-servers and second when not. Drivers can support either both or only one of these approaches. So, set this opt to True if share driver is able to handle share servers and it is desired mode else set False. It is set to None by default to make this choice intentional.
   * - ``enable_periodic_hooks`` = ``False``
     - (BoolOpt) Whether to enable periodic hooks or not.
   * - ``enable_post_hooks`` = ``False``
     - (BoolOpt) Whether to enable post hooks or not.
   * - ``enable_pre_hooks`` = ``False``
     - (BoolOpt) Whether to enable pre hooks or not.
   * - ``enabled_share_backends`` = ``None``
     - (ListOpt) A list of share backend names to use. These backend names should be backed by a unique [CONFIG] group with its options.
   * - ``enabled_share_protocols`` = ``NFS, CIFS``
     - (ListOpt) Specify list of protocols to be allowed for share creation. Available values are '('NFS', 'CIFS', 'GLUSTERFS', 'HDFS')'
   * - ``executor_thread_pool_size`` = ``64``
     - (IntOpt) Size of executor thread pool.
   * - ``hook_drivers`` =
     - (ListOpt) Driver(s) to perform some additional actions before and after share driver actions and on a periodic basis. Default is [].
   * - ``migration_create_delete_share_timeout`` = ``300``
     - (IntOpt) Timeout for creating and deleting share instances when performing share migration (seconds).
   * - ``migration_data_copy_node_ip`` = ``None``
     - (StrOpt) The IP of the node responsible for copying data during migration, such as the data copy service node, reachable by the backend.
   * - ``migration_ignore_files`` = ``lost+found``
     - (ListOpt) List of files and folders to be ignored when migrating shares. Items should be names (not including any path).
   * - ``migration_mounting_backend_ip`` = ``None``
     - (StrOpt) Backend IP in admin network to use for mounting shares during migration.
   * - ``migration_protocol_mount_command`` = ``None``
     - (StrOpt) The command for mounting shares for this backend. Must specifythe executable and all necessary parameters for the protocol supported. It is advisable to separate protocols per backend.
   * - ``migration_readonly_support`` = ``True``
     - (BoolOpt) Specify whether read only access mode is supported in thisbackend.
   * - ``migration_tmp_location`` = ``/tmp/``
     - (StrOpt) Temporary path to create and mount shares during migration.
   * - ``migration_wait_access_rules_timeout`` = ``90``
     - (IntOpt) Time to wait for access rules to be allowed/denied on backends when migrating shares using generic approach (seconds).
   * - ``network_config_group`` = ``None``
     - (StrOpt) Name of the configuration group in the Manila conf file to look for network config options.If not set, the share backend's config group will be used.If an option is not found within provided group, then'DEFAULT' group will be used for search of option.
   * - ``root_helper`` = ``sudo``
     - (StrOpt) Deprecated: command to use for running commands as root.
   * - ``share_manager`` = ``manila.share.manager.ShareManager``
     - (StrOpt) Full class name for the share manager.
   * - ``share_name_template`` = ``share-%s``
     - (StrOpt) Template string to be used to generate share names.
   * - ``share_snapshot_name_template`` = ``share-snapshot-%s``
     - (StrOpt) Template string to be used to generate share snapshot names.
   * - ``share_usage_audit_period`` = ``month``
     - (StrOpt) Time period to generate share usages for. Time period must be hour, day, month or year.
   * - ``suppress_post_hooks_errors`` = ``False``
     - (BoolOpt) Whether to suppress post hook errors (allow driver's results to pass through) or not.
   * - ``suppress_pre_hooks_errors`` = ``False``
     - (BoolOpt) Whether to suppress pre hook errors (allow driver perform actions) or not.
   * - ``unmanage_remove_access_rules`` = ``False``
     - (BoolOpt) If set to True, then manila will deny access and remove all access rules on share unmanage.If set to False - nothing will be changed.
   * - ``unused_share_server_cleanup_interval`` = ``10``
     - (IntOpt) Unallocated share servers reclamation time interval (minutes). Minimum value is 10 minutes, maximum is 60 minutes. The reclamation function is run every 10 minutes and delete share servers which were unused more than unused_share_server_cleanup_interval option defines. This value reflects the shortest time Manila will wait for a share server to go unutilized before deleting it.
   * - ``use_scheduler_creating_share_from_snapshot`` = ``False``
     - (BoolOpt) If set to False, then share creation from snapshot will be performed on the same host. If set to True, then scheduling step will be used.
