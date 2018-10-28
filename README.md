Git
=========

Setup 'git' along with a specified configuration. If no configuration is specified, the default configuration is applied.

Requirements
------------

None

Role Variables
--------------

    scope: scope of the git configuration
    settings: any git config settings in a yaml dictionary format

Dependencies
------------

None

Example Playbook
----------------

Scope and settings can, but do not have to be input.

    - hosts: localhost
      roles: 
        role: git
        vars:
          scope: local
          settings:
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

Tibor Csoka
