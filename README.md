# ansible-rpi-cluster

This is a basic collection of Ansible playbooks to perform common tasks in a Raspberry Pi cluster.

Feel free to contribute other common tasks that would be useful.

## Requirements

* [Ansible](http://www.ansible.com/)

## Installation

Clone the repository

    git clone https://github.com/dastergon/ansible-rpi-cluster.git

Copy `hosts.sample` to `hosts`

    cp hosts.sample hosts

Edit `hosts` file with your own topology. For example:

```
[all:vars]
ansible_user=pi
ansible_ssh_pass=addyourpassword

[picluster]
192.168.1.2
192.168.1.3
192.168.1.4
192.168.1.5
```

Run any of the playbooks.

## Shutdown

To shutdown all your RPis execute the following playbook:

    ansible-playbook playbooks/shutdown.yml -i hosts

## Reboot

To shutdown all your RPis execute the following playbook:

    ansible-playbook playbooks/reboot.yml -i hosts
