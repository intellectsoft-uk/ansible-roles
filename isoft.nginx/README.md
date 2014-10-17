Intellectsoft Nginx Ansible role
=================================

Base nginx role for symfony-based projects

##Example playbook

```
---
 - hosts: all
   vars:
      nginx:
        server_name: vagrant
        root_dir: /vagrant/web # for symfony based projects
   roles:
     - isoft.nginx
```

### WebSockets
If you are using nginx for proxy websockets, then you may just set this variables:

```
nginx:
  websockets_location /wsapp
  websockets_upstream: http://localhost:8743
```

See template for details

## TODO:
 - ssl version
 - add tcp/ip configuration step?
 - optimize amount of workers (worker_processes = number of CPU cores, worker_processes = ulimit -n and so on)

