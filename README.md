# MacOS Setup with Ansible

This repository contains an Ansible configuration for setting up a Mac from scratch. It's primary purpose is setting up a new Mac from scratch, but I endeavor to also use it for adding new software as I go so that it remains up to date. At the moment it's being used for setting up M1 based Macs running MacOS Monterey.

## Getting Started
There's a simple shell script in `warmup` which will perform the initial steps of:
1. Installing brew
2. Installing ansible

After `warmup` is done and the base software is installed then run the playbook

```bash
ansible-playbook -i "localhost," -c local ansible_osx.yml --ask-become-pass
```