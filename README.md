#  CodeBleu_Server - Serveur Central de Gestion des Urgences

##  Description
Serveur centralisé qui gère le système de déclaration et notification d'urgences médicales "Code Bleu". Il agit comme un intermédiaire entre les infirmiers (via CORBA) et les médecins (via RMI).

##  Architecture
- **Serveur CORBA** : Expose des services pour les déclarations d'urgence
- **Serveur RMI** : Gère les notifications push vers les médecins
- **Gestionnaire d'urgences** : Stocke et traite les données d'urgence
- 
##  Fonctionnalités
1. **Réception d'urgences** depuis les clients infirmiers (CORBA)
2. **Stockage centralisé** des urgences déclarées
3. **Notification en temps réel** aux médecins connectés (RMI Callback)
4. **Gestion des connexions** des clients médecin

## Lancement
# 1. Générer les stubs CORBA depuis Urgence.idl
idlj -fall Urgence.idl

# 2. Démarrer le serveur
 main.ServerMain
