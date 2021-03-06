.. ## WARNING ######################################
.. This file is automatically generated, do not edit
.. #################################################

======================================
Clustering service command-line client
======================================

The senlin client is the command-line interface (CLI) for
the Clustering service API and its extensions.

This chapter documents :command:`senlin` version ``0.2.1``.

For help on a specific :command:`senlin` command, enter:

.. code-block:: console

   $ senlin help COMMAND

.. _senlin_command_usage:

senlin usage
~~~~~~~~~~~~

.. code-block:: console

   usage: senlin [--version] [-d] [-v] [--api-timeout API_TIMEOUT]
                 [--senlin-api-version SENLIN_API_VERSION]
                 [--os-auth-plugin AUTH_PLUGIN] [--os-auth-url AUTH_URL]
                 [--os-project-id PROJECT_ID] [--os-project-name PROJECT_NAME]
                 [--os-tenant-id TENANT_ID] [--os-tenant-name TENANT_NAME]
                 [--os-domain-id DOMAIN_ID] [--os-domain-name DOMAIN_NAME]
                 [--os-project-domain-id PROJECT_DOMAIN_ID]
                 [--os-project-domain-name PROJECT_DOMAIN_NAME]
                 [--os-user-domain-id USER_DOMAIN_ID]
                 [--os-user-domain-name USER_DOMAIN_NAME]
                 [--os-username USERNAME] [--os-user-id USER_ID]
                 [--os-password PASSWORD] [--os-trust-id TRUST_ID]
                 [--os-cacert CA_BUNDLE_FILE | --verify | --insecure]
                 [--os-token TOKEN] [--os-access-info ACCESS_INFO]
                 [--os-api-name <service>=<name>]
                 [--os-api-region <service>=<region>]
                 [--os-api-version <service>=<version>]
                 [--os-api-interface <service>=<interface>]
                 <subcommand> ...

Subcommands
-----------

``action-list``
  List actions.

``action-show``
  Show detailed info about the specified action.

``build-info``
  Retrieve build information.

``cluster-create``
  Create the cluster.

``cluster-delete``
  Delete the cluster(s).

``cluster-list``
  List the user's clusters.

``cluster-node-add``
  Add specified nodes to cluster.

``cluster-node-del``
  Delete specified nodes from cluster.

``cluster-node-list``
  List nodes from cluster.

``cluster-policy-attach``
  Attach policy to cluster.

``cluster-policy-detach``
  Detach policy from cluster.

``cluster-policy-disable``
  Disable a policy on a cluster.

``cluster-policy-enable``
  Enable a policy on a cluster.

``cluster-policy-list``
  List policies from cluster.

``cluster-policy-show``
  Show a specific policy that is bound to the specified
  cluster.

``cluster-policy-update``
  Update a policy's properties on a cluster.

``cluster-resize``
  Resize a cluster.

``cluster-scale-in``
  Scale in a cluster by the specified number of nodes.

``cluster-scale-out``
  Scale out a cluster by the specified number of nodes.

``cluster-show``
  Show details of the cluster.

``cluster-update``
  Update the cluster.

``event-list``
  List events.

``event-show``
  Describe the event.

``node-create``
  Create the node.

``node-delete``
  Delete the node(s).

``node-join``
  Make node join the specified cluster.

``node-leave``
  Make node leave its current cluster.

``node-list``
  Show list of nodes.

``node-show``
  Show detailed info about the specified node.

``node-update``
  Update the node.

``policy-create``
  Create a policy.

``policy-delete``
  Delete policy(s).

``policy-list``
  List policies that meet the criteria.

``policy-show``
  Show the policy details.

``policy-type-list``
  List the available policy types.

``policy-type-show``
  Get the details about a policy type.

``policy-update``
  Update a policy.

``profile-create``
  Create a profile.

``profile-delete``
  Delete profile(s).

``profile-list``
  List profiles that meet the criteria.

``profile-show``
  Show the profile details.

``profile-type-list``
  List the available profile types.

``profile-type-show``
  Get the details about a profile type.

``profile-update``
  Update a profile.

``receiver-create``
  Create a receiver.

``receiver-delete``
  Delete receiver(s).

``receiver-list``
  List receivers that meet the criteria.

``receiver-show``
  Show the receiver details.

``bash-completion``
  Prints all of the commands and options to stdout.

``help``
  Display help about this program or one of its
  subcommands.

.. _senlin_command_options:

senlin optional arguments
~~~~~~~~~~~~~~~~~~~~~~~~~

``--version``
  Shows the client version and exits.

