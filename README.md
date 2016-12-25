WildFly
=======

Install [WildFly Application Server](http://wildfly.org) along with OpenJDK on
Ubuntu.

I've developed and tested with Ansible 2.2 on Ubuntu 16.04.
Other versions should work as well (please let me know so that I can update the
supported platforms!)

Requirements
------------

Your host must have internet access in order to download the WildFly archive.

Role Variables
--------------

WildFly v10.1.0 gets installed by default:

    wildfly_version: "10.1.0.Final"
    wildfly_checksum: "sha1:5ea0a70a483a4beaf327faeaf0a391208d33d4bd"

If you change the version please also update the zip archive's checksum.

PS: The basedir - accessible via `wildfly_home` - is `/opt/wildfly`.

Dependencies
------------

None.

Example Playbook
----------------

Use it like this:

```yaml
- hosts: servers
  roles:
     - role: bjoernalbers.wildfly
```

License
-------

BSD

Author Information
------------------

Björn Albers
