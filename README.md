# WildFly

Install [WildFly Application Server](http://wildfly.org) along with OpenJDK on
Ubuntu.

I've developed and tested with Ansible 2.2 on Ubuntu 16.04.
Other versions should work as well (please let me know so that I can update the
supported platforms!)


## Requirements

Your host must have internet access in order to download the WildFly archive.


## Role Variables

### Installed version

WildFly v10.1.0 gets installed by default:

    wildfly_version: "10.1.0.Final"
    wildfly_checksum: "sha1:5ea0a70a483a4beaf327faeaf0a391208d33d4bd"

If you want to install a different version don't forget to update the SHA-1
checksum as well!

### Configuration

You can overwrite these settings:

```yaml
# The configuration you want to run
wildfly_config: standalone.xml

# The mode you want to run
wildfly_mode: standalone

# The address to bind to
wildfly_bind: 0.0.0.0
```

### Wildfly HOME

Wildfly's HOME is `/opt/wildfly` - a symlink to the basedir.
Please use `wildfly_home` to access this directory from your
roles or playbooks.


## Dependencies

None.


## Example Playbook

Use it like this:

```yaml
- hosts: servers
  roles:
     - role: bjoernalbers.wildfly
```

## License

BSD


## Author Information

Björn Albers
