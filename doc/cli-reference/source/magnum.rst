.. ## WARNING ######################################
.. This file is automatically generated, do not edit
.. #################################################

======================================
Containers service command-line client
======================================

The magnum client is the command-line interface (CLI) for
the Containers service API and its extensions.

This chapter documents :command:`magnum` version ``1.1.0``.

For help on a specific :command:`magnum` command, enter:

.. code-block:: console

   $ magnum help COMMAND

.. _magnum_command_usage:

magnum usage
~~~~~~~~~~~~

.. code-block:: console

   usage: magnum [--version] [--debug] [--os-cache]
                 [--os-region-name <region-name>]
                 [--os-tenant-id <auth-tenant-id>]
                 [--service-type <service-type>]
                 [--endpoint-type <endpoint-type>]
                 [--magnum-api-version <magnum-api-ver>]
                 [--os-cacert <ca-certificate>] [--bypass-url <bypass-url>]
                 [--os-auth-system <auth-system>] [--os-username <username>]
                 [--os-password <password>] [--os-tenant-name <tenant-name>]
                 [--os-token <token>] [--os-auth-url <auth-url>]
                 <subcommand> ...

Subcommands
-----------

``baymodel-create``
  Create a baymodel.

``baymodel-delete``
  Delete specified baymodel.

``baymodel-list``
  Print a list of bay models.

``baymodel-show``
  Show details about the given baymodel.

``baymodel-update``
  Updates one or more baymodel attributes.

``bay-create``
  Create a bay.

``bay-delete``
  Delete specified bay.

``bay-list``
  Print a list of available bays.

``bay-show``
  Show details about the given bay.

``bay-update``
  Update information about the given bay.

``ca-show``
  Show details about the CA certificate for a bay.

``ca-sign``
  Generate the CA certificate for a bay.

``container-create``
  Create a container.

``container-delete``
  Delete specified containers.

``container-exec``
  Execute command in a container.

``container-list``
  Print a list of available containers.

``container-logs``
  Get logs of a container.

``container-pause``
  Pause specified containers.

``container-reboot``
  Reboot specified containers.

``container-show``
  Show details of a container.

``container-start``
  Start specified containers.

``container-stop``
  Stop specified containers.

``container-unpause``
  Unpause specified containers.

``service-list``
  Print a list of magnum services.

``node-create``
  Create a node.

``node-list``
  Print a list of configured nodes.

``pod-create``
  Create a pod.

``pod-delete``
  Delete specified pod.

``pod-list``
  Print a list of registered pods.

``pod-show``
  Show details about the given pod.

``pod-update``
  Update information about the given pod.

``rc-create``
  Create a replication controller.

``rc-delete``
  Delete specified replication controller.

``rc-list``
  Print a list of registered replication controllers.

``rc-show``
  Show details about the given replication controller.

``rc-update``
  Update information about the given replication
  controller.

``coe-service-create``
  Create a coe service.

``coe-service-delete``
  Delete specified coe service(s).

``coe-service-list``
  Print a list of coe services.

``coe-service-show``
  Show details about the given coe service.

``coe-service-update``
  Update information about the given coe service.

``bash-completion``
  Prints arguments for bash-completion. Prints all of
  the commands and options to stdout so that the
  magnum.bash_completion script doesn't have to hard
  code them.

``help``
  Display help about this program or one of its
  subcommands.

.. _magnum_command_options:

magnum optional arguments
~~~~~~~~~~~~~~~~~~~~~~~~~

``--version``
  show program's version number and exit

``--debug``
  Print debugging output.

``--os-cache``
  Use the auth token cache. Defaults to False if
  ``env[OS_CACHE]`` is not set.

``--os-region-name <region-name>``
  Region name. Default= ``env[OS_REGION_NAME]``.

``--os-tenant-id <auth-tenant-id>``
  Defaults to ``env[OS_TENANT_ID]``.

``--service-type <service-type>``
  Defaults to container for all actions.

``--endpoint-type <endpoint-type>``
  Defaults to ``env[MAGNUM_ENDPOINT_TYPE]`` or publicURL.

``--magnum-api-version <magnum-api-ver>``
  Accepts "api", defaults to ``env[MAGNUM_API_VERSION]``.

``--os-cacert <ca-certificate>``
  Specify a CA bundle file to use in verifying a TLS
  (https) server certificate. Defaults to
  ``env[OS_CACERT]``.

``--bypass-url <bypass-url>``
  Use this API endpoint instead of the Service Catalog.


magnum.. _magnum_common_auth:

magnum common authentication arguments
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

``--os-auth-system <auth-system>``
  Defaults to ``env[OS_AUTH_SYSTEM]``.

