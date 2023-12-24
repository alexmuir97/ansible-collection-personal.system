# Ansible Role: personal.system.hostname
An Ansible role to configure hostnames.

## Description
The role configures the hostname, either from the given inventory hostname or a given hostname by a variable.

## Dependencies
None.

## Conflicts
None.

## Variables
The role comes with default variables (via `defaults/main.yml`), which can be overridden.

```yaml
---
hostname_name: "{{ inventory_hostname }}"
```
by default, the variable `hostname_name` is set to `{{ inventory_hostname }}`, utilizing the full `inventory_hostname`, which represents the current host being iterated over in the play. This is not influenced by delegation and consistently reflects the original host for the task. For example, if `inventory_hostname` is `www.example.com`, then `hostname_name` takes the value `www.example.com`.

Alternatively, you can opt for the abbreviated version with `inventory_hostname_short`, derived from the first section after splitting the inventory_hostname via `.`. This is influenced by delegation and will represent the 'short name' of the delegated host. For example, if the `inventory_hostname` is `www.example.com`, then `inventory_hostname_short` becomes `www`.

## Additional hints
None.

## Examples
The below examples should help to explain how the role can be used.

```yaml
# Simple example with defaults

- name: "Examples for the usage"
  hosts: "all"

  tasks:

    - name: "Example with defaults"
      ansible.builtin.import_role:
        name: "personal.system.hostname"
```