``-d, --debug``
  Defaults to ``env[SENLINCLIENT_DEBUG]``.

``-v, --verbose``
  Print more verbose output.

``--api-timeout API_TIMEOUT``
  Number of seconds to wait for an API response,
  defaults to system socket timeout

``--senlin-api-version SENLIN_API_VERSION``
  Version number for Senlin API to use, Default to "1".

``--os-auth-plugin AUTH_PLUGIN``
  Authentication plugin, default to ``env[OS_AUTH_PLUGIN]``

``--os-auth-url AUTH_URL``
  Defaults to ``env[OS_AUTH_URL]``

``--os-project-id PROJECT_ID``
  Defaults to ``env[OS_PROJECT_ID]``.

``--os-project-name PROJECT_NAME``
  Defaults to ``env[OS_PROJECT_NAME]``.

``--os-tenant-id TENANT_ID``
  Defaults to ``env[OS_TENANT_ID]``.

``--os-tenant-name TENANT_NAME``
  Defaults to ``env[OS_TENANT_NAME]``.

``--os-domain-id DOMAIN_ID``
  Domain ID for scope of authorization, defaults to
  ``env[OS_DOMAIN_ID]``.

``--os-domain-name DOMAIN_NAME``
  Domain name for scope of authorization, defaults to
  ``env[OS_DOMAIN_NAME]``.

``--os-project-domain-id PROJECT_DOMAIN_ID``
  Project domain ID for scope of authorization, defaults
  to ``env[OS_PROJECT_DOMAIN_ID]``.

``--os-project-domain-name PROJECT_DOMAIN_NAME``
  Project domain name for scope of authorization,
  defaults to ``env[OS_PROJECT_DOMAIN_NAME]``.

``--os-user-domain-id USER_DOMAIN_ID``
  User domain ID for scope of authorization, defaults to
  ``env[OS_USER_DOMAIN_ID]``.

``--os-user-domain-name USER_DOMAIN_NAME``
  User domain name for scope of authorization, defaults
  to ``env[OS_USER_DOMAIN_NAME]``.

``--os-username USERNAME``
  Defaults to ``env[OS_USERNAME]``.

``--os-user-id USER_ID``
  Defaults to ``env[OS_USER_ID]``.

``--os-password PASSWORD``
  Defaults to ``env[OS_PASSWORD]``

``--os-trust-id TRUST_ID``
  Defaults to ``env[OS_TRUST_ID]``

``--os-cacert CA_BUNDLE_FILE``
  Path of CA TLS certificate(s) used to verify the
  remote server's certificate. Without this option
  senlin looks for the default system CA certificates.

``--verify``
  Verify server certificate (default)

``--insecure``
  Explicitly allow senlinclient to perform "insecure
  SSL" (HTTPS) requests. The server's certificate will
  not be verified against any certificate authorities.
  This option should be used with caution.

``--os-token TOKEN``
  A string token to bootstrap the Keystone database,
  defaults to ``env[OS_TOKEN]``

``--os-access-info ACCESS_INFO``
  Access info, defaults to ``env[OS_ACCESS_INFO]``

``--os-api-name <service>=<name>``
  Desired API names, defaults to ``env[OS_API_NAME]``

``--os-api-region <service>=<region>``
  Desired API region, defaults to ``env[OS_API_REGION]``

``--os-api-version <service>=<version>``
  Desired API versions, defaults to ``env[OS_API_VERSION]``

``--os-api-interface <service>=<interface>``
  Desired API interface, defaults to ``env[OS_INTERFACE]``

.. _senlin_action-list:

senlin action-list
~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin action-list [-f <KEY1=VALUE1;KEY2=VALUE2...>] [-k <KEYS>]
                             [-s <DIR>] [-l <LIMIT>] [-m <ID>] [-F]

List actions.

Optional arguments
------------------

``-f <KEY1=VALUE1;KEY2=VALUE2...>, --filters <KEY1=VALUE1;KEY2=VALUE2...>``
  Filter parameters to apply on returned actions. This
  can be specified multiple times, or once with
  parameters separated by a semicolon.

``-k <KEYS>, --sort-keys <KEYS>``
  Name of keys used for sorting the returned actions.

``-s <DIR>, --sort-dir <DIR>``
  Direction for sorting, where DIR can be "asc" or
  "desc".

``-l <LIMIT>, --limit <LIMIT>``
  Limit the number of actions returned.

``-m <ID>, --marker <ID>``
  Only return actions that appear after the given node
  ID.

``-F, --full-id``
  Print full IDs in list.

.. _senlin_action-show:

