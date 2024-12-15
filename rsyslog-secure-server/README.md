# RSyslog Secure Server

Ce projet configure automatiquement un serveur RSyslog centralisé sécurisé avec Ansible, ainsi que ses clients.

## Structure du Projet
- **ansible.cfg** : Configuration Ansible.
- **inventory/** : Inventaire des hôtes.
- **group_vars/** : Variables globales.
- **roles/** : Rôles Ansible pour le serveur et les clients.
- **playbooks/** : Playbooks principaux.

## Commandes

### 1. Configurer le serveur
```bash
ansible-playbook -i inventory/clients.yml playbooks/setup_server.yml
```

### 2. Configurer les clients
```bash
ansible-playbook -i inventory/clients.yml playbooks/setup_clients.yml
```

## Remarques
- Assurez-vous que les hôtes sont accessibles via SSH.
- Remplissez les IP dans `inventory/clients.yml`.
