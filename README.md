# Ansible Role: common

[![License](https://img.shields.io/badge/License-Apache%202.0-brightgreen.svg)](https://opensource.org/licenses/Apache-2.0)

## Description

Install and configures directory structure and required packages on RedHat/CentOS and Debian/Ubuntu

## Requirements

- Ansible >=2.3
- EPEL Repo for RedHat/CentOS


## Role Variables

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `data_dir` | /data | Creates a data directory |
| `apps_dir` | /apps | Creates a application installation directory |
| `apt_libraries_utilities` | | Install the list of packages needed for Debian family VM's |

Libraries and utilities for Debian/Ubuntu systems
```
apt_libraries_utilities:
- ntp
- lsof
- wget
- python-software-properties
- zip
- unzip
- build-essential
```
Libraries and utilities for RedHat/CentOS
```
yum_libraries_utilities:
- ntp
- lsof
- wget
- policycoreutils-python
- zip
- unzip
- vim
- dkms
- iptables-services
- kernel-devel
- kernel-tools
```

## Example 

### Playbook

Just install Libraries and utilities 

```
- hosts: all
  become: yes
  gather_facts: yes
  roles:
    - role: common
```

## License


Licensed under the Apache License V2.0. See the [LICENSE file](LICENSE) for details.

## Author Information

You can find me on Twitter: [@skydevops](https://twitter.com/skydevops)

## Contributors

- Shashi Yebbare ([@skydevops](https://twitter.com/skydevops))