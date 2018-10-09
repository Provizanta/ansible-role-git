Git
=========

Setup 'git' along with a specified configuration. If no configuration is specified, the default configuration is applied.

Requirements
------------

None

Role Variables
--------------

scope - scope of the git configuration (e.g. global)

settings - any git config settings in a yaml dictionary formt (e.g. core.editor: 'vim')

Dependencies
------------

None

Example Playbook
----------------

Scope and settings can, but do not have to be input.

    - hosts: localhost
      roles:
         - git
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
