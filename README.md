Ansible role: git
=========

[![Build Status](https://travis-ci.com/Provizanta/ansible-role-git.svg?branch=master)](https://travis-ci.com/Provizanta/ansible-role-git)

Setup `git` along with a specified configuration. If no configuration is specified, a limited minimal configuration is loaded to setup global gitignore policies.

Requirements
------------

None

Role Variables
--------------

Optional variables:

    scope: <enum global|local, scope of the git configuration>
    global_gitignore: <list, lines for the global gitignore file>
    configuration: <git configuration in YAML format>

Dependencies
------------

None

Example Playbook
----------------

    - hosts: localhost
      roles:
        role: git
        vars:
          scope: local
          configuration:
            user:
              name: "Name Surname"
              email: "name@surname.com"
            core:
              editor: vim

License
-------

MIT

Author Information
------------------

Tibor Csóka
