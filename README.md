# Raspberry Pi Project

This project is designed to automate the installation of Pi-hole and a media center on Raspberry Pi Zero and Raspberry Pi 4 devices.

## Overview

The project uses Ansible for automation. It includes tasks for setting up the necessary software, including Python3, pip3, and Docker, as well as tasks for downloading and executing the Docker installation script.

The main components of the project are:

- Requirements : Docker to run my tools as containers
- Pi-hole: A network-wide ad blocking application. It will be installed on the Raspberry Pi Zero.
- Media Center: A software application designed to organize and play media. It will be installed on the Raspberry Pi 4.

## Requirements

- Raspberry Pi Zero and Raspberry Pi 4 devices with a fresh install of the latest Raspberry Pi OS (No desktop environment needed).
- An ssh access to the Raspberry pi on the control machine.
- Ansible installed on the control machine.

## Install ansible

```bash
# Create a python venv
python3 -m virtualenv $PWD
source $PWD/bin/activate
pip3 install ansible
```

## Usage

To use this project, first update the Ansible inventory file with the hostnames of your Raspberry Pi devices.
Then, run the Ansible playbook:

```bash
ansible-playbook -i inventories/inventory.yaml main.yaml
