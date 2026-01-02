# Ansible Playbooks

Secrets are encrypted with ansible vault.

## Running 

Run everything `ansible-playbook site.yml -i hosts -u root --vault-password-file vault-pass.txt`

Run a single group `ansible-playbook site.yml -i hosts -u root -l kali --vault-password-file vault-pass.txt`

Run WSL playbook from WSL using a local connection `ansible-playbook roles/wsl/tasks/main.yml --connection=local`

## group_vars

all.yml and kali.yml are encrypted and contain the important `myuser` variable and some mail aliases

## OS

- vps and laptops are Fedora
- axiom and proxmox are Debian
- kali is Kali
- wsl is Kali running on wsl
