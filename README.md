AIDE
====

This role configures a host to be regularly monitored by [AIDE](https://aide.github.io/).

[![CI](https://github.com/markcaudill/ansible-role-aide/workflows/CI/badge.svg)](https://github.com/markcaudill/ansible-role-aide/actions?query=workflow%3ACI)

Role Variables
--------------

See (`defaults/main.yml`) for a complete listing of variables.


Dependencies
------------

None

Example Playbook
----------------

    - hosts: all
      become: yes
      roles:
         - {role: markcaudill.ansible_role_aide}

License
-------

MIT

Author Information
------------------

Mark Caudill <mark@mrkc.me>
