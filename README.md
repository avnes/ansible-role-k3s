# ansible-role-k3s

![Ansible](https://github.com/avnes/ansible-role-k3s/actions/workflows/ansible.yaml/badge.svg)

Ansible role for installing k3s.

## Requirements

Poetry. Install it from <https://python-poetry.org/docs/>

## Role Variables

```yaml
k3s_version: 3.7.2
k3s_for_all_users: true # If false it will install in in the users ~/bin directory
command_shell: bash         # Must be bash or zsh
```

## Dependencies

None

## Example Playbook

```yaml
- hosts: all
  roles:
     - { role: avnes.k3s }
```

## For pip compability

```bash
poetry export --dev --output requirements.txt
```

## Test

```bash
poetry install
poetry shell
molecule test
```

## License

MIT

## Author Information

<https://github.com/avnes>
