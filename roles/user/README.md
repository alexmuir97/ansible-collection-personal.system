# Ansible Role: personal.system.user
An Ansible role to manage users and related configuration.

## Description
This role configures users locally on a system, providing their public keys and sudoer files where required.

## Dependencies
None.

## Conflicts
None.

## Variables
The role comes with default variables (via `defaults/main.yml`), which can be overridden.

## Additional hints
To set a password for a user, generate a valid password hash in advance. This can be achieved using the following command:

With mkpasswd:

```shell
$ mkpasswd --method=sha-512
Password: mysecurepassword
$6$AXc46V09JLJkVUhl$WAWVDjlbTnAsTv.RppZbhQjVDbIfHCPdA/xeiQYY3iLtWztJanuzN3jluSXQOABybgXhOmxhAYyzzHmYbj6Oq/
```

## Examples
The below examples should help to explain how the role can be used.

```yaml
# Simple example with defaults

- name: "Examples for the usage"
  hosts: "all"

  tasks:

    - name: "Example with defaults"
      ansible.builtin.import_role:
        name: "personal.system.user"
```
