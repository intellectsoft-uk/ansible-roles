Intellectsoft install deb package and config Ansible role
=========================================================

Install deb package and configs and execute some commands after it

## Example playbook
```
---
- hosts: all
  vars:
    npm_global_packages: [gulp, bower]
  roles:
    - isoft.setup

```
