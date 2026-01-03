#Connexion navigation
ssh user@IP                    # Connexion SSH
exit                           # Déconnexion
hostname                       # Nom de la machine
whoami                         # Utilisateur actuel
pwd                            # Dossier actuel
#Gestion services
systemctl status SERVICE       # Statut service
systemctl start SERVICE        # Démarrer
systemctl stop SERVICE         # Arrêter
systemctl restart SERVICE      # Redémarrer
#Gestionn users
sudo useradd -m -s /bin/bash USER    # Créer utilisateur
sudo passwd USER                      # Définir mot de passe
sudo groupadd GROUP                   # Créer groupe
sudo usermod -aG GROUP USER           # Ajouter au groupe
groups USER                           # Voir groupes d'un user
#Permissions
chmod 770 DOSSIER             # Permissions rwxrwx---
chown USER:GROUP FICHIER      # Changer propriétaire
chgrp GROUP DOSSIER           # Changer groupe
#Fichiers et dossiers
ls -lh                        # Lister avec détails
mkdir DOSSIER                 # Créer dossier
rm FICHIER                    # Supprimer fichier
cp SOURCE DEST                # Copier
mv SOURCE DEST                # Déplacer/renommer
cat FICHIER                   # Afficher contenu
#Networking
ip addr show                  # Voir IPs
ping IP                       # Tester connectivité
