# Ansible role users

Prepare users profile

## Install

```shell
ansible-galaxy role install git+https://github.com/sergelogvinov/ansible-role-users.git,main
```

## Usage

```ini
# inventory file

[servers]
server-1          ansible_host=1.2.3.1
```

```yaml
# hosts/server-1.yaml

users:
  - username: developer
    name: "Developer account"
    groups: ""
    uid: 1500

users_deleted:
  - username: user
  - username: debian
  - username: cloud-user
```

```yaml
# values.yaml

- hosts: servers
  roles:
    - ansible-role-users
```
