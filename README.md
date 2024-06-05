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

Python 3.12 and Pip installed. You can use the following ansible tasks to ensure requirements are met:

```yaml
- name: Add Deadsnakes APT repository
  ansible.builtin.apt_repository:
    repo: ppa:deadsnakes/ppa

- name: Install python3.12 via APT
  ansible.builtin.apt:
    state: present
    update_cache: true
    name:
      - python3.12
      - python3.12-dev
      - python3.12-venv

- name: Install python3-pip via APT
  ansible.builtin.apt:
    state: present
    name: python3-pip
```


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

