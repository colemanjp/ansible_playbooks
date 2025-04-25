# Ansible Playbooks

This isn't beautiful production ready code, but it serves to run a scalable zoo of personal machines. Secrets are encrypted with ansible vault.

## Running 

Run everything `ansible-playbook site.yml -i hosts -u root --vault-password-file vault-pass.txt`

Run a single group `ansible-playbook site.yml -i hosts -u root -l kali --vault-password-file vault-pass.txt`

Run WSL playbook from WSL using a local connection `ansible-playbook roles/wsl/tasks/main.yml --connection=local`

## group_vars

all.yml and kali.yml each contain one variable: `myuser`

## OS

- servers and laptops are Fedora
- axiom and proxmox are Debian
- kali is Kali
- wsl is Kali running on wsl
