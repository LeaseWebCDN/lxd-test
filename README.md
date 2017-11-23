# Introduction
This repo contains a playground for LXD Linux Containers

# Dependencies
* Virtualbox
* Vagrant

# Deployment

## Vagrant
I use Vagrant in combination with Virtualbox so this playground can be deployed on any system.

### Start Virtualbox machines
Run ```vagrant up``` to turn on all the machines

### Snapshot Virtualbox machines
Run ```vagrant snapshot save init``` to save snapshots called 'init' for all machines.

### Restore snapshots
Run ```vagrant snapshot restore init``` to restore snapshots called 'init' for all machines.

## Ansible
Running the Ansible playbook is as simple as ```ansible-playbook -i hosts --vault-password-file ~/.vault playbook.yml``` as the hosts file already contains a reference to the private keys generated by Vagrant.
