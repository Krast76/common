[![Build Status](https://travis-ci.org/Krast76/common.svg?branch=master)](https://travis-ci.org/Krast76/common)

Role Name
=========

This role can be used to boostrap new servers, or update server.

Requirements
------------

None. Only servers who can be managed by Ansible

Role Variables
--------------

* package_state: (Default: present) 
* update: (Default: False) Do a package upgrade
* system_timezone: (not defined by default) Set the system timezone
* users: (Default: empty) Create user, and set it in groups

exemple :
```yaml
users:
  bob:
    groups: wheel,toto
```

* ssh_key: (Default: empty) Setup ssh keys

exemple :

```yaml
ssh_key:
  - name: "bob" # User who will get the public ssh keys on his .authorized_key
    state: "present" # The pub key should be present
    ssh_key:
      - "PUBKEY 1"
      - "PUBKEY 2"
```
# Only for CentOS

* epel: Install EPEL repository
* kernel_number: Default: 1) number of old kernel to keep
* selinux_state: (Default: enforcing) Set the state of SELinux 
* selinux_policy: (Default: targeted) Set the policy of SELinux

Dependencies
------------

No dependencies.

Example Playbook
----------------

Simple playbook:

```bash
- hosts: servers
  roles:
     - common
```
License
-------

BSD

Author Information
------------------

if you break something with this ansible role, i will not responsible.
