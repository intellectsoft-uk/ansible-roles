Intellectsoft Nginx Ansible role
=================================

Base nginx role for symfony-based projects

##Example playbook

```
---
 - hosts: all
   vars:
      nginx_server_name: vagrant
      nginx_root_dir: /vagrant/web # for symfony based projects
   roles:
     - isoft.nginx
```

### WebSockets
If you are using nginx for proxy websockets, then you may just set this variables:

```
nginx_websockets_location /wsapp
nginx_websockets_upstream: http://localhost:8743
```

See template for details

### Templates
You may want to change default templates for nginx.conf and your vhosts. To do so you can change `nginx_config_template` and `nginx_template_path` variables to specify your templates.

## TODO:
 - ssl version
 - nginx.conf configuration


