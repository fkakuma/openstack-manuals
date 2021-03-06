..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _glance-filesystem:

.. list-table:: Description of filesystem configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[glance_store]**
     -
   * - ``filesystem_store_datadir`` = ``/var/lib/glance/images``
     - (StrOpt) Directory to which the Filesystem backend store writes images.
   * - ``filesystem_store_datadirs`` = ``None``
     - (MultiStrOpt) List of directories and its priorities to which the Filesystem backend store writes images.
   * - ``filesystem_store_file_perm`` = ``0``
     - (IntOpt) The required permission for created image file. In this way the user other service used, e.g. Nova, who consumes the image could be the exclusive member of the group that owns the files created. Assigning it less then or equal to zero means don't change the default permission of the file. This value will be decoded as an octal digit.
   * - ``filesystem_store_metadata_file`` = ``None``
     - (StrOpt) The path to a file which contains the metadata to be returned with any location associated with this store. The file must contain a valid JSON object. The object should contain the keys 'id' and 'mountpoint'. The value for both keys should be 'string'.
