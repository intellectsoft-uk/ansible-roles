Intellectsoft install deb package and config Ansible role
=========================================================

Install deb package and configs and execute some commands after it

## Example playbook
```
---
- hosts: all
  vars:
    setup_deb: yes
    setup_deb_path_src: builds/build.deb
  roles:
    - isoft.setup

```
