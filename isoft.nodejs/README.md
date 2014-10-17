Intellectsoft NodeJS and NPM Ansible role
=========================================

Installs latest node.js and npm on Debian based system

## Example playbook
```
---
- hosts: all
  vars:
    npm_global_packages: [gulp, bower]
  roles:
    - isoft.nodejs

```
