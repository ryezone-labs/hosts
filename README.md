ryezone_labs.hosts
=========

Sets /etc/hosts file with specified hostname.

Role Variables
--------------

### Global Variables

- `ryezone_labs_top_level_domain` (string)

   Sets the top level domain for DNS and DHCP.

### Role Variables

- `hosts_hostname` (string)

   When set, configures the /etc/hosts file and the hostname.

- `hosts_domain` (string)

   Sets the domain component of the hostname.  Defaults to `{{ryezone_labs_top_level_domain}}`.

Example Playbook
----------------

```yaml
---
- hosts: 127.0.0.1
  connection: local
  roles:
    - ryezone_labs.hosts
  vars:
    hosts_hostname: my-host
    hosts_domain: 'domain.local'
```

License
-------

BSD
