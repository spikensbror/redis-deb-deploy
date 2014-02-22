Redis Debian Deployment Scripts
===============================

Description
-----------

This repository contains easy-to-use install and uninstall scripts for getting redis up
and running on Debian.

Features
--------

 * Install
 * Uninstall
 * 'redis' User and Group
 * init.d Script

Usage
-----

### Configuration

The init.d script is configured to load the __Redis__ configuration from `/etc/redis.conf`,
you can either leave this file non-existant to use the defaults or create it and configure it
to your preferences.

### Installing

To install __Redis__ with the deployment scripts, simply run the `./redis-install` script.
This will download, compile and install the latest stable version of __Redis__ as well as
make __Redis__ start up on boot. It will also create the necessary `redis` user and group
that the init.d script will run __Redis__ as. This also copies a default configuration to
`/etc/redis.conf`.

### Uninstalling

To uninstall __Redis__ with the deployment scripts, simply run the `./redis-uninstall` script.
This will remove any traces of __Redis__ as well as the user/group pair.

_Note: Uninstalling does not remove the configuration file at `/etc/redis.conf`_
