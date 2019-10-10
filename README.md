Ansible role: git
=========

[![Build Status](https://travis-ci.com/Provizanta/ansible-role-git.svg?branch=master)](https://travis-ci.com/Provizanta/ansible-role-git)

Setup `git` along with a specified configuration. If no configuration is specified, a limited minimal configuration is loaded to setup global gitignore policies.

Requirements
------------

None

Role Variables
--------------

These variables are defined in [defaults/main.yml](./defaults/main.yml):

    git_scope: global           # enum: global|local

    git_global_gitignore: []    # global gitignore lines

These variables are not defaulted and can be specified:

    git_configuration:          # dict, configuration in YAML format

Dependencies
------------

None

Example Playbook
----------------

    - name: Converge
      hosts: all
      roles:
        - role: git
          vars:
            git_scope: global
            git_configuration:
              user:
                name: "Name Surname"
                email: "name@surname.com"
              core:
                excludesfile: "/tmp/gitignore"

License
-------

MIT

Author Information
------------------

Tibor Csóka
