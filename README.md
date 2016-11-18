Ansible Installation
=========

This role can be used to install Ansible on Ubuntu

[![Build Status](https://travis-ci.org/Rheinwerk/ansible-role-ansible.svg?branch=master)](https://travis-ci.org/Rheinwerk/ansible-role-ansible)

Requirements
------------

None.

Role Variables
--------------

None.


Dependencies
------------

None.


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      var:
        ansible:
          ...
      roles:
         - { role: ansible, tags: [ 'ansible' ], _ansible: "{{ ansible }}" }

License
-------

Please see LICENSE.

Author Information
------------------

Original author is [Daniel Schneller](https://github.com/dschneller) as member of the [Rheinwerk](https://github.com/Rheinwerk) project.

