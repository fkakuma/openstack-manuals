.. _shared_file_systems_key_concepts:

============
Key concepts
============

Share
~~~~~

In the Shared File Systems service ``share`` is the fundamental resource unit
allocated by the Shared File System service. It represents an allocation of a
persistent, readable, and writable filesystem. Compute instances access these
filesystems. Depending on the deployment configuration, clients outside of
OpenStack can also access the filesystem.

.. note::

   A ``share`` is an abstract storage object that may or may not directly
   map to a "share" concept from the underlying storage provider.


Snapshot
~~~~~~~~

A ``snapshot`` is a point-in-time, read-only copy of a ``share``. You can
create ``Snapshots`` from an existing, operational ``share`` regardless
of whether a client has mounted the file system. A ``snapshot``
can serve as the content source for a new ``share`` when the ``share``
is created with the create from snapshot option specified.

Storage Pools
~~~~~~~~~~~~~

With the Kilo release of OpenStack, Shared File Systems can use
``storage pools``. The storage may present one or more logical storage
resource pools from which the Shared File Systems service
will select as a storage location when provisioning ``shares``.

Share Type
~~~~~~~~~~

``Share type`` is an abstract collection of criteria used to characterize
``shares``. They are most commonly used to create a hierarchy of functional
capabilities. This hierarchy represents tiered storage services levels. For
example, a cloud administrator might define a premium ``share type`` that
indicates a greater level of performance than a basic ``share type``.
Premium represents the best performance level.


Share Access Rules
~~~~~~~~~~~~~~~~~~

``Share access rules`` define which users can access a particular ``share``.
For example, cloud administrators can declare rules for NFS shares by
listing the valid IP networks which will access the ``share``. List the
IP networks in CIDR notation.

Security Services
~~~~~~~~~~~~~~~~~

``Security services``allow granular client access rules for cloud
administrators. They can declare rules for authentication or
authorization to access ``share`` content. External services including LDAP,
Active Directory, Kerberos can be declared as resources. Examine and consult
these resources when making an access decision for a particular ``share``.
You can associate ``Shares`` with multiple security services, but only one
service per one type.

Share Networks
~~~~~~~~~~~~~~

A ``share network`` is an object that defines a relationship between a
tenant's network and subnet, as defined in an OpenStack Networking service or
Compute service. The ``share network`` is also defined in ``shares``
created by the same tenant. A tenant may find it desirable to
provision ``shares`` such that only instances connected to a particular
OpenStack-defined network have access to the ``share``. Also,
``security services`` can be attached to ``share networks``,
because most of auth protocols require some interaction with network services.

The Shared File Systems service has the ability to work outside of OpenStack.
That is due to the ``StandaloneNetworkPlugin``. The plugin is compatible with
any network platform, and does not require specific network services in
OpenStack like Compute or Networking service. You can set the network
parameters in the ``manila.conf`` file.

Share Servers
~~~~~~~~~~~~~

A ``share server`` is a logical entity that hosts the shares created
on a specific ``share network``. A ``share server`` may be a
configuration object within the storage controller, or it may represent
logical resources provisioned within an OpenStack deployment used to
support the data path used to access ``shares``.

``Share servers`` interact with network services to determine the appropriate
IP addresses on which to export ``shares`` according to the related ``share
network``. The Shared File Systems service has a pluggable network model that
allows ``share servers`` to work with different implementations of
the Networking service.
