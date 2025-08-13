Ansible Installation
=========

This role can be used to install Ansible on Ubuntu

[![Build Status](https://github.com/Rheinwerk/ansible-role-ansible/actions/workflows/ci.yml/badge.svg)](https://github.com/Rheinwerk/ansible-role-ansible/actions/workflows/ci.yml)

Requirements
------------

None.

Role Variables
--------------

None.


Dependencies
------------

Python and Pip installed.


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      var:
        ansible:
          ansible_version: "" # latest
          python_binary: "/usr/bin/python3"
          virtualenv: "/opt/ansible_virtualenv"
      roles:
         - { role: ansible, tags: [ 'ansible' ], _ansible: "{{ ansible }}" }

License
-------

Please see LICENSE.

Author Information
------------------

Original author is [Michael Schmitz](https://github.com/eifelmicha) as member of the [Rheinwerk](https://github.com/Rheinwerk) project.
