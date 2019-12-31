lb-tier
=========

Install Tomcat as payload.

Requirements
------------

Install repo through the role base-config

Role Variables
--------------

payload: tomcat
tomcat_web_root: /usr/share/tomcat/webapps/ROOT

Templates
------------

haproxy.cfg.j2 : Configure file HA Proxy.

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
