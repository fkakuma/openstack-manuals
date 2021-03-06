..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _zaqar-api:

.. list-table:: Description of API configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[DEFAULT]**
     -
   * - ``admin_mode`` = ``False``
     - (BoolOpt) Activate privileged endpoints.
   * - ``daemon`` = ``False``
     - (BoolOpt) Run Zaqar server in the background.
   * - ``unreliable`` = ``False``
     - (BoolOpt) Disable all reliability constraints.
   * - **[notification]**
     -
   * - ``smtp_command`` = ``/usr/sbin/sendmail -t -oi``
     - (StrOpt) The command of smtp to send email. The format is "command_name arg1 arg2".
   * - **[oslo_policy]**
     -
   * - ``policy_default_rule`` = ``default``
     - (StrOpt) Default rule. Enforced when a requested rule is not found.
   * - ``policy_dirs`` = ``['policy.d']``
     - (MultiStrOpt) Directories where policy configuration files are stored. They can be relative to any directory in the search path defined by the config_dir option, or absolute paths. The file defined by policy_file must exist for these directories to be searched. Missing or empty directories are ignored.
   * - ``policy_file`` = ``policy.json``
     - (StrOpt) The JSON file that defines policies.
   * - **[signed_url]**
     -
   * - ``secret_key`` = ``None``
     - (StrOpt) Secret key used to encrypt pre-signed URLs.