``--os-username <username>``
  Defaults to ``env[OS_USERNAME]``.

``--os-password <password>``
  Defaults to ``env[OS_PASSWORD]``.

``--os-tenant-name <tenant-name>``
  Defaults to ``env[OS_TENANT_NAME]``.

``--os-token <token>``
  Defaults to ``env[OS_TOKEN]``.

``--os-auth-url <auth-url>``
  Defaults to ``env[OS_AUTH_URL]``.

.. _magnum_bay-create:

magnum bay-create
~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum bay-create [--name <name>] --baymodel <baymodel>
                            [--node-count <node-count>]
                            [--master-count <master-count>]
                            [--discovery-url <discovery-url>]
                            [--timeout <timeout>]

Create a bay.

Optional arguments
------------------

``--name <name>``
  Name of the bay to create.

``--baymodel <baymodel>``
  ID or name of the baymodel.

``--node-count <node-count>``
  The bay node count.

``--master-count <master-count>``
  The number of master nodes for the bay.

``--discovery-url <discovery-url>``
  Specifies custom discovery url for node discovery.

``--timeout <timeout>``
  The timeout for bay creation in minutes. Set to 0 for
  no timeout. The default is no timeout.

.. _magnum_bay-delete:

magnum bay-delete
~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum bay-delete <bay> [<bay> ...]

Delete specified bay.

Positional arguments
--------------------

``<bay>``
  ID or name of the (bay)s to delete.

.. _magnum_bay-list:

magnum bay-list
~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum bay-list

Print a list of available bays.

.. _magnum_bay-show:

magnum bay-show
~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum bay-show <bay>

Show details about the given bay.

Positional arguments
--------------------

``<bay>``
  ID or name of the bay to show.

.. _magnum_bay-update:

magnum bay-update
~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum bay-update <bay> <op> <path=value> [<path=value> ...]

Update information about the given bay.

Positional arguments
--------------------

``<bay>``
  UUID or name of bay

``<op>``
  Operations: 'add', 'replace' or 'remove'

``<path=value>``
  Attributes to add/replace or remove (only PATH is necessary on
  remove)

.. _magnum_baymodel-create:

magnum baymodel-create
~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum baymodel-create [--name <name>] --image-id <image-id>
                                 --keypair-id <keypair-id> --external-network-id
                                 <external-network-id> --coe <coe>
                                 [--fixed-network <fixed-network>]
                                 [--network-driver <network-driver>]
                                 [--ssh-authorized-key <ssh-authorized-key>]
                                 [--dns-nameserver <dns-nameserver>]
                                 [--flavor-id <flavor-id>]
                                 [--master-flavor-id <master-flavor-id>]
                                 [--docker-volume-size <docker-volume-size>]
                                 [--http-proxy <http-proxy>]
                                 [--https-proxy <https-proxy>]
                                 [--no-proxy <no-proxy>]
                                 [--labels <KEY1=VALUE1,KEY2=VALUE2...>]
                                 [--tls-disabled] [--public]

Create a baymodel.

Optional arguments
------------------

``--name <name>``
  Name of the bay to create.

``--image-id <image-id>``
  The name or UUID of the base image to customize for
  the bay.

``--keypair-id <keypair-id>``
  The name or UUID of the SSH keypair to load into the
  Bay nodes.

``--external-network-id <external-network-id>``
  The external Neutron network ID to connect to this bay
  model.

``--coe <coe>``
  Specify the Container Orchestration Engine to use.

``--fixed-network <fixed-network>``
  The private Neutron network name to connect to this
  bay model.

``--network-driver <network-driver>``
  The network driver name for instantiating container
  networks.

``--ssh-authorized-key <ssh-authorized-key>``
  The SSH authorized key to use

``--dns-nameserver <dns-nameserver>``
  The DNS nameserver to use for this Bay.

``--flavor-id <flavor-id>``
  The nova flavor id to use when launching the bay.

``--master-flavor-id <master-flavor-id>``
  The nova flavor id to use when launching the master
  node of the bay.

``--docker-volume-size <docker-volume-size>``
  Specify the number of size in GB for the docker volume
  to use.

``--http-proxy <http-proxy>``
  The http_proxy address to use for nodes in bay.

``--https-proxy <https-proxy>``
  The https_proxy address to use for nodes in bay.

``--no-proxy <no-proxy>``
  The no_proxy address to use for nodes in bay.

``--labels <KEY1=VALUE1,KEY2=VALUE2...>``
  Arbitrary labels in the form of key=value pairs to
  associate with a baymodel. May be used multiple times.

``--tls-disabled``
  Disable TLS in the Bay.

``--public``
  Make baymodel public.

.. _magnum_baymodel-delete:

