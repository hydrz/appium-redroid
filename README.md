# Appium-Redroid

## Ansible Playbook

The goal is easily install a Kubernetes cluster on machines running:

- [X] Debian
- [X] Ubuntu
- [X] CentOS

on processor architecture:

- [X] x64
- [X] arm64
- [X] armhf

## System requirements

Deployment environment must have Ansible 2.4.0+
Master and nodes must have passwordless SSH access

## Usage


Edit `inventory.ini` to match the system information gathered above. For example:

```bash
[node]
192.16.35.[10:11]
```

Start provisioning of the cluster using the following command:

```bash
ansible-playbook site.yml -i inventory.ini
```

## Reset

```bash
ansible-playbook reset.yml -i inventory.ini
```
