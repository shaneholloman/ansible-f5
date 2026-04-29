<!-- This was created with Claude Code -->

f5_add
======

An Ansible role for f5 add.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **pool_name**: Variable used in: Set facts if creating appserver
  - Default: `https_pool`

* **virtual_server_name**: Variable used in: app_pool
  - Default: `webapp`

* **virtual_server_ip**: Variable used in: poolapp
  - Default: `172.16.3.121`

* **virtual_server_fqdn**: Variable used in: poolapp
  - Default: `lb.shadowman.dev`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: f5_add
      vars:
        pool_name: <value>
        virtual_server_name: <value>
        virtual_server_ip: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
