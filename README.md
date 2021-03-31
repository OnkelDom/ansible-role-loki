# Ansible Role: Loki

[![ubuntu-18](https://img.shields.io/badge/ubuntu-18.x-orange?style=flat&logo=ubuntu)](https://ubuntu.com/)
[![ubuntu-20](https://img.shields.io/badge/ubuntu-20.x-orange?style=flat&logo=ubuntu)](https://ubuntu.com/)
[![debian-9](https://img.shields.io/badge/debian-9.x-orange?style=flat&logo=debian)](https://www.debian.org/)
[![debian-10](https://img.shields.io/badge/debian-10.x-orange?style=flat&logo=debian)](https://www.debian.org/)
[![centos-7](https://img.shields.io/badge/centos-7.x-orange?style=flat&logo=centos)](https://www.centos.org/)
[![centos-8](https://img.shields.io/badge/centos-8.x-orange?style=flat&logo=centos)](https://www.centos.org/)

[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg?style=flat)](https://opensource.org/licenses/MIT)
[![GitHub issues](https://img.shields.io/github/issues/OnkelDom/ansible-role-loki?style=flat)](https://github.com/OnkelDom/ansible-role-loki/issues)
[![GitHub tag](https://img.shields.io/github/tag/OnkelDom/ansible-role-loki.svg?style=flat)](https://github.com/OnkelDom/ansible-role-loki/tags)
[![GitHub action](https://github.com/OnkelDom/ansible-role-loki/workflows/ansible-lint/badge.svg)](https://github.com/OnkelDom/ansible-role-loki)

## Description

Deploy [loki](https://github.com/grafana/loki) using ansible.

## Requirements

- Ansible >= 2.9 (It might work on previous versions, but we cannot guarantee it)
- Community Packages: `ansible-galaxy collection install community.general`

## Role Variables

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `proxy_env` | {} | Proxy environment variables |
| `loki_version` | 2.2.0 | app version |
| `loki_listen_port` | 3100 | default listen port |
| `loki_listen_address` | 0.0.0.0 | default listen address |
| `loki_config_dir` | /etc/loki | default config dir |
| `loki_config_file` | config.yml | default config file |
| `loki_binary_install_dir` | /usr/local/bin | default bin dir |
| `loki_data_dir` | /var/lib/loki | default data dir |
| `loki_config_log_level` | warn | default log level |
| `loki_system_user` | loki | default system user |
| `loki_system_group` | loki | default system group |
| `loki_user_additional_groups` | adm | additional groups |
| `loki_allow_firewall` | false | allow on firewall |
| `loki_config` | [defaults/main.yml#L14](defaults/main.yml#L14) | loki config |

## Example

### Playbook

```yaml
---
- hosts: all
  roles:
  - onkeldom.loki
```

## Contributing

See [contributor guideline](CONTRIBUTING.md).

## License

This project is licensed under MIT License. See [LICENSE](/LICENSE) for more details.
