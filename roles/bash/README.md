# Ansible Role: personal.system.bash
An Ansible role to install and configure bash.

## Description
Having a Bash environment is mandatory for most workflows done via SSH or console input.

## Dependencies
None.

## Conflicts
None.

## Variables
The role comes with default variables (via `defaults/main.yml`), which can be overridden.

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
        name: "personal.system.bash"
```
