Intellectsoft PHP Ansible role
=================================

Handles installation of php-fpm and php-cli. Will also install listed php and pecl extensions.
 
## Installed extensions
There is set of mandatory extensions:

```
- php5-intl
- php5-sqlite
- php5-mcrypt
- php5-gd
- php5-curl
```

If you need some other extensions, just set list of it into `php_extensions` var. Also you have `pecl_extensions` list.

## Dependency
On Debian depends from `isoft.dotdeb`

## Variables
see `defaults/main.yml`

## Example playbook

```
---
- hosts: all
  roles:
    - isoft.php
```
