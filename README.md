Ansible Roles
=================

Collection of ansible roles for internal usage. If you are using some other roles that you don't want to commit, so go ahead. Every directory except `isoft.*` will be ignored so fill free to install galaxy roles with command:

```
ansible-galaxy install -p path/to/roles some.role,version
```

**Note**: it is better to store all galaxy roles in one file and install them using `--role-file` options.

## Documentation fo roles
Each role contain (or should contain) README file

## Contribution

Please use tags for commits. For example if your commit relies to nginx role, then use this commit message format:

```
[nginx] Your commit description
```

