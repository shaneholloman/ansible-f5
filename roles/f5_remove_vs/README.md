<!-- This was created with Claude Code -->

f5_remove_vs
============

An Ansible role for f5 remove vs.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **virtual_server_fqdn**: Variable used in: Setup fact for app server
  - Default: `lb.shadowman.dev`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: f5_remove_vs
      vars:
        virtual_server_fqdn: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
