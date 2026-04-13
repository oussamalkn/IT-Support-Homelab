# Windows Server 2022 Installation — DC-01

## Objectif
Installer Windows Server 2022 comme base pour le Domain Controller.

## Spécifications VM
- RAM : 3 GB
- CPU : 2 vCPU
- Disque : 60 GB
- Réseau : Internal Network — labnet
- IP statique : 192.168.10.2

## Étapes d'installation
1. Créer la VM dans VirtualBox
2. Attacher l'ISO Windows Server 2022 Evaluation
3. Désactiver l'Unattended Installation (supprimer le floppy)
4. Choisir : Windows Server 2022 Standard Evaluation (Desktop Experience)
5. Installation Custom sur disque vide
6. Créer mot de passe Administrator fort

## Configuration post-installation
- IP statique configurée : 192.168.10.2/24
- Gateway : 192.168.10.1
- DNS : 127.0.0.1 (lui-même après AD DS)
- Renommage serveur : DC-01

## Réseau VirtualBox
- Adapter 1 : Internal Network
- Nom réseau : labnet

## Screenshot
![Windows Server Installation]
