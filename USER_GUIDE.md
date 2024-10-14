![Logo John the Ripper](Images/JtR.png)

# DOCUMENTATION UTILISATEUR

## Notions juridiques

### Code pénal: Livre III : Des crimes et délits contre les biens (Articles 311-1 à 324-9)

#### Chapitre III : Des atteintes aux systèmes de traitement automatisé de données (Articles 323-1 à 323-8)

 - **Article 323-1** (Modifié par LOI n°2023-22 du 24 janvier 2023 - art. 6)
    - Le fait d'accéder ou de se maintenir, frauduleusement, dans tout ou partie d'un système de traitement automatisé de données est puni de trois ans d'emprisonnement et de 100 000 € d'amende.

    - Lorsqu'il en est résulté soit la suppression ou la modification de données contenues dans le système, soit une altération du fonctionnement de ce système, la peine est de cinq ans d'emprisonnement et de 150 000 € d'amende.

    - Lorsque les infractions prévues aux deux premiers alinéas ont été commises à l'encontre d'un système de traitement automatisé de données à caractère personnel mis en œuvre par l'Etat, la peine est portée à sept ans d'emprisonnement et à 300 000 € d'amende.
     
 - **Article 323-2** (Modifié par LOI n°2015-912 du 24 juillet 2015 - art. 4)

    - Le fait d'entraver ou de fausser le fonctionnement d'un système de traitement automatisé de données est puni de cinq ans d'emprisonnement et de 150 000 € d'amende.

    - Lorsque cette infraction a été commise à l'encontre d'un système de traitement automatisé de données à caractère personnel mis en œuvre par l'Etat, la peine est portée à sept ans d'emprisonnement et à 300 000 € d'amende. 
    
 - **Article 323-3** (Modifié par LOI n°2015-912 du 24 juillet 2015 - art. 4)
    - Le fait d'introduire frauduleusement des données dans un système de traitement automatisé, d'extraire, de détenir, de reproduire, de transmettre, de supprimer ou de modifier frauduleusement les données qu'il contient est puni de cinq ans d'emprisonnement et de 150 000 € d'amende.

    - Lorsque cette infraction a été commise à l'encontre d'un système de traitement automatisé de données à caractère personnel mis en œuvre par l'Etat, la peine est portée à sept ans d'emprisonnement et à 300 000 € d'amende.
    
    (Source: [Legifrance.gouv.fr](https://www.legifrance.gouv.fr/codes/section_lc/LEGITEXT000006070719/LEGISCTA000006117598/#LEGISCTA000006117598))


## Utilisation de base :

Il faut plusieurs étapes our vérifier la robustesse du mot de passe d'un fichier zippé. 
Allez tout d'abord dans votre Terminal Linux.  

La première est d'extraire le mot de passe de votre fichier (ici pour l'exemple, ``` dossier.zip ```. Pour cela, utilisez : ```zip2john dossier.zip > hash.txt ```.
![Première commande à effectuer](Images/Base_Etape1.png)

Pour information, ton nouveau fichier ``hash.txt``` devrait ressembler à ceci :
![Hash.txt](Images/Base_Etape1_pourinfo.png)

La deuxième est de lancer la commande ```john hash.txt ```.
Deux résultats possibles pour cette commande : 
1. Le mot de passe est trouvé rapidement. Il n'est pas assez robuste.
![Exemple 1 d'un mot de passe faible : Marseille](Images/Base_Etape2_Exemple1.png)
On peut voir dans cet exemple que le mot de passe était Marseille et qu'il a été trouve en 0 seconde.
![Exemple 2 d'un mot de passe faible : Azerty1*](Images/Base_Etape2_Exemple2.png)
On peut voir dans cet exemple que le mot de passe était Azerty1* et qu'il a été trouve en 5min02.

3. La commande tourne. C'est à vous de juger votre seuil de robustesse. Arrêtez la commande avec CTRL+Z quand vous estimerez que le mot de passe est sufffisamment résistant. Attention, le temps de recherche dépend de la puissance de votre carte graphique et de votre processeur.
![Exemple d'un mot de passe fort : J'aimelespastèques4](Images/base_Etape2_Exemple3.png)
![Après un CTRL+Z](Images/BAse_Etape2_Exemple4.png)   
On peut voir ici que John-the-ripper était en train d'utiliser son dernier mode d'attaque, le mode incrémentiel.


## Utilisation avancée :

1. Lancer une attaque uniquement avec le mode simple : ```john --s hash.txt ```  
2. Lancer une attaque uniquement avec le mode dictionnaire ```john --w hash.txt ```
3. Voir l'aide de John-the-ripper : ```john -h```


## FAQ :
- solutions aux problèmes connus et communs liés à l’utilisation
- No hashes loaded
- Zip2john not found
