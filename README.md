AIDE
====

This role configures a host to be regularly monitored by [AIDE](https://aide.github.io/).

[![CI](https://github.com/markcaudill/ansible-role-aide/workflows/CI/badge.svg)](https://github.com/markcaudill/ansible-role-aide/actions?query=workflow%3ACI)

Role Variables
--------------

See (`defaults/main.yml`) for a complete listing of variables.

- `aide['tags']`:  a list of the tags applied to each task in this role (default: `[aide]`)
- `aide['packages']`: a list of packages installed (default: `[aide, crontabs]`)
- `aide['no_nfs']`: whether or not to exclude the currently-known NFS mounts (default: `true`)
- `aide['cron']`: the cron configuration to use (default is essentially `@weekly`, see `defaults/main.yml` for more detail)
- `aide['database_init']`: whether or not to initialize the database if it doesn't already exist (default: `true`)
- `aide['config']`: the variables used to generate the `aide.conf` file (see `defaults/main.yml` for more detail)


Dependencies
------------

None

Example Playbook
----------------

    - hosts: all
      become: yes
      roles:
         - { role: markcaudill.aide }

License
-------

MIT

Author Information
------------------

Mark Caudill <mark@mrkc.me>
