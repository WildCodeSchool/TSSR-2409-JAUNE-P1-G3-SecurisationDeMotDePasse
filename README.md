# TSSR-2409-JAUNE-P1-G3-SecurisationDeMotDePasse
## Sécurisation de mot de passe

### **1- Présentation du projet, objectifs finaux**
Le projet est d'installer un logiciel de décryptage de mot de passe, John The Ripper, sur une machine Client, connecté à un Serveur et d'effectuer une attaque par dictionnaire sur le mot de passe d'un dossier zip sur un serveur.  

John The Ripper est   ????


Les **objectifs** sont :  
- Avoir le serveur et le client fonctionnels et connectés entre eux.  
- Avoir le logiciel John The Ripper installé chez le client et fonctionnel.
- Configurer un dossier de partage sur le serveur, accessible par un client.  
- Effectuer une attaque par dictionnaire sur le mot de passe d'un dossier zip.
- Analyser les résultats pour en déduire la robustesse des mots de passe.  
- Fournir les livrables (README.md, INSTALL.md et USER_GUIDE.md)  

L'**objectif final** est de sensibiliser les utilisateurs à l'utilisation de mots de passe forts.  


### 2- Introduction : mise en contexte

### 3- Membres du groupe de projet 

Pour le sprint 1 : 

| Équipe     | Rôle   | Missions                                                                                      |
| ---------- | ------ | --------------------------------------------------------------------------------------------- |
| Arnaud     | PO     | Configuratiion de la VM Client, Création de la documentation générale, Installation de John   |
| Christophe | SM     | Recherche sur les logiciels, Création des documentations User et Admin, Installation de John  |
| Charlène   | Membre | Recherche sur les logiciels, Installation de John, Création de la présentation                |
| Mahmoud    | Membre | Configuration de la VM Serveur, Installation de John                                          |

Pour le sprint 2 :

| Équipe     | Rôle   | Missions                                                                                      |
| ---------- | ------ | --------------------------------------------------------------------------------------------- |
| Arnaud     | PO     |     |
| Christophe | SM     |   |
| Charlène   | Membre |                 |
| Mahmoud    | Membre |       |

### 4- Choix techniques 

Le choix du Serveur a été imposé par le client : Windows Server 2022.  
Le choix due l'OS Client a été imposé par le client : Ubuntu. Nous avons priviligié Ubuntu 22.04 LTS car, en service depuis plusieurs années, elle présente de plus fortes probabilitéss d'être présente sur une machine client.   
Le choix du logiciel s'est porté sur John The Ripper car il est plus ancien et plus soutenu, et il propose plus de fonctions de hachage, en particulier le Yescript, et 

### 5- Difficultés rencontrées : problèmes techniques rencontrés

### 6- Solutions trouvées : Solutions et alternatives trouvées

### 7- Améliorations possibles






Préparation des fichiers de dictionnaire:Téléchargez ou créez des fichiers de dictionnaire contenant les mots de passe à tester.
##### Utilisation de John the Ripper
###### 1- Utilisation de John the Ripper :Exécutez John the Ripper avec le hash extrait et le fichier de dictionnaire.

 3-Extraction du hash : Utilisez un outil John the Ripper pour extraire le hash du fichier zippé, ce qui permet à John the Ripper de l'analyser.
###### 4-Préparation des fichiers de dictionnaire:Téléchargez ou créez des fichiers de dictionnaire contenant les mots de passe à tester.
##### Utilisation de John the Ripper
###### 1- Utilisation de John the Ripper :Exécutez John the Ripper avec le hash extrait et le fichier de dictionnaire.