senlin action-show
~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin action-show <ACTION>

Show detailed info about the specified action.

Positional arguments
--------------------

``<ACTION>``
  Name or ID of the action to show the details for.

.. _senlin_build-info:

senlin build-info
~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin build-info

Retrieve build information. :param sc: Instance of senlinclient. :param args:
Additional command line arguments, if any.

.. _senlin_cluster-create:

senlin cluster-create
~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin cluster-create -p <PROFILE> [-n <MIN-SIZE>] [-m <MAX-SIZE>]
                                [-c <DESIRED-CAPACITY>] [-o <PARENT_ID>]
                                [-t <TIMEOUT>] [-M <KEY1=VALUE1;KEY2=VALUE2...>]
                                <CLUSTER_NAME>

Create the cluster.

Positional arguments
--------------------

``<CLUSTER_NAME>``
  Name of the cluster to create.

Optional arguments
------------------

``-p <PROFILE>, --profile <PROFILE>``
  Profile Id used for this cluster.

``-n <MIN-SIZE>, --min-size <MIN-SIZE>``
  Min size of the cluster. Default to 0.

``-m <MAX-SIZE>, --max-size <MAX-SIZE>``
  Max size of the cluster. Default to -1, means
  unlimited.

``-c <DESIRED-CAPACITY>, --desired-capacity <DESIRED-CAPACITY>``
  Desired capacity of the cluster. Default to min_size
  if min_size is specified else 0.

``-o <PARENT_ID>, --parent <PARENT_ID>``
  ID of the parent cluster, if exists.

``-t <TIMEOUT>, --timeout <TIMEOUT>``
  Cluster creation timeout in seconds.

``-M <KEY1=VALUE1;KEY2=VALUE2...>, --metadata <KEY1=VALUE1;KEY2=VALUE2...>``
  Metadata values to be attached to the cluster. This
  can be specified multiple times, or once with key-
  value pairs separated by a semicolon.

.. _senlin_cluster-delete:

senlin cluster-delete
~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin cluster-delete <CLUSTER> [<CLUSTER> ...]

Delete the cluster(s).

Positional arguments
--------------------

``<CLUSTER>``
  Name or ID of cluster(s) to delete.

.. _senlin_cluster-list:

senlin cluster-list
~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin cluster-list [-n] [-f <KEY1=VALUE1;KEY2=VALUE2...>] [-k <KEYS>]
                              [-s <DIR>] [-l <LIMIT>] [-m <ID>] [-g] [-F]

List the user's clusters.

Optional arguments
------------------

``-n, --show-nested``
  Include nested clusters if any.

``-f <KEY1=VALUE1;KEY2=VALUE2...>, --filters <KEY1=VALUE1;KEY2=VALUE2...>``
  Filter parameters to apply on returned clusters. This
  can be specified multiple times, or once with
  parameters separated by a semicolon.

``-k <KEYS>, --sort-keys <KEYS>``
  Name of keys used for sorting the returned clusters.

``-s <DIR>, --sort-dir <DIR>``
  Direction for sorting, where DIR can be "asc" or
  "desc".

``-l <LIMIT>, --limit <LIMIT>``
  Limit the number of clusters returned.

``-m <ID>, --marker <ID>``
  Only return clusters that appear after the given
  cluster ID.

``-g, --global-project``
  Indicate that the cluster list should include clusters
  from all projects. This option is subject to access
  policy checking. Default is False.

``-F, --full-id``
  Print full IDs in list.

.. _senlin_cluster-node-add:

senlin cluster-node-add
~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin cluster-node-add -n <NODES> <CLUSTER>

Add specified nodes to cluster.

Positional arguments
--------------------

``<CLUSTER>``
  Name or ID of cluster to operate on.

Optional arguments
------------------

``-n <NODES>, --nodes <NODES>``
  ID of nodes to be added; multiple nodes can be
  separated with ","

.. _senlin_cluster-node-del:

senlin cluster-node-del
~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin cluster-node-del -n <NODES> <CLUSTER>

Delete specified nodes from cluster.

Positional arguments
--------------------

``<CLUSTER>``
  Name or ID of cluster to operate on.

Optional arguments
------------------

``-n <NODES>, --nodes <NODES>``
  ID of nodes to be deleted; multiple nodes can be
  separated with ",".

.. _senlin_cluster-node-list:

senlin cluster-node-list
~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin cluster-node-list [-f <KEY1=VALUE1;KEY2=VALUE2...>] [-l <LIMIT>]
                                   [-m <ID>] [-F]
                                   <CLUSTER>

List nodes from cluster.

