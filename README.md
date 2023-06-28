# ansible-role-vbox-autostart

[![GitHub latest release](https://img.shields.io/github/v/release/dmotte/ansible-role-vbox-autostart?logo=github&style=flat-square)](https://github.com/dmotte/ansible-role-vbox-autostart/actions)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-dmotte.vbox__autostart-blueviolet?logo=ansible&style=flat-square)](https://galaxy.ansible.com/dmotte/vbox_autostart)

Ansible role to setup **automatic startup** of **VirtualBox VMs** at system boot.

This role is inspired by the following article: [AutoStart VirtualBox VMs on System Boot on Linux - kifarunix.com](https://kifarunix.com/autostart-virtualbox-vms-on-system-boot-on-linux/).

## Usage

1. Install this role using the `ansible-galaxy` CLI tool
2. You can then include it into the `tasks` section of your _Ansible Playbook_. See [`test/playbook.yml`](test/playbook.yml) for an example of how to do that. Remember to replace the role name with `dmotte.vbox_autostart`.

> **Note**: this role must be run as root (`ansible_become: true`).

> **Note**: if you want to automate also the _VirtualBox_ installation on the host, you can use the [oefenweb.virtualbox](https://galaxy.ansible.com/oefenweb/virtualbox) role.

### Role variables

See [`defaults/main.yml`](defaults/main.yml).

## Development

If you want to contribute to this project, you can use the [`test/playbook.yml`](test/playbook.yml) file to test the role while editing it.

Place your inventory file (e.g. `hosts.yml`) inside the `test` folder.

Edit the `vars` section of the [`test/playbook.yml`](test/playbook.yml) file to match your scenario.

You can then **execute the playbook** against your host:

```bash
cd test/
ansible-playbook -i hosts.yml playbook.yml
```
