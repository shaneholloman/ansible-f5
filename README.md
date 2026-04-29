<!-- This was created with Claude Code -->

# F5 Automation

[![Contribute](https://img.shields.io/badge/OpenShift-Dev%20Spaces-525C86?logo=redhatopenshift&labelColor=EE0000)](https://devspaces.apps.ocp.shadowman.dev/#https://github.com/shadowman-lab/Ansible-F5)


This directory contains Ansible automation for f5 management and operations.

## Overview

The F5 automation provides playbooks and roles for managing and configuring
f5 infrastructure and services.

## Roles

| Role | Description |
| ---- | ----------- |
| [f5_add](roles/f5_add/README.md) | Role for f5 add |
| [f5_disable](roles/f5_disable/README.md) | Role for f5 disable |
| [f5_enable](roles/f5_enable/README.md) | Role for f5 enable |
| [f5_remove](roles/f5_remove/README.md) | Role for f5 remove |
| [f5_remove_vs](roles/f5_remove_vs/README.md) | Role for f5 remove vs |

## Playbooks

| Playbook | Description | Target Hosts |
| -------- | ----------- | ------------ |
| add_to_load_balancer.yml | Playbook for add to load balancer | {{ vm_name | default('all') }} |
| disable_pool_member.yml | Playbook for disable pool member | {{ vm_name | default('all') }} |
| enable_pool_member.yml | Playbook for enable pool member | {{ vm_name | default('all') }} |
| remove_from_load_balancer.yml | Playbook for remove from load balancer | {{ vm_name | default('all') }} |
| remove_virtual_server.yml | Playbook for remove virtual server | localhost |

## Usage

### Running with ansible-navigator

```bash
# Run a playbook
ansible-navigator run add_to_load_balancer.yml

# Run in stdout mode
ansible-navigator run add_to_load_balancer.yml -m stdout
```

### Using roles

```yaml
- hosts: target_hosts
  roles:
    - f5_add
```

## Requirements

- Ansible 2.9 or higher (via ansible-navigator)
- Required collections (see `collections/requirements.yml` if present)
- Appropriate access credentials configured via environment variables

## Directory Structure

```
Ansible-F5/
├── roles/              # Ansible roles
├── *.yml               # Playbooks
├── collections/        # Collection dependencies (if present)
└── ansible-navigator.yml  # Navigator configuration
```
