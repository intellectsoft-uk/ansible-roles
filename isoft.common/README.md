Common Role for ansible
===========================

Do initial configuration, installs main environment dependencies, creates system users

List of required packages:
```
- curl
- aptitude
- python-pycurl
- python-software-properties
```

You can use `apt_repositories` and `apt_keys`.

You can add your own packages via `common_apt_packages` var. Both lists will be merged and installed.

To specify default locale you can use `common_locale_lang` and `common_locale_all` vars. Both by default have value `en_US.UTF-8`.

To specify timezone, use `common_timezone` var. UTC by default.

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
