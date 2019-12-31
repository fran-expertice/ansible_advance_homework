app-tier
=========

This role installs and configures the Tomcat.

Requirements
------------


Role Variables
--------------

payload: tomcat
tomcat_web_root: /usr/share/tomcat/webapps/ROOT

Templates
------------

index.html.j2 : Index File.

Example Playbook
----------------

- name: setup app tier
  hosts: apps
  become: yes
  gather_facts: false
  roles:
    - {name: app-tier, tags: [apps, tomcat]}

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
