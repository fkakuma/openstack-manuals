..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _nova-ironic:

.. list-table:: Description of bare metal configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[ironic]**
     -
   * - ``admin_auth_token`` = ``None``
     - (StrOpt) Ironic keystone auth token.DEPRECATED: use admin_username, admin_password, and admin_tenant_name instead
   * - ``admin_password`` = ``None``
     - (StrOpt) Ironic keystone admin password.
   * - ``admin_tenant_name`` = ``None``
     - (StrOpt) Ironic keystone tenant name.
   * - ``admin_url`` = ``None``
     - (StrOpt) Keystone public API endpoint.
   * - ``admin_username`` = ``None``
     - (StrOpt) Ironic keystone admin name
   * - ``api_endpoint`` = ``None``
     - (StrOpt) URL for Ironic API endpoint.
   * - ``api_max_retries`` = ``60``
     - (IntOpt) How many retries when a request does conflict. If <= 0, only try once, no retries.
   * - ``api_retry_interval`` = ``2``
     - (IntOpt) How often to retry in seconds when a request does conflict
   * - ``api_version`` = ``1``
     - (IntOpt) Version of Ironic API service endpoint. DEPRECATED: Setting the API version is not possible anymore.
   * - ``client_log_level`` = ``None``
     - (StrOpt) Log level override for ironicclient. Set this in order to override the global "default_log_levels", "verbose", and "debug" settings. DEPRECATED: use standard logging configuration.
