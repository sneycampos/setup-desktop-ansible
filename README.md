# Ubuntu Desktop Configuration

This Ansible playbook automates the process of setting up an Ubuntu desktop environment. It installs essential packages, repositories, and configurations to streamline your workflow.

## Prerequisites

- Ansible installed on your local machine.
- Ubuntu Desktop operating system.

## Installing Ansible

You can install Ansible on Ubuntu using the following steps:

1. Update your package index:

    ```bash
    sudo apt update
    ```

2. Install Ansible:

    ```bash
    sudo apt install ansible
    ```

3. Verify the installation by checking the Ansible version:

    ```bash
    ansible --version
    ```

## Usage

1. Clone this repository to your local machine:

    ```bash
    git clone git@github.com:sneycampos/setup-desktop-ansible.git
    ```

2. Navigate to the cloned repository:

    ```bash
    cd setup-desktop-ansible
    ```

3. Execute the Ansible playbook:

    Tools
    ```bash
    ansible-playbook tools.yml --ask-become-pass
    ```

    Setup Docker, Docker Compose and New User
    ```bash
    ansible-playbook setup.yml --ask-become-pass
    ```

## What This Playbooks Does

- Updates the apt cache.
- Adds specified apt repositories.
- Installs essential apt packages:
    - curl
    - wget
    - gdebi
    - git
    - zsh
    - htop
    - docker
    - docker compose
    - flameshot
    - firefox
    - libreoffice
    - copyq
- Installs specified snap packages:
    - code
    - discord
    - postman
    - slack
    - spotify
    - telegram-desktop
- Downloads and installs the Warp Terminal.
- Adds the current user to the docker group to run docker without sudo
- Installs NVM (Node Version Manager) to manage multiple Node.js versions.

## Customization

You can customize this playbook by modifying the `tools.yml` and `docker.yml` files to include additional apt repositories, packages, or configurations according to your requirements.

## Notes

- Ensure that you have necessary permissions to execute the playbook and install packages.
- Review the playbook before execution to understand the changes it will make to your system.

## Disclaimer

This playbook is provided "as is" and without warranty. Use it at your own risk.
