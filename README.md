couchpotato
===========

[![Build Status](https://img.shields.io/travis/marvinpinto/ansible-role-couchpotato/master.svg?style=flat-square)](https://travis-ci.org/marvinpinto/ansible-role-couchpotato)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-couchpotato-blue.svg?style=flat-square)](https://galaxy.ansible.com/marvinpinto/couchpotato)
[![License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.txt)

Ansible Galaxy role to install and manage [CouchPotato](https://couchpota.to/).


Requirements
------------

This role has been tested on Ubuntu 14.04 and will likely only work on an
Ubuntu-like system.


Role Variables
--------------

``` yaml
# Application config
couchpotato_app_src_directory: '/opt/couchpotato_src'
couchpotato_app_data_directory: '/opt/couchpotato_data'
couchpotato_app_pid_file: '/tmp/couchpotato.pid'

# Daemon config
couchpotato_daemon_user: 'couchdaemon'
couchpotato_daemon_extra_args: ''
```


Examples
--------

Install this module from Ansible Galaxy into the './roles' directory:
```bash
ansible-galaxy install marvinpinto.couchpotato -p ./roles
```

Use it in a playbook as follows:
```yaml
- hosts: '127.0.0.1'
  roles:
    - role: 'marvinpinto.couchpotato'
      become: true
```


Development
-----------
Use the supplied `Vagrantfile` for local development and testing (hint: `vagrant up --provision`)
