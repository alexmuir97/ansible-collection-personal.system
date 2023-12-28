# Ansible Role: personal.system.timezone
An Ansible role to configure timezones.

## Description
The role configures a timezone, setting Europe/London by default. The timezone should be changed where approriate; you may consider using UTC to avoid DST and log time issues.

## Dependencies
None.

## Conflicts
None.

## Variables
The role comes with default variables (via `defaults/main.yml`), which can be
overridden.

`timezone_name` is used to define the system's timezone.

## Additional hints
For supported Linux systems, a list of timezones can be found by running the following command:

```shell
$ timedatectl list-timezones
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
        name: "personal.system.timezone"
```
