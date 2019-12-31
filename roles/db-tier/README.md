db-tier
=========

Install and configure Postgres.

Requirements
------------

Install repo through the role base-config

Role Variables
--------------

Nothing.

Example Playbook
----------------

- name: setup database tier
  become: yes
  hosts: appdbs
  roles:
    - {name: base-config, tags: base-config}
    - {name: db-tier, tags: [dbs, postgres]}

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
