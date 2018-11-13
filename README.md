# ansible-inxi

Ansible role to print inxi and neofetch results ;-).

[![Build Status](https://img.shields.io/travis/feffi/ansible-inxi.svg)](https://travis-ci.org/feffi/ansible-inxi) [![Github All Releases](https://img.shields.io/github/downloads/feffi/ansible-inxi/total.svg)](https://github.com/feffi/ansible-inxi) [![GitHub forks](https://img.shields.io/github/forks/feffi/ansible-inxi.svg?style=social&label=Fork)](https://github.com/feffi/ansible-inxi) [![GitHub stars](https://img.shields.io/github/stars/feffi/ansible-inxi.svg?style=social&label=Star)](https://github.com/feffi/ansible-inxi) [![GitHub watchers](https://img.shields.io/github/watchers/feffi/ansible-inxi.svg?style=social&label=Watch)](https://github.com/feffi/ansible-inxi) [![Twitter Follow](https://img.shields.io/twitter/follow/feffi1.svg?style=social&label=Follow)](https://twitter.com/feffi1) [![License](http://img.shields.io/:license-mit-blue.svg)](https://github.com/feffi/ansible-inxi/blob/master/LICENSE)
## Requirements

- Ansible 2.7.1
- pacman ;-)

### ansible.cfg

```yaml
hash_behaviour = merge
```

## Install

Just add the role to your ``requirements.yml`` file:

```yaml
- src: https://github.com/feffi/ansible-inxi.git
  name: ansible-inxi
```

## Role Defaults Variables

```yaml
ansible_inxi: {
  # The inxi options to print
  options: "-Ffmns --slots --usb"
  # The AUR compile user
  owner: {
    name: "feffi",
    group: "feffi"
  },
}
```

Example:

```yaml
- hosts: all
  vars:
    ansible_inxi:
      # The inxi options to print
      options: "-Ffmns --slots --usb"
      # The AUR compile user
      owner:
        name: "feffi"
        group: "feffi"
  roles:
    - { role: ansible-inxi }
```
