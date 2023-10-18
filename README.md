Ansible Role: AD DHCP static lease
=========

An Ansible role to create a static DHCP lease on a domain joined DHCP server.

Requirements
------------

DA credentials.

Role Variables
--------------

```yml
domain_pdc: pdc01
domain_admin_user: 'AD01\Administrator'
domain_admin_password: Password!
dhcp_lease_ip: 192.168.91.69
dhcp_hostname: '{{ ansible_facts.hostname }}'
dhcp_scope_id: 192.168.91.0
```

Dependencies
------------

None.

Example Playbook
----------------

```yml
- hosts: wks01
  roles:
    - role: xbufu.ad_dhcp_lease
      vars:
        domain_pdc: pdc01
        domain_admin_user: 'AD01\Administrator'
        domain_admin_password: Password!
        dhcp_lease_ip: 192.168.91.69
        dhcp_hostname: '{{ ansible_facts.hostname }}'
        dhcp_scope_id: 192.168.91.0
```

License
-------

MIT / BSD

Author Information
------------------

Created by xbufu.
