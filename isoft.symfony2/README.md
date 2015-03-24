Symfony 2
=========

Role installs symfony dependencies and makes other preparatons (copies `parameters.yml`, migrations, cache clearing, etc)

Role Variables
--------------

You may change default variables

 - `php_path`
 - `composer {no_dev, optimize_autoloader}`

Dependencies
------------

This role requires composer installed globally and depends on `isoft.composer` role. Place it only after `isoft.composer` role or use it if you sure that composer has been installed earlier

Example Playbook
----------------

Before running role you should define `web_server_dir` which points to symfony 2 project home directory and make sure all variables from `parameters.yml.j2` are exited in vars block

    - hosts: servers
      vars:
         web_server_dir: "/vagrant"
      roles:
         - isoft.symfony2
