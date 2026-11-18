Ansible Installation
=========

This role can be used to install Ansible on Ubuntu

[![Build Status](https://github.com/Rheinwerk/ansible-role-ansible/actions/workflows/ci.yml/badge.svg)](https://github.com/Rheinwerk/ansible-role-ansible/actions/workflows/ci.yml)

Requirements
------------

None.

Role Variables
--------------

Every setting is one variable with a default in `defaults/main.yml`; set only the ones that
differ. The defaults are the CenterDevice values.

| Variable | Default |
|---|---|
| `_ansible_ansible_version` | `==2.21.5` (pip version specifier for ansible-core; `""` installs the latest) |
| `_ansible_python_binary` | `/usr/bin/python3` (creates the virtualenv) |
| `_ansible_virtualenv` | `/opt/ansible_virtualenv` |

The role installs ansible-core and the Python libraries the CenterDevice playbooks need into the
virtualenv and links the `ansible*` commands into `/usr/bin`.

Until v1.3.1 the role took one `_ansible` dict with the keys `ansible_version`, `python_binary` and
`virtualenv` instead.

Dependencies
------------

Python with the `venv` module and pip installed.


Example Playbook
----------------

A Debian 12 host that builds the virtualenv with Python 3.12:

    - hosts: servers
      vars:
        _ansible_python_binary: "/usr/bin/python3.12"
      roles:
        - { role: ansible, tags: ['ansible'] }

License
-------

Please see LICENSE.

Author Information
------------------

Original author is [Michael Schmitz](https://github.com/eifelmicha) as member of the [Rheinwerk](https://github.com/Rheinwerk) project.
