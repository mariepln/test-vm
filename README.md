# Serveur Web Linux avec VM

## Objectif
Héberger un serveur web Apache sur une VM Ubuntu Server, administré via SSH.

## Architecture
- **VM** : Ubuntu Server 22.04 (VirtualBox)
- **Réseau** : NAT + Host-only (192.168.56.102)
- **Service** : Apache2
- **Administration** : SSH

## Compétences démontrées
- Installation et configuration VM
- Configuration réseau multi-cartes
- Administration Linux à distance (SSH)
- Installation et configuration service web
- Troubleshooting

## Commandes clés utilisées
```bash
# Connexion SSH
ssh admin@192.168.56.102

# Installation Apache
sudo apt install apache2 -y

# Vérification service
systemctl status apache2

# Modification page web
sudo nano /var/www/html/index.html
```

## Résultat
Site web accessible sur http://192.168.56.102


## Jour 2 : Gestion utilisateurs et automatisation

### Utilisateurs créés
- alice (groupe: equipe)
- bob (groupe: equipe)

### Dossier partagé
- `/projets` accessible par le groupe equipe
- Permissions: 770 (lecture/écriture pour le groupe)

### Script de sauvegarde
- Sauvegarde automatique de /var/www/html
- Archive compressée avec horodatage
- Testée avec succès (backup + restore)

### Commandes clés
```bash
# Création utilisateur
sudo useradd -m -s /bin/bash alice

# Gestion groupes
sudo groupadd equipe
sudo usermod -aG equipe alice

# Permissions dossier
sudo chmod 770 /projets
sudo chgrp equipe /projets

# Script backup
tar -czf backup.tar.gz /var/www/html
```
