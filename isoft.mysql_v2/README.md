Intellectsoft MySQL Ansible role v2
=================================

Role, which setup only databases. No more

## Example playbook


```
---
- hosts: all
  vars:
    mysql_username: root
    mysql_password: ''
    mysql_databases:
        - name: "{{app_name}}db"
  roles:
    - isoft.mysql_v2
```