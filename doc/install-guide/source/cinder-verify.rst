.. _cinder-verify:

Verify operation
~~~~~~~~~~~~~~~~

Verify operation of the Block Storage service.

.. note::

   Perform these commands on the controller node.

#. Source the ``admin`` credentials to gain access to
   admin-only CLI commands:

   .. code-block:: console

      $ source admin-openrc.sh

#. List service components to verify successful launch of each process:

   .. code-block:: console

      $ cinder service-list
      +------------------+------------+------+---------+-------+----------------------------+-----------------+
      |      Binary      |    Host    | Zone |  Status | State |         Updated_at         | Disabled Reason |
      +------------------+------------+------+---------+-------+----------------------------+-----------------+
      | cinder-scheduler | controller | nova | enabled |   up  | 2014-10-18T01:30:54.000000 |       None      |
      | cinder-volume    | block1@lvm | nova | enabled |   up  | 2014-10-18T01:30:57.000000 |       None      |
      +------------------+------------+------+---------+-------+----------------------------+-----------------+