Positional arguments
--------------------

``<CLUSTER>``
  Name or ID of cluster to nodes from.

Optional arguments
------------------

``-f <KEY1=VALUE1;KEY2=VALUE2...>, --filters <KEY1=VALUE1;KEY2=VALUE2...>``
  Filter parameters to apply on returned nodes. This can
  be specified multiple times, or once with parameters
  separated by a semicolon.

``-l <LIMIT>, --limit <LIMIT>``
  Limit the number of nodes returned.

``-m <ID>, --marker <ID>``
  Only return nodes that appear after the given node ID.

``-F, --full-id``
  Print full IDs in list.

.. _senlin_cluster-policy-attach:

senlin cluster-policy-attach
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin cluster-policy-attach -p <POLICY> [-r <PRIORITY>] [-l <LEVEL>]
                                       [-c <SECONDS>] [-e]
                                       <NAME or ID>

Attach policy to cluster.

Positional arguments
--------------------

``<NAME or ID>``
  Name or ID of cluster to operate on.

Optional arguments
------------------

``-p <POLICY>, --policy <POLICY>``
  ID or name of policy to be attached.

``-r <PRIORITY>, --priority <PRIORITY>``
  An integer specifying the relative priority among all
  policies attached to a cluster. The lower the value,
  the higher the priority. Default is 50.

``-l <LEVEL>, --enforcement-level <LEVEL>``
  An integer between 0 and 100 representing the
  enforcement level. Default to enforcement level of
  policy.

``-c <SECONDS>, --cooldown <SECONDS>``
  An integer indicating the cooldown seconds once the
  policy is effected. Default to cooldown of policy.

``-e, --enabled``
  Whether the policy should be enabled once attached.
  Default to enabled.

.. _senlin_cluster-policy-detach:

senlin cluster-policy-detach
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin cluster-policy-detach -p <POLICY> <NAME or ID>

Detach policy from cluster.

Positional arguments
--------------------

``<NAME or ID>``
  Name or ID of cluster to operate on.

Optional arguments
------------------

``-p <POLICY>, --policy <POLICY>``
  ID or name of policy to be detached.

.. _senlin_cluster-policy-disable:

senlin cluster-policy-disable
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin cluster-policy-disable -p <POLICY> <NAME or ID>

Disable a policy on a cluster.

Positional arguments
--------------------

``<NAME or ID>``
  Name or ID of cluster to operate on.

Optional arguments
------------------

``-p <POLICY>, --policy <POLICY>``
  ID or name of policy to be disabled.

.. _senlin_cluster-policy-enable:

senlin cluster-policy-enable
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin cluster-policy-enable -p <POLICY> <NAME or ID>

Enable a policy on a cluster.

Positional arguments
--------------------

``<NAME or ID>``
  Name or ID of cluster to operate on.

Optional arguments
------------------

``-p <POLICY>, --policy <POLICY>``
  ID or name of policy to be enabled.

.. _senlin_cluster-policy-list:

senlin cluster-policy-list
~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin cluster-policy-list [-f <KEY1=VALUE1;KEY2=VALUE2...>]
                                     [-k <KEYS>] [-s <DIR>] [-F]
                                     <CLUSTER>

List policies from cluster.

Positional arguments
--------------------

``<CLUSTER>``
  Name or ID of cluster to query on.

Optional arguments
------------------

``-f <KEY1=VALUE1;KEY2=VALUE2...>, --filters <KEY1=VALUE1;KEY2=VALUE2...>``
  Filter parameters to apply on returned results. This
  can be specified multiple times, or once with
  parameters separated by a semicolon.

``-k <KEYS>, --sort-keys <KEYS>``
  Name of keys used for sorting the returned policies.

``-s <DIR>, --sort-dir <DIR>``
  Direction for sorting, where DIR can be "asc" or
  "desc".

``-F, --full-id``
  Print full IDs in list.

.. _senlin_cluster-policy-show:

senlin cluster-policy-show
~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin cluster-policy-show -p <POLICY> <CLUSTER>

Show a specific policy that is bound to the specified cluster.

Positional arguments
--------------------

``<CLUSTER>``
  ID or name of the cluster to query on.

Optional arguments
------------------

``-p <POLICY>, --policy <POLICY>``
  ID or name of the policy to query on.

.. _senlin_cluster-policy-update:

senlin cluster-policy-update
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin cluster-policy-update -p <POLICY> [-r <PRIORITY>] [-l <LEVEL>]
                                       [-c <COOLDOWN>] [-e <BOOLEAN>]
                                       <NAME or ID>

