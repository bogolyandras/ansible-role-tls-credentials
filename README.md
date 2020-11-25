TLS credentials
=========

A brief description of the role goes here.

[![Ansible Galaxy](https://img.shields.io/badge/galaxy-bogolyandras.tls_credentials-52009.svg?style=flat)](https://galaxy.ansible.com/bogolyandras/tls-credentials)
[![Build Status](https://travis-ci.com/bogolyandras/ansible-role-tls-credentials.svg?branch=main)](https://travis-ci.com/bogolyandras/ansible-role-tls-credentials)

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

```yaml
tls_key_path_source: /path/to/my.key
tls_cert_path_source: /path/to/my.crt
tls_root_dir: /etc/pki/mykey
tls_key_path: "{{ tls_root_dir }}/tls.key"
tls_cert_path: "{{ tls_root_dir }}/tls.crt"
```
Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
---
- hosts: servers
  become: true
  vars:
      tls_key_path_source: /path/to/my.key
      tls_cert_path_source: /path/to/my.crt
      tls_root_dir: /etc/pki/mykey
      tls_key_path: "{{ tls_root_dir }}tls.key"
      tls_cert_path: "{{ tls_root_dir }}tls.crt"
  roles:
    - tls-credentials
    - vsftpd
    - nginx

```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
