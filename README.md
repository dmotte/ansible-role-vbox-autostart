# ansible-role-vbox-autostart

[![GitHub Workflow Status](https://img.shields.io/github/workflow/status/dmotte/ansible-role-vbox-autostart/release?logo=github&style=flat-square)](https://github.com/dmotte/ansible-role-vbox-autostart/actions)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-dmotte.vbox__autostart-blueviolet?logo=ansible&style=flat-square)](https://galaxy.ansible.com/dmotte/vbox_autostart)

Ansible role to setup **automatic startup** of **VirtualBox VMs** at system boot.

This role is inspired by the following article: [AutoStart VirtualBox VMs on System Boot on Linux - kifarunix.com](https://kifarunix.com/autostart-virtualbox-vms-on-system-boot-on-linux/).

## Usage

1. Install this role using the `ansible-galaxy` CLI tool
2. You can then include it into the `tasks` section of your *Ansible Playbook* like this:

   ```yaml
   - name: Include the dmotte.vbox_autostart role
     include_role: { name: dmotte.vbox_autostart }
     vars:
       vbox_vms:
         - MyVirtualMachine01
         - AnotherVM02
   ```

> **Note**: if you want to automate also the *VirtualBox* installation on the host, you can use the [oefenweb.virtualbox](https://galaxy.ansible.com/oefenweb/virtualbox) role.

### Role variables

Variable   | Description
---------- | ---
`vbox_vms` | List of the names of the VMs to autostart

## Development

If you want to contribute to this project, you can use the `tests/playbook.yml` file to test the role while editing it.

First of all, **clone this repository** on your local machine:

```bash
git clone https://github.com/dmotte/ansible-role-vbox-autostart.git
```

Then place your inventory file (e.g. `hosts.yml`) inside the `tests` folder.

Edit the `vars` section of the `tests/playbook.yml` file to match your scenario.

Finally, you can **execute the playbook** against your host:

```bash
cd tests/
ansible-playbook -i hosts.yml playbook.yml
```
