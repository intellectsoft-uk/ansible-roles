Intellectsoft Composer role
=================================

You should provide `composer_github_oauth_token` variable to work with github repos without problems.

## Example playbook

```
---
 - hosts: all
   vars:
     composer_global_packages:
       - fabpot/php-cs-fixer:dev-master
     composer_github_oauth_token: 21af0695acfa6d2269fa4a532c00b5aeab434990
   roles:
     - isoft.composer

```

**Note**: OAuth token in this example is just a random string, so it shouldn't work.

