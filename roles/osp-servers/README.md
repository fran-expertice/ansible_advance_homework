osp-servers
=========

Create instances into osp.

Requirements
------------

First, you provision the Ansible Advanced - Homework and Ansible Advanced - OpenStack lab environments. 

Role Variables
--------------

more datails see /roles/osp-servers/vars/

Dependencies
------------

Nothing.

Example Playbook
----------------
   - name: create frontend  instance
  
- name: create frontend  instance
    include_role:
      name: osp-servers
      vars_from: frontend.yaml

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