Update a policy's properties on a cluster.

Positional arguments
--------------------

``<NAME or ID>``
  Name or ID of cluster to operate on.

Optional arguments
------------------

``-p <POLICY>, --policy <POLICY>``
  ID or name of policy to be updated.

``-r <PRIORITY>, --priority <PRIORITY>``
  An integer specifying the relative priority among all
  policies attached to a cluster. The lower the value,
  the higher the priority. Default is 50.

``-l <LEVEL>, --enforcement-level <LEVEL>``
  New enforcement level.

``-c <COOLDOWN>, --cooldown <COOLDOWN>``
  Cooldown interval in seconds.

``-e <BOOLEAN>, --enabled <BOOLEAN>``
  Whether the policy should be enabled.

.. _senlin_cluster-resize:

senlin cluster-resize
~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin cluster-resize [-c <CAPACITY>] [-a <ADJUSTMENT>]
                                [-p <PERCENTAGE>] [-t <MIN_STEP>] [-s] [-n MIN]
                                [-m MAX]
                                <CLUSTER>

Resize a cluster.

Positional arguments
--------------------

``<CLUSTER>``
  Name or ID of cluster to operate on.

Optional arguments
------------------

``-c <CAPACITY>, --capacity <CAPACITY>``
  The desired number of nodes of the cluster.

``-a <ADJUSTMENT>, --adjustment <ADJUSTMENT>``
  A positive integer meaning the number of nodes to add,
  or a negative integer indicating the number of nodes
  to remove.

``-p <PERCENTAGE>, --percentage <PERCENTAGE>``
  A value that is interpreted as the percentage of size
  adjustment. This value can be positive or negative.

``-t <MIN_STEP>, --min-step <MIN_STEP>``
  An integer specifying the number of nodes for
  adjustment when <PERCENTAGE> is specified.

``-s, --strict A``
  boolean specifying whether the resize should be
  performed on a best-effort basis when the new capacity
  may go beyond size constraints.

``-n MIN, --min-size MIN``
  New lower bound of cluster size.

``-m MAX, --max-size MAX``
  New upper bound of cluster size. A value of -1
  indicates no upper limit on cluster size.

.. _senlin_cluster-scale-in:

senlin cluster-scale-in
~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin cluster-scale-in [-c <COUNT>] <CLUSTER>

Scale in a cluster by the specified number of nodes.

Positional arguments
--------------------

``<CLUSTER>``
  Name or ID of cluster to operate on.

Optional arguments
------------------

``-c <COUNT>, --count <COUNT>``
  Number of nodes to be deleted from the specified
  cluster.

.. _senlin_cluster-scale-out:

senlin cluster-scale-out
~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin cluster-scale-out [-c <COUNT>] <CLUSTER>

Scale out a cluster by the specified number of nodes.

Positional arguments
--------------------

``<CLUSTER>``
  Name or ID of cluster to operate on.

Optional arguments
------------------

``-c <COUNT>, --count <COUNT>``
  Number of nodes to be added to the specified cluster.

.. _senlin_cluster-show:

senlin cluster-show
~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin cluster-show <CLUSTER>

Show details of the cluster.

Positional arguments
--------------------

``<CLUSTER>``
  Name or ID of cluster to show.

.. _senlin_cluster-update:

senlin cluster-update
~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin cluster-update [-p <PROFILE>] [-t <TIMEOUT>] [-r <PARENT>]
                                [-M <KEY1=VALUE1;KEY2=VALUE2...>] [-n <NAME>]
                                <CLUSTER>

Update the cluster.

Positional arguments
--------------------

``<CLUSTER>``
  Name or ID of cluster to be updated.

Optional arguments
------------------

``-p <PROFILE>, --profile <PROFILE>``
  ID of new profile to use.

``-t <TIMEOUT>, --timeout <TIMEOUT>``
  New timeout (in seconds) value for the cluster.

``-r <PARENT>, --parent <PARENT>``
  ID of parent cluster for the cluster.

``-M <KEY1=VALUE1;KEY2=VALUE2...>, --metadata <KEY1=VALUE1;KEY2=VALUE2...>``
  Metadata values to be attached to the cluster. This
  can be specified multiple times, or once with key-
  value pairs separated by a semicolon.

``-n <NAME>, --name <NAME>``
  New name for the cluster to update.

.. _senlin_event-list:

senlin event-list
~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin event-list [-f <KEY1=VALUE1;KEY2=VALUE2...>] [-l <LIMIT>]
                            [-m <ID>] [-k <KEYS>] [-s <DIR>] [-g] [-F]

