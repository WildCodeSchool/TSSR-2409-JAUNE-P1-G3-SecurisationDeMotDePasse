# TSSR-2409-JAUNE-P1-G3-SecurisationDeMotDePasse
## Sécurisation de mot de passe

### **1- Présentation du projet, objectifs finaux**
Le projet est d'installer un logiciel de décryptage de mot de passe, John The Ripper, sur une machine Client, connecté à un Serveur et d'effectuer une attaque par dictionnaire sur le mot de passe d'un dossier zip sur un serveur.  

John The Ripper (souvent abrégé JtR ou John) est un logiciel libre  et [open source](https://github.com/openwall/john) de cassage de mots de passe développé à l'origine pour les systèmes Unix. Il est désormais disponible sur de nombreuses plateformes, dont Windows, Linux et macOS. Il s'agit d'un puissant outil de craquage de mots de passe largement utilisé dans le domaine de la sécurité informatique.


Les **objectifs** sont :  
- Avoir le serveur et le client fonctionnels et connectés entre eux.  
- Avoir le logiciel John The Ripper installé chez le client et fonctionnel.
- Configurer un dossier de partage sur le serveur, accessible par un client.  
- Effectuer une attaque par dictionnaire sur le mot de passe d'un dossier zip.
- Analyser les résultats pour en déduire la robustesse des mots de passe.  
- Fournir les livrables (README.md, INSTALL.md et USER_GUIDE.md)  

L'**objectif final** est de sensibiliser les utilisateurs à l'utilisation de mots de passe forts.  


### **2- Introduction : mise en contexte**
John the Ripper est couramment utilisé pour :

  -  Tester la robustesse des mots de passe dans le cadre d'audits de sécurité
  -  Récupérer des mots de passe perdus
  -  Démontrer les risques liés aux mots de passe faibles

### **3- Membres du groupe de projet**

Pour le sprint 1 : 

| Équipe     | Rôle   | Missions                                                                                      |
| ---------- | ------ | --------------------------------------------------------------------------------------------- |
| Arnaud     | PO     | Configuration de la VM Client, Création de la documentation générale, Installation de John et des VM  |
| Christophe | SM     | Recherche sur les logiciels, Création des documentations User et Admin, Installation de John et des VM  |
| Charlène   | Membre | Recherche sur les logiciels, Création de la présentation, Installation de John et des VM                 |
| Mahmoud    | Membre | Configuration de la VM Serveur, Installation de John et des VM                                        |

Pour le sprint 2 :

| Équipe     | Rôle   | Missions                                                                                      |
| ---------- | ------ | --------------------------------------------------------------------------------------------- |
| Arnaud     | Member |     |
| Christophe | Member |   |
| Charlène   | SM     |                 |
| Mahmoud    | PO     |       |

### 4- Choix techniques 

Le choix du Serveur a été imposé par le client : Windows Server 2022.  
Le choix due l'OS Client a été imposé par le client : Ubuntu. Nous avons priviligié Ubuntu 22.04 LTS car, en service depuis plusieurs années, elle présente de plus fortes probabilitéss d'être présente sur une machine client.   
Le choix du logiciel s'est porté sur John the Ripper car il dispose d'une fonctionnalité d'autodétection des fonctions de hachage utilisées pour stocker les mots de passe. Il est utilisé par une importante communauté et il propose de nombreuse fonctions de hachage, tel que:
- Les algorithmes classiques :
  - MD5
  - SHA (différentes variantes)
  - UNIX crypt(3)
  - DES traditionnel
  - Blowfish
- Hachages spécifiques aux systèmes :
  - Windows LM (DES-based)
  -  NTLM (pour les versions récentes de Windows)
  -  erberos/AFS
  -  FreeBSD MD5-based (utilisé aussi par Linux et Cisco IOS)
  -  OpenBSD Blowfish-based
  -  SHA-crypt (utilisé par les versions récentes de Fedora et Ubuntu)
  -  SUNMD5 (utilisé par Solaris)

### 5- Difficultés rencontrées : problèmes techniques rencontrés
  
  - 1 Problème rencontré concernant l'accès aux fichiers .zip protégés par mots de passe, qui sont stocké sur le serveur Windows depuis la machine cliente.
    
  - 2 Problème rencontré avec l'utilisation des différentes versions de VirtualBox. Incapacité à partager les images OVA des machines virtuelles et ainsi bénéficier d'une version commune du Lab pour effectuer les tests d'utilisation de JTH.
    
### 6- Solutions trouvées : Solutions et alternatives trouvées
  
  - 1 La solution choisie consiste à créer un dossier partagé entre les deux machines virtuelles qui permet au client de récupérer les fichiers à craquer, à l'aide de JtH.
    
  - 2 La solution choisie a été de créer des machines virtuelles individuelles pour pouvoir réaliser les tests du logiciel de manière locale.

### 7- Améliorations possibles

  - 1 
  
  - 2 L'amélioration possible serait de revenir à une version antérieure commune qui présenterait une plus grande stabilité.

Préparation des fichiers de dictionnaire:Téléchargez ou créez des fichiers de dictionnaire contenant les mots de passe à tester.
##### Utilisation de John the Ripper
###### 1- Utilisation de John the Ripper :Exécutez John the Ripper avec le hash extrait et le fichier de dictionnaire.

 3-Extraction du hash : Utilisez un outil John the Ripper pour extraire le hash du fichier zippé, ce qui permet à John the Ripper de l'analyser.
###### 4-Préparation des fichiers de dictionnaire:Téléchargez ou créez des fichiers de dictionnaire contenant les mots de passe à tester.
##### Utilisation de John the Ripper
###### 1- Utilisation de John the Ripper :Exécutez John the Ripper avec le hash extrait et le fichier de dictionnaire.
