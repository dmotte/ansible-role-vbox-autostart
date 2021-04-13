# ansible-role-vbox-autostart

[![GitHub Workflow Status](https://img.shields.io/github/workflow/status/dmotte/ansible-role-vbox-autostart/release?logo=github&style=flat-square)](https://github.com/dmotte/ansible-role-vbox-autostart/actions)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-dmotte.vbox__autostart-blueviolet?logo=ansible&style=flat-square)](https://galaxy.ansible.com/dmotte/vbox_autostart)

Ansible role to setup **automatic startup** of **VirtualBox VMs** at system boot.

TODO https://kifarunix.com/autostart-virtualbox-vms-on-system-boot-on-linux/
TODO oefenweb.virtualbox

## Usage

1. Install this role using the `ansible-galaxy` CLI tool
2. You can then include it into the `tasks` section of your *Ansible Playbook* like this:

   ```yaml
   - name: Include the dmotte.vbox_autostart role
     include_role: { name: dmotte.vbox_autostart }
     vars:
       TODO username: TODO
       TODO vms list: TODO
   ```

### Role variables

TODO

## Development

If you want to contribute to this project, you can use the `playbook.yml` file to test the role while editing it.

First of all, **clone this repository** on your local machine:

```bash
git clone https://github.com/dmotte/ansible-role-vbox-autostart.git
```

Then place your inventory file (e.g. `hosts.yml`) inside the `tests` folder.

Finally, you can **execute the playbook** against your host:

```bash
cd tests/
ansible-playbook -i hosts.yml playbook.yml
```
