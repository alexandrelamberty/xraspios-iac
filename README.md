[![ansible-lint](https://github.com/alexandrelamberty/xraspios-iac/actions/workflows/ansible-lint.yml/badge.svg)](https://github.com/alexandrelamberty/xraspios-iac/actions/workflows/ansible-lint.yml)

# Xraspios Infrastructure as Code

Ansible management for my Raspberry Pis.

## Introduction

This project automates the setup and configuration of Raspberry Pi infrastructure using Ansible. It installs Docker, Portainer, and other necessary components to manage and maintain Raspberry Pi clusters efficiently.

## Prerequisites

- Ansible installed on the control machine.
- Raspberry Pis accessible via SSH.
- Basic knowledge of Ansible and Raspberry Pi administration.

## Project Structure

- `playbook.yaml`: Main Ansible playbook containing tasks for Raspberry Pi setup.
- `hosts.ini`: Inventory file listing Raspberry Pi hosts.
- `roles/`: Directory for organizing Ansible roles.
  - `common/`: Role for common configurations across all Raspberry Pis.
    - `tasks/`: Directory containing tasks specific to the `common` role.
      - `main.yaml`: Main tasks file for the `common` role.
    - `defaults/`: Directory containing default variables for the `common` role.
      - `main.yaml`: Default variables file for the `common` role.
- `requirements.txt`: File listing Ansible collections or roles required by the project.

## Usage

1. Clone this repository to your local machine.

2. Modify the `hosts.ini` file to include the IP addresses of your Raspberry Pis.

3. Execute the playbook using the following command:

   ```bash
   ansible-playbook --inventory-file hosts.ini playbook.yml -u pi --ask-pass
   ```

4. Access Portainer by navigating to <http://pi01-srv:9000> in your web browser.
