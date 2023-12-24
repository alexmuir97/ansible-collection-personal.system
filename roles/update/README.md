# Ansible Role: personal.system.update
An Ansible role to manage and install updates.

## Description
By default, this role will allow a user to upgrade all packages found on a system. If required, specific packages may also be targeted. The role is mostly intended for ongoing maintenance but can also be useful for initial deployments.

## Dependencies
None.

## Conflicts
None.

## Variables
The role comes with default variables (via `defaults/main.yml`), which can be overridden.

```yaml
---
update_package_name: "*"
```

`update_package_name: "*"` is used to target all packages on a system for updates. `"*"` can be changed to specify a package or list of packages.


```yaml
update_reboot_enabled: true
update_reboot_timeout: 3600
update_reboot_delay: 0
```

When set to true, `update_reboot_enabled` will result in the system being rebooted when a change is found.
`update reboot_timeout` sets the maximum duration in seconds for machine to reboot and respond to a test command.
`update_reboot_delay` sets how many seconds to wait before reboot. On Linux, this is converted to minutes and rounded down. If less than 60, it will be set to 0.

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
        name: "personal.system.update"
```
