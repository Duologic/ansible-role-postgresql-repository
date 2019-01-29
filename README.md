Duologic.postgresql_repository
==============================

This role install the official Postgresql repositories. Tested on CentOS 7 and Ubuntu 18.04/Bionic. This role is sets facts for use in [geerlingguy.postgresql](https://github.com/geerlingguy/ansible-role-postgresql).

Role Variables
--------------

    postgres_repo_version: '11'

The [defaults](defaults/main.yml) use the `ansible_*` variables to find the platform and architecture.

The YUM repository matrix in [vars/yum.yml](vars/yum.yml) is scraped from the Postgresql website and transformed into a YAML file with PyYaml and `generate_yum_yaml.py`.

Example Playbook
----------------

```
    - hosts: servers
      become: yes
      roles:
         - { role: Duologic.postgresql_repository, postgres_repo_version: '11' }
```

License
-------

MIT

Author Information
------------------

Jeroen Op 't Eynde, jeroen@simplistic.be
