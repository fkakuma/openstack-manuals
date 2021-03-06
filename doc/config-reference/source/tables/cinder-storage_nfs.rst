..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _cinder-storage_nfs:

.. list-table:: Description of NFS storage configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[DEFAULT]**
     -
   * - ``nfs_mount_attempts`` = ``3``
     - (IntOpt) The number of attempts to mount NFS shares before raising an error. At least one attempt will be made to mount an NFS share, regardless of the value specified.
   * - ``nfs_mount_options`` = ``None``
     - (StrOpt) Mount options passed to the NFS client. See section of the NFS man page for details.
   * - ``nfs_mount_point_base`` = ``$state_path/mnt``
     - (StrOpt) Base dir containing mount points for NFS shares.
   * - ``nfs_oversub_ratio`` = ``1.0``
     - (FloatOpt) This will compare the allocated to available space on the volume destination. If the ratio exceeds this number, the destination will no longer be valid. Note that this option is deprecated in favor of "max_oversubscription_ratio" and will be removed in the Mitaka release.
   * - ``nfs_shares_config`` = ``/etc/cinder/nfs_shares``
     - (StrOpt) File with the list of available NFS shares
   * - ``nfs_sparsed_volumes`` = ``True``
     - (BoolOpt) Create volumes as sparsed files which take no space.If set to False volume is created as regular file.In such case volume creation takes a lot of time.
   * - ``nfs_used_ratio`` = ``0.95``
     - (FloatOpt) Percent of ACTUAL usage of the underlying volume before no new volumes can be allocated to the volume destination. Note that this option is deprecated in favor of "reserved_percentage" and will be removed in the Mitaka release.
