# Ansible Role: personal.system.avahi
An Ansible role to install and configure Avahi.

## Description
Avahi is a system which facilitates service discovery on a local network via the multicast DNS (mDNS) and DNS Service Discovery (DNS-SD) protocol suite. This Ansible role will install Avahi and start the daemon. If firewalld is installed, it will also allow mDNS traffic.

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
        name: "personal.system.avahi"
```
