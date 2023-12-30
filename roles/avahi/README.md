# Ansible Role: personal.system.avahi
An Ansible role to install and configure Avahi.

## Description
Avahi is a service discovery technology for Linux using multicast DNS (mDNS)/DNS Service Discovery (DNS-SD) which eases the discovery of local hosts in a network. The Ansible role install Avahi and starts the daemon. If firewalld is installed, it will also allow mDNS traffic to path through.

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
