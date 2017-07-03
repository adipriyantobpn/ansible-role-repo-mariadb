Ansible Role: MariaDB Repository
=========

An Ansible Role that to manage MariaDB Yum repository

Requirements
------------

This role needs no special requirements, except sudo access

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):


```yaml
---
repo_location:              international   # available options: international, vagrant
mariadb_enabled:            yes
mariadb_version:            10.2
```

Dependencies
------------

None

Example Playbook
----------------

We can use this roles multiple times with different `mariadb_version` like this:

```yaml
---
- name: Prepare CentOS 7 server
  hosts: centos7
  roles:
    - role: adipriyantobpn.repo-mariadb
      repo_location:              vagrant
      mariadb_enabled:            yes
      mariadb_version:            10.2
    - role: adipriyantobpn.repo-mariadb
      repo_location:              international
      mariadb_enabled:            no
      mariadb_version:            10.1
    - role: adipriyantobpn.repo-mariadb
      repo_location:              international
      mariadb_enabled:            no
      mariadb_version:            10.0
    - role: adipriyantobpn.repo-mariadb
      repo_location:              international
      mariadb_enabled:            no
      mariadb_version:            5.5
```

License
-------

BSD

Author Information
------------------

This role was created in 2017 by [Adi Priyanto](https://github.com/adipriyantobpn) as a learning purpose for community.