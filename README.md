# Ansible OpenProject [![Build Status](https://travis-ci.org/danihodovic/ansible-role-openproject.svg?branch=master)](https://travis-ci.org/danihodovic/ansible-role-openproject)

An opinionated role that installs OpenProject as a single Docker container. If
you're looking for a role that installs it as multiple containers -
https://github.com/abate/ansible-role-openproject.

### Role Variables

Required:

- `openproject_secret_key_base`

Optional variables in [defaults.yml](./defaults/main.yml).

Example Playbook
----------------

```yaml
---
- name: Install OpenProject
  hosts: localhost
  roles:
    - role: ansible-role-openproject
      vars:
        openproject_secret_key_base: secret
        openproject_docker_ports: ['80:80']
        openproject_config: '{{ lookup("template", "openproject_config.yml") }}'
```

### License

MIT

### Author Information

Dani Hodovic (https://depode.com)