magnum baymodel-delete
~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum baymodel-delete <baymodels> [<baymodels> ...]

Delete specified baymodel.

Positional arguments
--------------------

``<baymodels>``
  ID or name of the (baymodel)s to delete.

.. _magnum_baymodel-list:

magnum baymodel-list
~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum baymodel-list

Print a list of bay models.

.. _magnum_baymodel-show:

magnum baymodel-show
~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum baymodel-show <baymodel>

Show details about the given baymodel.

Positional arguments
--------------------

``<baymodel>``
  ID of the baymodel to show.

.. _magnum_baymodel-update:

magnum baymodel-update
~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum baymodel-update <baymodel> <op> <path=value> [<path=value> ...]

Updates one or more baymodel attributes.

Positional arguments
--------------------

``<baymodel>``
  UUID or name of baymodel

``<op>``
  Operations: 'add', 'replace' or 'remove'

``<path=value>``
  Attributes to add/replace or remove (only PATH is necessary on
  remove)

.. _magnum_ca-show:

magnum ca-show
~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum ca-show --bay <bay>

Show details about the CA certificate for a bay.

Optional arguments
------------------

``--bay <bay>``
  ID or name of the bay.

.. _magnum_ca-sign:

magnum ca-sign
~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum ca-sign [--csr <csr>] --bay <bay>

Generate the CA certificate for a bay.

Optional arguments
------------------

``--csr <csr>``
  File path of the csr file to send to Magnum to get signed.

``--bay <bay>``
  ID or name of the bay.

.. _magnum_coe-service-create:

magnum coe-service-create
~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum coe-service-create [--manifest-url <manifest-url>]
                                    [--manifest <manifest>] --bay <bay>

Create a coe service.

Optional arguments
------------------

``--manifest-url <manifest-url>``
  Name/URL of the serivce file to use for creating
  services.

``--manifest <manifest>``
  File path of the service file to use for creating
  services.

``--bay <bay>``
  Id or name of the bay.

.. _magnum_coe-service-delete:

magnum coe-service-delete
~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum coe-service-delete <services> [<services> ...] <bay>

Delete specified coe service(s).

Positional arguments
--------------------

``<services>``
  ID or name of the (service)s to delete.

``<bay>``
  UUID or Name of Bay

.. _magnum_coe-service-list:

magnum coe-service-list
~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum coe-service-list <bay>

Print a list of coe services.

Positional arguments
--------------------

``<bay>``
  UUID or Name of Bay

.. _magnum_coe-service-show:

magnum coe-service-show
~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum coe-service-show <service> <bay>

Show details about the given coe service.

Positional arguments
--------------------

``<service>``
  ID or name of the service to show.

``<bay>``
  UUID or Name of Bay

.. _magnum_coe-service-update:

magnum coe-service-update
~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum coe-service-update <service> <bay> <op> <path=value>
                                    [<path=value> ...]

Update information about the given coe service.

Positional arguments
--------------------

``<service>``
  UUID or name of service

``<bay>``
  UUID or Name of Bay

``<op>``
  Operations: 'add', 'replace' or 'remove'

``<path=value>``
  Attributes to add/replace or remove (only PATH is necessary on
  remove)

.. _magnum_container-create:

magnum container-create
~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum container-create [--name <name>] --image <image> --bay <bay>
                                  [--command <command>] [--memory <memory>]

Create a container.

Optional arguments
------------------

``--name <name>``
  name of the container

``--image <image>``
  name or ID of the image

``--bay <bay>``
  ID or name of the bay.

``--command <command>``
  Send command to the container

``--memory <memory>``
  The container memory size (format: <number><optional
  unit>, where unit = b, k, m or g)

.. _magnum_container-delete:

magnum container-delete
~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum container-delete <container> [<container> ...]

Delete specified containers.

Positional arguments
--------------------

``<container>``
  ID or name of the (container)s to delete.

.. _magnum_container-exec:

magnum container-exec
~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum container-exec --command <command> <container>

Execute command in a container.

Positional arguments
--------------------

``<container>``
  ID or name of the container to start.

Optional arguments
------------------

``--command <command>``
  The command to execute

.. _magnum_container-list:

magnum container-list
~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum container-list

Print a list of available containers.

.. _magnum_container-logs:

magnum container-logs
~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum container-logs <container>

Get logs of a container.

Positional arguments
--------------------

``<container>``
  ID or name of the container to start.

.. _magnum_container-pause:

magnum container-pause
~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum container-pause <container> [<container> ...]

Pause specified containers.

Positional arguments
--------------------

``<container>``
  ID or name of the (container)s to start.

.. _magnum_container-reboot:

magnum container-reboot
~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum container-reboot <container> [<container> ...]

Reboot specified containers.

