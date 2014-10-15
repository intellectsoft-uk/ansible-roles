Intellectsoft MySQL Ansible role
=================================

Based on `geerlingguy.mysql`

## Example playbook
```
---
- hosts: all
  vars:
    mysql_root_password: root
    mysql_users:
        - name: "{{app_name}}"
          password: ~
    
    mysql_databases:
        - name: "{{app_name}}db"
  roles:
    - isoft.mysql
```