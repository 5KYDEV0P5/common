# Ansible Role: common

[![License](https://img.shields.io/badge/License-Apache%202.0-brightgreen.svg)](https://opensource.org/licenses/Apache-2.0)
[![Ansible Role](https://img.shields.io/badge/ansible%20role-skydevops.common-brightgreen.svg)](https://skydevops.co.in)
<!-- [![GitHub last commit](https://img.shields.io/github/last-commit/google/skia.svg)]() -->

[![GitHub tag](https://img.shields.io/github/tag/expressjs/express.svg)](https://github.com/5KYDEV0P5/common)

## Description

Install and configures directory structure and required packages on RedHat/CentOS and Debian/Ubuntu

## Requirements

- Ansible >=2.3
- EPEL Repo for RedHat/CentOS


## Role Variables

All variables which can be overridden are stored in [defaults/main.yml](vars/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `data_dir` | /data | Creates a data directory |
| `apps_dir` | /apps | Creates a application installation directory |
| `apt_libraries_utilities` | ntp, lsof, wget,  zip,<br> python-software-properties,<br> unzip,<br> build-essentials | Install the list of packages needed for Debian/Ubuntu family VM's, add them as named variables |
| `yum_libraries_utilities` | ntp, lsof, wget, dkms,<br> kernel-devel,<br> kernel-tools,<br> zip,<br> unzip,<br> iptables-services,<br> policycoreutils-python,<br>  build-essentials | Install the list of packages needed for RedHat/CentOS family VM's, add them as named variables |


## Example 

### Playbook

Just install Libraries and utilities 

```yaml
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