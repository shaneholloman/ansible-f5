<!-- This was created with Claude Code -->

f5_disable
==========

An Ansible role for f5 disable.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **pool_name**: Variable used in: Set facts if enabling appserver
  - Default: `https_pool`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: f5_disable
      vars:
        pool_name: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
