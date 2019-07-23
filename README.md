[![Build Status](https://travis-ci.org/Krast76/common.svg?branch=master)](https://travis-ci.org/Krast76/common)
Role Name
=========

This role can be used to boostrap new servers, or update server.

Requirements
------------

None. Only servers who can be managed by Ansible

Role Variables
--------------

package_state: (Default: present) 
update: (Default: False) Do a package upgrade

# Only for CentOS
epel: Install EPEL repository
kernel_number: Default: 1) number of old kernel to keep

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
