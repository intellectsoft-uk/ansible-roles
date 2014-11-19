Common Role for ansible
===========================

Do initial configuration, installs main environment dependencies, creates system users

List of required packages:
```
- vim
- curl
- mc
- aptitude
- python-pycurl
- python-software-properties
```

You can use `apt_repositories` and `apt_keys`.
You can add your own packages via `common_apt_packages` var. Both lists will be merged and installed.

## TODO
- set locale

## Example Playbook

```
---
 - hosts: all
   vars:
    apt_keys:
      - http://www.dotdeb.org/dotdeb.gpg
    apt_repositories:
      - deb http://packages.dotdeb.org wheezy all
    common_apt_packages:
      - htop
    system_users:
      - user: my_project
        comment: My Project User
        home: "/home/my_project"
   roles:
    - isoft.common

```