List events.

Optional arguments
------------------

``-f <KEY1=VALUE1;KEY2=VALUE2...>, --filters <KEY1=VALUE1;KEY2=VALUE2...>``
  Filter parameters to apply on returned events. This
  can be specified multiple times, or once with
  parameters separated by a semicolon.

``-l <LIMIT>, --limit <LIMIT>``
  Limit the number of events returned.

``-m <ID>, --marker <ID>``
  Only return events that appear after the given event
  ID.

``-k <KEYS>, --sort-keys <KEYS>``
  Name of keys used for sorting the returned events.

``-s <DIR>, --sort-dir <DIR>``
  Direction for sorting, where DIR can be "asc" or
  "desc".

``-g, --global-project``
  Whether events from all projects should be listed.
  Default to False. Setting this to True may demand for
  an admin privilege.

``-F, --full-id``
  Print full IDs in list.

.. _senlin_event-show:

senlin event-show
~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin event-show <EVENT>

Describe the event.

Positional arguments
--------------------

``<EVENT>``
  ID of event to display details for.

.. _senlin_node-create:

senlin node-create
~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin node-create -p <PROFILE> [-c <CLUSTER>] [-r <ROLE>]
                             [-M <KEY1=VALUE1;KEY2=VALUE2...>]
                             <NODE_NAME>

Create the node.

Positional arguments
--------------------

``<NODE_NAME>``
  Name of the node to create.

Optional arguments
------------------

``-p <PROFILE>, --profile <PROFILE>``
  Profile Id used for this node.

``-c <CLUSTER>, --cluster <CLUSTER>``
  Cluster Id for this node.

``-r <ROLE>, --role <ROLE>``
  Role for this node in the specific cluster.

``-M <KEY1=VALUE1;KEY2=VALUE2...>, --metadata <KEY1=VALUE1;KEY2=VALUE2...>``
  Metadata values to be attached to the node. This can
  be specified multiple times, or once with key-value
  pairs separated by a semicolon.

.. _senlin_node-delete:

senlin node-delete
~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin node-delete <NODE> [<NODE> ...]

Delete the node(s).

Positional arguments
--------------------

``<NODE>``
  Name or ID of node(s) to delete.

.. _senlin_node-join:

senlin node-join
~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin node-join -c CLUSTER <NODE>

Make node join the specified cluster.

Positional arguments
--------------------

``<NODE>``
  Name or ID of node to operate on.

Optional arguments
------------------

``-c CLUSTER, --cluster CLUSTER``
  ID or name of cluster for node to join.

.. _senlin_node-leave:

senlin node-leave
~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin node-leave <NODE>

Make node leave its current cluster.

Positional arguments
--------------------

``<NODE>``
  Name or ID of node to operate on.

.. _senlin_node-list:

senlin node-list
~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin node-list [-c <CLUSTER>] [-f <KEY1=VALUE1;KEY2=VALUE2...>]
                           [-k <KEYS>] [-s <DIR>] [-l <LIMIT>] [-m <ID>] [-g]
                           [-F]

Show list of nodes.

Optional arguments
------------------

``-c <CLUSTER>, --cluster <CLUSTER>``
  ID or name of cluster from which nodes are to be
  listed.

``-f <KEY1=VALUE1;KEY2=VALUE2...>, --filters <KEY1=VALUE1;KEY2=VALUE2...>``
  Filter parameters to apply on returned nodes. This can
  be specified multiple times, or once with parameters
  separated by a semicolon.

``-k <KEYS>, --sort-keys <KEYS>``
  Name of keys used for sorting the returned nodes.

``-s <DIR>, --sort-dir <DIR>``
  Direction for sorting, where DIR can be "asc" or
  "desc".

``-l <LIMIT>, --limit <LIMIT>``
  Limit the number of nodes returned.

``-m <ID>, --marker <ID>``
  Only return nodes that appear after the given node ID.

``-g, --global-project``
  Indicate that this node list should include nodes from
  all projects. This option is subject to access policy
  checking. Default is False.

``-F, --full-id``
  Print full IDs in list.

.. _senlin_node-show:

senlin node-show
~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin node-show [-D] <NODE>

Show detailed info about the specified node.

Positional arguments
--------------------

``<NODE>``
  Name or ID of the node to show the details for.

Optional arguments
------------------

``-D, --details``
  Include physical object details.

.. _senlin_node-update:

senlin node-update
~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin node-update [-n <NAME>] [-p <PROFILE ID>] [-r <ROLE>]
                             [-M <KEY1=VALUE1;KEY2=VALUE2...>]
                             <NODE>

