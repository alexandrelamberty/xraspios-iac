# Xraspios Infrastructure as Code

Ansible management for my Raspberry Pis.

## Features

- [Docker](https://www.docker.com/)
- [Portainer](https://www.portainer.io/)

## Execute playbook

```bash
ansible-playbook --inventory-file hosts.ini playbook.yml -u pi --ask-pass
```

## Configure Portainer

Navigate to <http://pi01-srv:9000/>
