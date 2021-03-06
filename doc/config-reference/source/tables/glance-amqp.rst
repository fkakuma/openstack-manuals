..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _glance-amqp:

.. list-table:: Description of AMQP configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[DEFAULT]**
     -
   * - ``control_exchange`` = ``openstack``
     - (StrOpt) The default exchange under which topics are scoped. May be overridden by an exchange name specified in the transport_url option.
   * - ``default_publisher_id`` = ``image.localhost``
     - (StrOpt) Default publisher_id for outgoing notifications.
   * - ``disabled_notifications`` =
     - (ListOpt) List of disabled notifications. A notification can be given either as a notification type to disable a single event, or as a notification group prefix to disable all events within a group. Example: if this config option is set to ["image.create", "metadef_namespace"], then "image.create" notification will not be sent after image is created and none of the notifications for metadefinition namespaces will be sent.
   * - ``transport_url`` = ``None``
     - (StrOpt) A URL representing the messaging driver to use and its full configuration. If not set, we fall back to the rpc_backend option and driver specific configuration.
   * - **[oslo_messaging_notifications]**
     -
   * - ``driver`` = ``[]``
     - (MultiStrOpt) The Drivers(s) to handle sending notifications. Possible values are messaging, messagingv2, routing, log, test, noop
   * - ``topics`` = ``notifications``
     - (ListOpt) AMQP topic used for OpenStack notifications.
   * - ``transport_url`` = ``None``
     - (StrOpt) A URL representing the messaging driver to use for notifications. If not set, we fall back to the same configuration used for RPC.