Update the node.

Positional arguments
--------------------

``<NODE>``
  Name or ID of node to update.

Optional arguments
------------------

``-n <NAME>, --name <NAME>``
  New name for the node.

``-p <PROFILE ID>, --profile <PROFILE ID>``
  ID of new profile to use.

``-r <ROLE>, --role <ROLE>``
  Role for this node in the specific cluster.

``-M <KEY1=VALUE1;KEY2=VALUE2...>, --metadata <KEY1=VALUE1;KEY2=VALUE2...>``
  Metadata values to be attached to the node. Metadata
  can be specified multiple times, or once with key-
  value pairs separated by a semicolon.

.. _senlin_policy-create:

senlin policy-create
~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin policy-create -s <SPEC_FILE> [-c <SECONDS>] [-l <LEVEL>] <NAME>

Create a policy.

Positional arguments
--------------------

``<NAME>``
  Name of the policy to create.

Optional arguments
------------------

``-s <SPEC_FILE>, --spec-file <SPEC_FILE>``
  The spec file used to create the policy.

``-c <SECONDS>, --cooldown <SECONDS>``
  An integer indicating the cooldown seconds once the
  policy is effected. Default to 0.

``-l <LEVEL>, --enforcement-level <LEVEL>``
  An integer between 0 and 100 representing the
  enforcement level. Default to 0.

.. _senlin_policy-delete:

senlin policy-delete
~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin policy-delete <POLICY> [<POLICY> ...]

Delete policy(s).

Positional arguments
--------------------

``<POLICY>``
  Name or ID of policy(s) to delete.

.. _senlin_policy-list:

senlin policy-list
~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin policy-list [-l <LIMIT>] [-m <ID>] [-F]

List policies that meet the criteria.

Optional arguments
------------------

``-l <LIMIT>, --limit <LIMIT>``
  Limit the number of policies returned.

``-m <ID>, --marker <ID>``
  Only return policies that appear after the given ID.

``-F, --full-id``
  Print full IDs in list.

.. _senlin_policy-show:

senlin policy-show
~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin policy-show <POLICY>

Show the policy details.

Positional arguments
--------------------

``<POLICY>``
  Name of the policy to be updated.

.. _senlin_policy-type-list:

senlin policy-type-list
~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin policy-type-list

List the available policy types.

.. _senlin_policy-type-show:

senlin policy-type-show
~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin policy-type-show [-F <FORMAT>] <TYPE_NAME>

Get the details about a policy type.

Positional arguments
--------------------

``<TYPE_NAME>``
  Policy type to retrieve.

Optional arguments
------------------

``-F <FORMAT>, --format <FORMAT>``
  The template output format, one of: yaml, json.

.. _senlin_policy-update:

senlin policy-update
~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin policy-update [-c <SECONDS>] [-l <LEVEL>] [-n <NAME>] <POLICY>

Update a policy.

Positional arguments
--------------------

``<POLICY>``
  Name of the policy to be updated.

Optional arguments
------------------

``-c <SECONDS>, --cooldown <SECONDS>``
  An integer indicating the cooldown seconds once the
  policy is effected. Default to 0.

``-l <LEVEL>, --enforcement-level <LEVEL>``
  An integer between 0 and 100 representing the
  enforcement level. Default to 0.

``-n <NAME>, --name <NAME>``
  New name of the policy to be updated.

.. _senlin_profile-create:

senlin profile-create
~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin profile-create -s <SPEC FILE> [-p <PERMISSION>]
                                [-M <KEY1=VALUE1;KEY2=VALUE2...>]
                                <PROFILE_NAME>

Create a profile.

Positional arguments
--------------------

``<PROFILE_NAME>``
  Name of the profile to create.

Optional arguments
------------------

``-s <SPEC FILE>, --spec-file <SPEC FILE>``
  The spec file used to create the profile.

``-p <PERMISSION>, --permission <PERMISSION>``
  A string format permission for this profile.

``-M <KEY1=VALUE1;KEY2=VALUE2...>, --metadata <KEY1=VALUE1;KEY2=VALUE2...>``
  Metadata values to be attached to the profile. This
  can be specified multiple times, or once with key-
  value pairs separated by a semicolon.

.. _senlin_profile-delete:

senlin profile-delete
~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin profile-delete <PROFILE> [<PROFILE> ...]

Delete profile(s).

Positional arguments
--------------------

``<PROFILE>``
  Name or ID of profile(s) to delete.

.. _senlin_profile-list:

senlin profile-list
~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin profile-list [-l <LIMIT>] [-m <ID>] [-F]

