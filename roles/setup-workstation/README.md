setup-workstation
=========

Configure Open Stack Platform and isolate node.

Requirements
------------

First, you provision the Ansible Advanced - Homework and Ansible Advanced - OpenStack lab environments. 

Role Variables
--------------

See more /roles/setup-workstation/vars/main.yml

Dependencies
------------

from playbook: (view example)
- import_playbook: site-install-isolated-node.yml 

from main role:
- include_tasks: pre-tasks.yml
- include_tasks: create-flavor.yml
- include_tasks: create-keypair.yml
- include_tasks: create-sg.yml
- include_tasks: create-image.yml
- include_tasks: create-network.yml

Example Playbook
----------------

- hosts: localhost
  tasks:
  - name: Create workstation inventory
    add_host:
       name: "workstation-{{OSP_GUID}}.rhpds.opentlc.com"
       group: workstation


- hosts: workstation
  become: yes
  roles:
    - setup-workstation

- import_playbook: site-install-isolated-node.yml 

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
