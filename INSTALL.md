![Logo John the Ripper](Images/JtR.png)

# DOCUMENTATION ADMINISTRATEUR

## Prérequis techniques

1. Connaissances minimum à travailller sur un terminal sous linux
2. Un serveur:
windows server 2022, identifié WINSERV01, sous le compte: Administrator avec le mot de passe Azerty1* et l'adresse IP fixe: 172.16.10.10 en masque sous réseau: 255.255.255.0,
installation dessus pour récuperer les fichiers "PsExec" (voire configuration).
3. un client:
Sous ubuntu 22.04, identifié clilin01, sous le compte utilisateur: wilder avec le mot de passe Azerty1* et l'adresse IP fixe: 172.16.10.20 en masque sous réseau: 255.255.255.0, installation dessus "samdump2" (voire configuration). 
4. Systèmes d'exploitation supportés :
Linux/Unix : John the Ripper a été initialement conçu pour fonctionner sur ces systèmes (Ubuntu, Debian, Fedora, etc.).
Windows : Il existe des versions adaptées pour Windows, mais l'utilisation est souvent plus fluide sous Linux.
macOS : Peut être utilisé avec les bons outils de compilation.
5. Dépendances :
Compilateur : Si vous compilez à partir du code source, vous aurez besoin d’un compilateur comme gcc sur Linux ou Xcode sur macOS. Sur Windows, il peut nécessiter Cygwin ou MinGW.
OpenSSL : Pour les algorithmes de hachage spécifiques, l'outil peut s'appuyer sur OpenSSL.
Git : Si vous téléchargez la version depuis le dépôt GitHub.
6. Matériel :
Processeur multicœur : John the Ripper est capable de tirer parti de plusieurs cœurs CPU.
GPU (optionnel) : Des versions comme John the Ripper Jumbo supportent l’utilisation de GPU via OpenCL ou CUDA pour accélérer le craquage de mots de passe.
RAM : Plus vous avez de RAM, plus vous pouvez gérer des fichiers de hachage volumineux.
7. Versions spécifiques :
John the Ripper standard : Pour les besoins basiques de test de mots de passe.
John the Ripper Jumbo : Cette version est enrichie de nombreux patchs et supporte un plus grand nombre d'algorithmes et de formats de fichiers (MD5, SHA-1, NTLM, etc.).
8. Algorithmes supportés :
MD5, SHA-1, SHA-256, bcrypt, DES, NTLM, Kerberos, et bien d’autres.
9. Accès à un fichier de hachage :
John the Ripper ne fonctionne pas directement sur des mots de passe en clair mais sur des fichiers contenant des hashs (comme /etc/shadow sous Linux, ou des dumps de bases de données).
10. Commandes de base :
Il faut connaître les commandes en ligne de John the Ripper pour craquer les mots de passe, lancer des attaques par dictionnaire ou par force brute(allez voir USER_GUIDE).
---
## Installation et configuration 

### -*Installation* 
1. Mise à jour du système
Avant d'installer un nouveau logiciel, il est recommandé de mettre à jour votre système pour vous assurer que vous disposez des dernières versions des paquets. Ouvrez un terminal et exécutez la commande suivante :
```sudo apt update && sudo apt upgrade -y```

![image](https://github.com/WildCodeSchool/TSSR-2409-JAUNE-P1-G3-SecurisationDeMotDePasse/blob/main/Images/Capture%20d%E2%80%99%C3%A9cran%20dinstall%20john-the%20ripper%204.png)

3. Installation de John the Ripper à partir des dépôts Ubuntu
John the Ripper est disponible dans les dépôts officiels d'Ubuntu. Vous pouvez l'installer directement à partir de ces dépôts avec la commande suivante :
```sudo snap install john-the-ripper```
 
![image](https://github.com/WildCodeSchool/TSSR-2409-JAUNE-P1-G3-SecurisationDeMotDePasse/blob/main/Images/Capture%20d%E2%80%99%C3%A9cran%20dinstall%20john-the%20ripper2.png)

5. Vérification de l'installation
Une fois installé, vous pouvez vérifier si John the Ripper est correctement installé en tapant la commande suivante dans le terminal :```john --version```

![image](https://github.com/WildCodeSchool/TSSR-2409-JAUNE-P1-G3-SecurisationDeMotDePasse/blob/main/Images/Capture%20d%E2%80%99%C3%A9cran%20d'install%20john-the-ripper%206.png)

Cela affichera la version installée de John the Ripper.

![image](https://github.com/WildCodeSchool/TSSR-2409-JAUNE-P1-G3-SecurisationDeMotDePasse/blob/main/Images/Capture%20d%E2%80%99%C3%A9cran%20d'install%20john-the-ripper%205%20.png)


### -*Configuration*

- création alias 'zip2john' en tapant la commande suivante dans le terminal :```sudo snap alias john-the-ripper.zip2john zip2john```

![image](https://github.com/WildCodeSchool/TSSR-2409-JAUNE-P1-G3-SecurisationDeMotDePasse/blob/main/Images/INSTALL3.png)
  

---
## FAQ
