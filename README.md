# Role Name

An ansible role for deploying [github-authorized-keys](https://github.com/terjekv/github-authorized-keys) onto a host.

## Requirements

None.

## Role Variables

All role variables are unset to defer to the the defaults of [github-authorized-keys](https://github.com/terjekv/github-authorized-keys). Supported variables are:

````bash
github_api_token
github_organization
github_admin_team_name
github_admin_team_id
github_user_team_name
github_user_team_id
sync_users_gid
sync_users_groups
sync_users_shell
sync_users_root
sync_users_interval
etcd_endpoint
etcd_ttl
etcd_prefix
listen
integrate_ssh
log_level
````

See the application [documentation](https://github.com/terjekv/github-authorized-keys/) for their interpretation and their default values.

Required variables are:

````bash
github_api_token
github_organization
github_admin_team_name or github_admin_team_id
````

## Dependencies

- [geerlingguy.docker](https://galaxy.ansible.com/geerlingguy/docker)

## Example Playbook

````yaml
---
- hosts: servers
  roles:
    - { role: terjekv.github-authorized-keys,
        github_token: "42",
        github_admin_team_name: "ssh",
        github_organization: "myorg",
      }
````

## License

MIT

## Author Information

This role was created in 2023 by [Terje Kvernes](https://github.com/terjekv) based a template from [Hans Spaans](https://github.com/hspaans/ansible-role-template).
