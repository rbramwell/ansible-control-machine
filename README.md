Role Name
=========

An Ansible role to configure an Ansible Control Machine

Requirements
------------

None

Role Variables
--------------

```
---
# defaults file for ansible-control-machine
ansible_roles:
  - repo: 'https://github.com/mrlesmithjr/ansible-base.git'
    dest: 'ansible-base'
  - repo: 'https://github.com/mrlesmithjr/ansible-bootstrap.git'
    dest: 'ansible-bootstrap'
  - repo: 'https://github.com/mrlesmithjr/ansible-manage-ssh-keys.git'
    dest: 'ansible-manage-ssh-keys'
  - repo: 'https://github.com/mrlesmithjr/ansible-ntp.git'
    dest: 'ansible-ntp'
  - repo: 'https://github.com/mrlesmithjr/ansible-postfix.git'
    dest: 'ansible-postfix'
  - repo: 'https://github.com/mrlesmithjr/ansible-rsyslog.git'
    dest: 'ansible-rsyslog'
ansible_roles_dir: '/etc/ansible/roles'
ansible_versions:
  - ver: '1.9.4'
    addl_modules: []
  - ver: '1.9.5'
    addl_modules: []
  - ver: '1.9.6'
    addl_modules:
      - 'ndg-httpsclient'
      - 'pyasn1'
      - 'pyopenssl'
      - 'pysphere'
      - 'pyvmomi'
  - ver: '2.0.0.1'
    addl_modules: []
  - ver: '2.0.0.2'
    addl_modules: []
  - ver: '2.0.1.0'
    addl_modules: []
  - ver: '2.0.2.0'
    addl_modules: []
  - ver: '2.1.0.0'
    addl_modules:
      - 'ndg-httpsclient'
      - 'pyasn1'
      - 'pyopenssl'
      - 'pysphere'
      - 'pyvmomi'
  - ver: '2.1.1.0'
    addl_modules:
      - 'ndg-httpsclient'
      - 'pyasn1'
      - 'pyopenssl'
      - 'pysphere'
      - 'pyvmomi'
ansible_virtualenv_dir: '/opt/ansible_virtualenvs'
easy_install_pip: false
```
Dependencies
------------

None

Example Playbook
----------------

```
---
- hosts: all
  become: true
  vars:
  roles:
    - role: ansible-control-machine
  tasks:
```

License
-------

BSD

Author Information
------------------

Larry Smith Jr.
- @mrlesmithjr
- http://everythingshouldbevirtual.com
- mrlesmithjr [at] gmail.com