Intellectsoft install deb package and config Ansible role
=========================================================

Install deb package and configs and execute some commands after it

## Example playbook
```

    ---
    - hosts: all
      vars:
        setup_path_dist: "/srv/project"
        setup_sudo_user: "project-user"
        setup_deb: yes
        setup_deb_path_src: "../../../artifacts/{{app_name}}.deb"
        setup_after_install: yes
        setup_configs_templates:
          - {src: '../../../targets/dev/parameters.yml.j2', dist: '/srv/project/app/config/'}
        setup_after_install_commands:
          - 'app/console cache:clear --env=prod'
          - 'app/console assetic:dump --env=prod'
          - 'app/console doctrine:migrations:migrate -n'
      roles:
        - isoft.setup

```