Positional arguments
--------------------

``<container>``
  ID or name of the (container)s to start.

.. _magnum_container-show:

magnum container-show
~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum container-show [--json] <container>

Show details of a container.

Positional arguments
--------------------

``<container>``
  ID or name of the container to show.

Optional arguments
------------------

``--json``
  Print JSON representation of the container.

.. _magnum_container-start:

magnum container-start
~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum container-start <container> [<container> ...]

Start specified containers.

Positional arguments
--------------------

``<container>``
  ID of the (container)s to start.

.. _magnum_container-stop:

magnum container-stop
~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum container-stop <container> [<container> ...]

Stop specified containers.

Positional arguments
--------------------

``<container>``
  ID or name of the (container)s to start.

.. _magnum_container-unpause:

magnum container-unpause
~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum container-unpause <container> [<container> ...]

Unpause specified containers.

Positional arguments
--------------------

``<container>``
  ID or name of the (container)s to start.

.. _magnum_node-create:

magnum node-create
~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum node-create [--type <type>] [--image-id <image-id>]

Create a node.

Optional arguments
------------------

``--type <type>``
  Type of node to create (virt or bare).

``--image-id <image-id>``
  The name or UUID of the base image to use for the
  node.

.. _magnum_node-list:

magnum node-list
~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum node-list

Print a list of configured nodes.

.. _magnum_pod-create:

magnum pod-create
~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum pod-create [--manifest-url <manifest-url>]
                            [--manifest <manifest>] --bay <bay>

Create a pod.

Optional arguments
------------------

``--manifest-url <manifest-url>``
  Name/URL of the pod file to use for creating PODs.

``--manifest <manifest>``
  File path of the pod file to use for creating PODs.

``--bay <bay>``
  ID or name of the bay.

.. _magnum_pod-delete:

magnum pod-delete
~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum pod-delete <pods> [<pods> ...] <bay>

Delete specified pod.

Positional arguments
--------------------

``<pods>``
  ID or name of the (pod)s to delete.

``<bay>``
  UUID or Name of Bay

.. _magnum_pod-list:

magnum pod-list
~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum pod-list <bay>

Print a list of registered pods.

Positional arguments
--------------------

``<bay>``
  UUID or Name of Bay

.. _magnum_pod-show:

magnum pod-show
~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum pod-show <pod> <bay>

Show details about the given pod.

Positional arguments
--------------------

``<pod>``
  ID or name of the pod to show.

``<bay>``
  UUID or Name of Bay

.. _magnum_pod-update:

magnum pod-update
~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum pod-update <pod-id> <bay> <op> <path=value> [<path=value> ...]

Update information about the given pod.

Positional arguments
--------------------

``<pod-id>``
  UUID or name of pod

``<bay>``
  UUID or Name of Bay

``<op>``
  Operations: 'add', 'replace' or 'remove'

``<path=value>``
  Attributes to add/replace or remove (only PATH is necessary on
  remove)

.. _magnum_rc-create:

magnum rc-create
~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum rc-create [--manifest-url <manifest-url>]
                           [--manifest <manifest>] --bay <bay>

Create a replication controller.

Optional arguments
------------------

``--manifest-url <manifest-url>``
  Name/URL of the replication controller file to use for
  creating replication controllers.

``--manifest <manifest>``
  File path of the replication controller file to use
  for creating replication controllers.

``--bay <bay>``
  ID or name of the bay.

.. _magnum_rc-delete:

magnum rc-delete
~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum rc-delete <rcs> [<rcs> ...] <bay>

Delete specified replication controller.

Positional arguments
--------------------

``<rcs>``
  ID or name of the replication (controller)s to delete.

``<bay>``
  UUID or Name of Bay

.. _magnum_rc-list:

magnum rc-list
~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum rc-list <bay>

Print a list of registered replication controllers.

Positional arguments
--------------------

``<bay>``
  UUID or Name of Bay

.. _magnum_rc-show:

magnum rc-show
~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum rc-show <rc> <bay>

Show details about the given replication controller.

Positional arguments
--------------------

``<rc>``
  ID or name of the replication controller to show.

``<bay>``
  UUID or Name of Bay

.. _magnum_rc-update:

magnum rc-update
~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum rc-update <rc> <bay> <op> <path=value> [<path=value> ...]

Update information about the given replication controller.

Positional arguments
--------------------

``<rc>``
  UUID or name of replication controller

``<bay>``
  UUID or Name of Bay

``<op>``
  Operations: 'add', 'replace' or 'remove'

``<path=value>``
  Attributes to add/replace or remove (only PATH is necessary on
  remove)

.. _magnum_service-list:

magnum service-list
~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: magnum service-list

Print a list of magnum services.