List profiles that meet the criteria.

Optional arguments
------------------

``-l <LIMIT>, --limit <LIMIT>``
  Limit the number of profiles returned.

``-m <ID>, --marker <ID>``
  Only return profiles that appear after the given ID.

``-F, --full-id``
  Print full IDs in list.

.. _senlin_profile-show:

senlin profile-show
~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin profile-show <PROFILE>

Show the profile details.

Positional arguments
--------------------

``<PROFILE>``
  Name or ID of profile to show.

.. _senlin_profile-type-list:

senlin profile-type-list
~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin profile-type-list

List the available profile types. :param sc: Instance of senlinclient. :param
args: Additional command line arguments, if any.

.. _senlin_profile-type-show:

senlin profile-type-show
~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin profile-type-show [-F <FORMAT>] <TYPE_NAME>

Get the details about a profile type.

Positional arguments
--------------------

``<TYPE_NAME>``
  Profile type to retrieve.

Optional arguments
------------------

``-F <FORMAT>, --format <FORMAT>``
  The template output format, one of: yaml, json.

.. _senlin_profile-update:

senlin profile-update
~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin profile-update [-n <NAME>] [-p <PERMISSION>]
                                [-M <KEY1=VALUE1;KEY2=VALUE2...>]
                                <PROFILE_ID>

Update a profile.

Positional arguments
--------------------

``<PROFILE_ID>``
  Name or ID of the profile to update.

Optional arguments
------------------

``-n <NAME>, --name <NAME>``
  The new name for the profile.

``-p <PERMISSION>, --permission <PERMISSION>``
  A string format permission for this profile.

``-M <KEY1=VALUE1;KEY2=VALUE2...>, --metadata <KEY1=VALUE1;KEY2=VALUE2...>``
  Metadata values to be attached to the profile. This
  can be specified multiple times, or once with key-
  value pairs separated by a semicolon.

.. _senlin_receiver-create:

senlin receiver-create
~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin receiver-create [-t <TYPE>] [-c <CLUSTER>] -a <ACTION>
                                 [-P <KEY1=VALUE1;KEY2=VALUE2...>]
                                 <NAME>

Create a receiver.

Positional arguments
--------------------

``<NAME>``
  Name of the receiver to create.

Optional arguments
------------------

``-t <TYPE>, --type <TYPE>``
  Type of the receiver to create.

``-c <CLUSTER>, --cluster <CLUSTER>``
  Targeted cluster for this receiver.

``-a <ACTION>, --action <ACTION>``
  Name or ID of the targeted action to be triggered.

``-P <KEY1=VALUE1;KEY2=VALUE2...>, --params <KEY1=VALUE1;KEY2=VALUE2...>``
  A dictionary of parameters that will be passed to
  target action when the receiver is triggered.

.. _senlin_receiver-delete:

senlin receiver-delete
~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin receiver-delete <RECEIVER> [<RECEIVER> ...]

Delete receiver(s).

Positional arguments
--------------------

``<RECEIVER>``
  Name or ID of receiver(s) to delete.

.. _senlin_receiver-list:

senlin receiver-list
~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin receiver-list [-f <KEY1=VALUE1;KEY2=VALUE2...>] [-l <LIMIT>]
                               [-m <ID>] [-k <KEYS>] [-s <DIR>] [-g] [-F]

List receivers that meet the criteria.

Optional arguments
------------------

``-f <KEY1=VALUE1;KEY2=VALUE2...>, --filters <KEY1=VALUE1;KEY2=VALUE2...>``
  Filter parameters to apply on returned receivers. This
  can be specified multiple times, or once with
  parameters separated by a semicolon.

``-l <LIMIT>, --limit <LIMIT>``
  Limit the number of receivers returned.

``-m <ID>, --marker <ID>``
  Only return receivers that appear after the given ID.

``-k <KEYS>, --sort-keys <KEYS>``
  Name of keys used for sorting the returned receivers.

``-s <DIR>, --sort-dir <DIR>``
  Direction for sorting, where DIR can be "asc" or
  "desc".

``-g, --global-project``
  Indicate that the list should include receivers from
  all projects. This option is subject to access policy
  checking. Default is False.

``-F, --full-id``
  Print full IDs in list.

.. _senlin_receiver-show:

senlin receiver-show
~~~~~~~~~~~~~~~~~~~~

.. code-block:: console

   usage: senlin receiver-show <RECEIVER>

Show the receiver details.

Positional arguments
--------------------

``<RECEIVER>``
  Name or ID of the receiver to show.

