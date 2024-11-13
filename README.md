# Ansible Role: makemkv

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Install [makemkv](https://www.makemkv.com) on Debian based systems with ansible. This role will download the makemkv-bin and makemkv-oss archive files and use `community.general.make` to install

## Requirements

`community.general`

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

Base download url:

```yaml
makemkv_url: https://www.makemkv.com/download
```

Set the full url for both the bin and oss archives:

```yaml
makemkv_bin_tar: "{{ makemkv_url }}/makemkv-bin-{{ makemkv_version }}.tar.gz"

makemkv_oss_tar: "{{ makemkv_url }}/makemkv-oss-{{ makemkv_version }}.tar.gz"
```

Version of makemkv to download and install:

```yaml
makemkv_version: 1.17.8
```

## Example Playbook

``` yaml
- hosts: all
  roles:
    - role: jeffreyjs.makemkv
```

## License

MIT / BSD

## Author Information

[Jeffrey Swindel](https://github.com/jeffreyjs)
