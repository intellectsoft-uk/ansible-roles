Common Role for ansible
===========================

Role setup locale as `en_US` and `UTC` timezone. Change `common_locale_lang` and `common_timezone` variables if you prefer another values

Role will install packages by default:

    - vim
    - curl
    - mc
    - aptitude
    - python-curl
    - python-software-properties
    
In `additional_apt_packages` variable define list of any packages you wish to install

## Example Playbook

```

    ---
     - hosts: all
       vars:
        apt_keys:
          - http://www.dotdeb.org/dotdeb.gpg
        apt_repositories:
          - deb http://packages.dotdeb.org wheezy all
        additional_apt_packages:
          - htop
        system_users:
          - user: my_project
            comment: My Project User
            home: "/home/my_project"
       roles:
        - isoft.common

```
