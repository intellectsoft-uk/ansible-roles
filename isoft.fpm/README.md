Intellectsoft FPM Ansible role
=================================

Install ruby fpm package.
https://github.com/jordansissel/fpm

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