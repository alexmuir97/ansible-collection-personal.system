# Ansible Role: personal.system.chrony
An Ansible role to install and configure chrony.

## Description
Chrony is a tool that can be used as a NTP client or NTP server.

## Dependencies
None.

## Conflicts
None.

## Variables
The role comes with default variables (via `defaults/main.yml`), which can be
overridden.

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
        name: "personal.system.chrony"
```