base-config
=========

Install repository file on all systems and install the necessary packages.

Templates
------------

open_three-tier-app.repo : Repo File.

Role Variables
--------------

Nothing.

Pre-requisite
------------

Install repo through the role base-config 

Example Playbook
----------------

- name: setup load-balancer tier
  hosts: frontends
  become: yes
  roles:
    - {name: base-config, tags: base-config}
    - {name: lb-tier, tags: [lbs, haproxy]}

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
