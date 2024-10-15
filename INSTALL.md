![Logo John the Ripper](Images/JtR.png)

# DOCUMENTATION ADMINISTRATEUR

## Prérequis techniques
1. Systèmes d'exploitation supportés :
Linux/Unix : John the Ripper a été initialement conçu pour fonctionner sur ces systèmes (Ubuntu, Debian, Fedora, etc.).
Windows : Il existe des versions adaptées pour Windows, mais l'utilisation est souvent plus fluide sous Linux.
macOS : Peut être utilisé avec les bons outils de compilation.
2. Dépendances :
Compilateur : Si vous compilez à partir du code source, vous aurez besoin d’un compilateur comme gcc sur Linux ou Xcode sur macOS. Sur Windows, il peut nécessiter Cygwin ou MinGW.
OpenSSL : Pour les algorithmes de hachage spécifiques, l'outil peut s'appuyer sur OpenSSL.
Git : Si vous téléchargez la version depuis le dépôt GitHub.
3. Matériel :
Processeur multicœur : John the Ripper est capable de tirer parti de plusieurs cœurs CPU.
GPU (optionnel) : Des versions comme John the Ripper Jumbo supportent l’utilisation de GPU via OpenCL ou CUDA pour accélérer le craquage de mots de passe.
RAM : Plus vous avez de RAM, plus vous pouvez gérer des fichiers de hachage volumineux.
4. Versions spécifiques :
John the Ripper standard : Pour les besoins basiques de test de mots de passe.
John the Ripper Jumbo : Cette version est enrichie de nombreux patchs et supporte un plus grand nombre d'algorithmes et de formats de fichiers (MD5, SHA-1, NTLM, etc.).
5. Algorithmes supportés :
MD5, SHA-1, SHA-256, bcrypt, DES, NTLM, Kerberos, et bien d’autres.
6. Accès à un fichier de hachage :
John the Ripper ne fonctionne pas directement sur des mots de passe en clair mais sur des fichiers contenant des hashs (comme /etc/shadow sous Linux, ou des dumps de bases de données).
7. Commandes de base :
Il faut connaître les commandes en ligne de John the Ripper pour craquer les mots de passe, lancer des attaques par dictionnaire ou par force brute(allez voir USER_GUIDE).
---
## Installation et configuration 

### -*Installation*  

### -*Configuration*

---
## FAQ
