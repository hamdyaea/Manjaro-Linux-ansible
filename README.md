# Manjaro / Arch Linux Updates with Ansible

Developer: Hamdy Abou El Anein
Contact: hamdy.aea@protonmail.com
License: GNU GPL v3 (see LICENSE).

A single-host-at-a-time pacman update playbook, using the maintained
`community.general.pacman` module.

## Setup and validation

```sh
ansible-galaxy collection install -r requirements.yml
ansible-playbook -i localhost, --syntax-check manjaro-update.yml
```

Review your own inventory and confirm all hosts before using it for
a real update. **Do not blindly run a rolling Arch/Manjaro upgrade**
without checking announcements, package conflicts, snapshots and backups.

This repository contains **only the playbook**. No system updates,
privilege escalation or remote commands were executed during
modernization. The original playbook is preserved on branch `old`.
