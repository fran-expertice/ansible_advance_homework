Role Name
=========

Configure Tower instance.

Requirements
------------

Prepare the provision instances on AWS  for the production environment.

Role Variables
--------------

See /roles/config-tower/vars/main.yml

Dependencies
------------

- include_tasks: pre-config-tower.yml
- include_tasks: post-config-tower.yml
- include_tasks: ec2_dynamic.yml
- include_tasks: job_template.yml
- include_tasks: workflow_template.yml

Example Playbook
----------------

- hosts: localhost
  gather_facts: false 
  become: yes 
  roles:
    - config-tower

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
