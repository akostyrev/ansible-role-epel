epel
====

[![Build Status](https://travis-ci.org/kostyrevaa/ansible-epel.svg?branch=master)](https://travis-ci.org/kostyrevaa/ansible-epel)

Installs and configures Yum EPEL repository.

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

| Name                                | Default | Description                                |
|-------------------------------------|---------|--------------------------------------------|
| epel_repo_enabled                   | true    | Enable/disable EPEL repo                   |
| epel_repo_debuginfo_enabled         | false   | Enable/disable EPEL debuginfo repo         |
| epel_repo_source_enabled            | false   | Enable/disable EPEL source repo            |
| epel_repo_testing_enabled           | false   | Enable/disable EPEL testing repo           |
| epel_repo_testing_debuginfo_enabled | false   | Enable/disable EPEL testing debuginfo repo |
| epel_repo_testing_source_enabled    | false   | Enable/disable EPEL testing source repo    |

Dependencies
------------

None

Example Playbook
----------------

Install and enable EPEL repo
```
- hosts: all
  roles:
    - { role: kostyrevaa.epel }
```

Install and disable EPEL repo
```
- hosts: all
  roles:
    - { role: kostyrevaa.epel, epel_repo_enabled: false }
```

License
-------

BSD

Author Information
------------------

Inspired by:
- Kevin Brebanov's [epel role](https://github.com/kbrebanov/ansible-epel.git))
- Derek Carter's [epel role](https://github.com/goozbach-ansible/role-epel.git))
