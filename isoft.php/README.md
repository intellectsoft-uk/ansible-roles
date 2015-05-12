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

If you need some other extensions, just set list of it into `php_extensions` var. Also you have `pecl_extensions` list of hashes.

### PECL extensions

You can specify ini file template for PECL extension via `ini` property:

```
pecl_extensions:
 - name: xdebug
   ini: templates/php/xdebug.ini.j2
```

Also you can extend default PECL extension ini:

```
{% extends 'roles/isoft.php/templates/extension.ini.j2' %}

{% block extension_settings %}
[debug]
; Remote settings
xdebug.remote_enable=1
xdebug.remote_autostart=1
{% endblock %}
```

Please note that `ini` property is optional.

## Variables
see `defaults/main.yml`

## Example playbook

```
---
- hosts: all
  roles:
    - isoft.php
```
