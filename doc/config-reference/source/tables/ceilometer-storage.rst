..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _ceilometer-storage:

.. list-table:: Description of storage configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[storage]**
     -
   * - ``max_retries`` = ``10``
     - (IntOpt) Maximum number of connection retries during startup. Set to -1 to specify an infinite retry count.
   * - ``retry_interval`` = ``10``
     - (IntOpt) Interval (in seconds) between retries of connection.
