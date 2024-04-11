# Ansible Role: jwt-cli

[![CI](https://github.com/sgaunet/ansible-role-jwt-cli/workflows/CI/badge.svg?event=push)](https://github.com/sgaunet/ansible-role-jwt-cli/actions?query=workflow%3ACI)

An Ansible Role that installs [jwt-cli][https://github.com/sgaunet/jwt-cli] on Linux.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    jwtcli_version: "latest"     # Version of jwt-cli to install. Use "latest" to install the latest version.
    jwtcli_bin_path: "/usr/local/bin"
    jwtcli_tmp_directory: "{{ lookup('env', 'TMPDIR') | default('/tmp', true) }}"
    jwtcli_os: "linux"
    jwtcli_arch: "amd64"

## Dependencies

None.

## Example Playbook

```yaml
- hosts: all
  roles:
    - sgaunet.jwt_cli
```

## License

MIT
