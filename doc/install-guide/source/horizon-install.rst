Install and configure
~~~~~~~~~~~~~~~~~~~~~

This section describes how to install and configure the dashboard
on the controller node.

The dashboard relies on functional core services including
Identity, Image service, Compute, and either Networking (neutron)
or legacy networking (nova-network). Environments with
stand-alone services such as Object Storage cannot use the
dashboard. For more information, see the
`developer documentation <http://docs.openstack.org/developer/
horizon/topics/deployment.html>`__.

.. note::

   This section assumes proper installation, configuration, and operation
   of the Identity service using the Apache HTTP server and Memcached
   service as described in the :ref:`Install and configure the Identity
   service <keystone-install>` section.

Install and configure components
--------------------------------

.. only:: obs or rdo or ubuntu

   .. include:: shared/note_configuration_vary_by_distribution.rst

.. only:: obs

   1. Install the packages:

      .. code-block:: console

         # zypper install openstack-dashboard

.. only:: rdo

   1. Install the packages:

      .. code-block:: console

         # yum install openstack-dashboard

.. only:: ubuntu

   1. Install the packages:

      .. code-block:: console

         # apt-get install openstack-dashboard

.. only:: debian

   1. Install the packages:

      .. code-block:: console

         # apt-get install openstack-dashboard-apache

   2. Respond to prompts for web server configuration.

      .. note::

         The automatic configuration process generates a self-signed
         SSL certificate. Consider obtaining an official certificate
         for production environments.

      .. note::

         There are two modes of installation. One using ``/horizon`` as the URL,
         keeping your default vhost and only adding an Alias directive: this is
         the default. The other mode will remove the default Apache vhost and install
         the dashboard on the webroot. It was the only available option
         before the Liberty release. If you prefer to set the Apache configuration
         manually,  install the ``openstack-dashboard`` package instead of
         ``openstack-dashboard-apache``.

.. only:: obs

   2. Configure the web server:

      .. code-block:: console

         # cp /etc/apache2/conf.d/openstack-dashboard.conf.sample \
           /etc/apache2/conf.d/openstack-dashboard.conf
         # a2enmod rewrite;a2enmod ssl;a2enmod wsgi

   3. Edit the
      ``/srv/www/openstack-dashboard/openstack_dashboard/local/local_settings.py``
      file and complete the following actions:

      * Configure the dashboard to use OpenStack services on the
        ``controller`` node:

        .. code-block:: ini

           OPENSTACK_HOST = "controller"

      * Allow all hosts to access the dashboard:

        .. code-block:: ini

           ALLOWED_HOSTS = ['*', ]

      * Configure the ``memcached`` session storage service:

        .. code-block:: ini

           CACHES = {
               'default': {
                    'BACKEND': 'django.core.cache.backends.memcached.MemcachedCache',
                    'LOCATION': '127.0.0.1:11211',
               }
           }

        .. note::

           Comment out any other session storage configuration.

      * Configure ``user`` as the default role for
        users that you create via the dashboard:

        .. code-block:: ini

           OPENSTACK_KEYSTONE_DEFAULT_ROLE = "user"

      * Optionally, configure the time zone:

        .. code-block:: ini

           TIME_ZONE = "TIME_ZONE"

        Replace ``TIME_ZONE`` with an appropriate time zone identifier.
        For more information, see the `list of time zones
        <http://en.wikipedia.org/wiki/List_of_tz_database_time_zones>`__.

.. only:: rdo

   2. Edit the
      ``/etc/openstack-dashboard/local_settings``
      file and complete the following actions:

      * Configure the dashboard to use OpenStack services on the
        ``controller`` node:

        .. code-block:: ini

           OPENSTACK_HOST = "controller"

      * Allow all hosts to access the dashboard:

        .. code-block:: ini

           ALLOWED_HOSTS = ['*', ]

      * Configure the ``memcached`` session storage service:

        .. code-block:: ini

           CACHES = {
               'default': {
                    'BACKEND': 'django.core.cache.backends.memcached.MemcachedCache',
                    'LOCATION': '127.0.0.1:11211',
               }
           }

        .. note::

           Comment out any other session storage configuration.

      * Configure ``user`` as the default role for
        users that you create via the dashboard:

        .. code-block:: ini

           OPENSTACK_KEYSTONE_DEFAULT_ROLE = "user"

      * Optionally, configure the time zone:

        .. code-block:: ini

           TIME_ZONE = "TIME_ZONE"

        Replace ``TIME_ZONE`` with an appropriate time zone identifier.
        For more information, see the `list of time zones
        <http://en.wikipedia.org/wiki/List_of_tz_database_time_zones>`__.

.. only:: ubuntu

   2. Edit the
      ``/etc/openstack-dashboard/local_settings.py``
      file and complete the following actions:

      * Configure the dashboard to use OpenStack services on the
        ``controller`` node:

        .. code-block:: ini

           OPENSTACK_HOST = "controller"

      * Allow all hosts to access the dashboard:

        .. code-block:: ini

           ALLOWED_HOSTS = ['*', ]

      * Configure the ``memcached`` session storage service:

        .. code-block:: ini

           CACHES = {
               'default': {
                    'BACKEND': 'django.core.cache.backends.memcached.MemcachedCache',
                    'LOCATION': '127.0.0.1:11211',
               }
           }

        .. note::

           Comment out any other session storage configuration.

      * Configure ``user`` as the default role for
        users that you create via the dashboard:

        .. code-block:: ini

           OPENSTACK_KEYSTONE_DEFAULT_ROLE = "user"

      * Optionally, configure the time zone:

        .. code-block:: ini

           TIME_ZONE = "TIME_ZONE"

        Replace ``TIME_ZONE`` with an appropriate time zone identifier.
        For more information, see the `list of time zones
        <http://en.wikipedia.org/wiki/List_of_tz_database_time_zones>`__.

Finalize installation
---------------------

.. only:: ubuntu or debian

   * Reload the web server configuration:

     .. code-block:: console

        # service apache2 reload

.. only:: obs

   * Start the web server and session storage service and configure
     them to start when the system boots:

     .. code-block:: console

        # systemctl enable apache2.service memcached.service
        # systemctl restart apache2.service memcached.service

     .. note::

        The ``systemctl restart`` command starts the Apache HTTP service if
        not currently running.

.. only:: rdo

   * Start the web server and session storage service and configure
     them to start when the system boots:

     .. code-block:: console

        # systemctl enable httpd.service memcached.service
        # systemctl restart httpd.service memcached.service

     .. note::

        The ``systemctl restart`` command starts the Apache HTTP service if
        not currently running.