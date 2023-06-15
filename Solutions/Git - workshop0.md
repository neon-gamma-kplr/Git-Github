# GIT : Gérer un projet avec Git

## Contexte
Vous travaillez sur un projet web avec votre binôme. Vous avez créé un dépôt Git sur la plateforme GitHub et vous êtes prêt à commencer à travailler dessus. Vous allez utiliser Git pour gérer les versions de votre code et collaborer avec votre binôme.

## Objectifs
* Mettre en place le dépôt Git pour le projet
* Ajouter et commiter des modifications
* Créer une branche pour travailler sur une fonctionnalité
* Fusionner la branche avec la branche principale
* Récupérer les modifications de votre binôme
* Résoudre les conflits

## Instructions

### Binome 1 
1. Créer un nouveau repository Github Vide
2. Ajouter votre binome en tant que colaborateur
   
![image](https://github.com/kplr-training/Git-Github/assets/123757632/bf3433ae-bc21-4400-b16f-af728985461d)
![image](https://github.com/kplr-training/Git-Github/assets/123757632/861ec46f-7bfe-4e0b-abb3-82d831829b99)

4. Ouvrir le dépot Github directement sur Gitpod
5. Créer un ficher python banque.py
7. Ajoutez le dossier a l'index Git
8. Création d'un premier commit
10. Poussez vos modifications vers GitHub.

### Binome 2
# Accepter l'invitation de votre binome 

  cliquer sur l'icone de la cloche qui se trouve dans la navbar a droite , puis cliquer sur "accepter l'invitation"
  
  ![image](https://github.com/kplr-training/Git-Github/assets/123757632/bdc164ea-2792-4217-ac9a-a2c74ae35cb7)
  
# Ouvrir le dépot Github directement sur Gitpod en utilisant l'url du dépot de votre binome

# 4. Création de la nouvelle branche compte_bancaire_binome2

Une branche est une ligne de développement isolée qui permet aux utilisateurs de travailler sur des fonctionnalités, des correctifs ou des expérimentations sans affecter la branche principale du projet, généralement appelée "branche principale" ou "branche maître" (par convention, "master" en anglais).

```
git branch compte_bancaire_binome2
```
La commande "git branch compte_bancaire_binome2" est utilisée pour créer une nouvelle branche dans un référentiel Git avec le nom "compte_bancaire_binome2". 

### 5. Basculer vers la branche compte_bancaire_binome2

La commande "git checkout compte_bancaire_binome2" est utilisée pour basculer vers une branche spécifique dans un référentiel Git. Dans ce cas, la branche spécifique est "compte_bancaire_binome2".

```
git checkout compte_bancaire_binome2
```
Lorsque vous exécutez cette commande, Git met à jour votre répertoire de travail pour refléter l'état de la branche spécifiée. Cela signifie que les fichiers dans votre répertoire de travail seront modifiés pour correspondre à l'état de la branche "compte_bancaire_binome2". Les modifications non validées dans votre branche actuelle peuvent être perdues si elles ne sont pas sauvegardées ou validées avant de passer à une autre branche.

### 6. Ouvrez le fichier `banque.py` et ajoutez la fonction CompteBancaire

```
class CompteBancaire:
    def __init__(self, numero_compte, solde=0):
        self.numero_compte = numero_compte
        self.solde = solde
    
    def deposer(self, montant):
        self.solde += montant
    
    def retirer(self, montant):
        if self.solde >= montant:
            self.solde -= montant
        else:
            print("Solde insuffisant.")
    
    def transferer(self, compte_destinataire, montant):
        if self.solde >= montant:
            self.solde -= montant
            compte_destinataire.deposer(montant)
        else:
            print("Solde insuffisant.")
```
La fonction ajouter_élève permet à l'utilisateur d'entrer l'identifiant et le nom d'un nouvel élève, puis ajoute ces informations au dictionnaire élèves.


### 7. Ajoutez le fichier `banque.py` au suivi de Git en utilisant la commande suivante 

```
$ git add .
```

La commande `git add .` est utilisée pour ajouter le fichier `banque.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### 8. Création du commit pour la classe `CompteBancaire` 

Créez un commit pour enregistrer la fonction `CompteBancaire` 

```
$ git commit -m "Ajout de la classe CompteBancaire"
```

La commande `git commit -m "Ajout de la classe CompteBancaire"` est utilisée pour créer un nouveau commit dans le dépôt Git. Un commit est une capture instantanée des modifications apportées aux fichiers suivis par Git.

Explication de la commande :

* `git commit` est la commande principale pour créer un commit.
* `-m "Ajout de la classe CompteBancaire"` est un paramètre qui permet de spécifier le message du commit. Le message doit être placé entre guillemets.

Une fois le commit créé, les modifications apportées aux fichiers sont enregistrées de manière permanente dans le dépôt Git. 

### 9. Afficher l'historique des commits et vérifier que votre commit a été enregistré avec succès

```
$ git log
```

La commande `git log` est utilisée pour afficher l'historique des commits dans le dépôt Git. Lorsque vous exécutez cette commande, Git affiche une liste des commits effectués, triés du plus récent au plus ancien.

Résultat de l'exécution de la commande :

- Chaque commit est affiché avec des informations telles que l'identifiant du commit (SHA-1), l'auteur, la date et le message du commit.
- Par exemple :
  ```
  commit f7fde4f82d5e8a7574680a8e138e41c05d1e3d6e
  Author: Votre nom <votre@email.com>
  Date:   Lun. Sept. 13 10:00:00 2023 +0200

      Ajout de la fonction d'addition

  commit 2cfd3b1e8949a7b894ca57182a3b14db6c0ee43f
  Author: Autre contributeur <autre@email.com>
  Date:   Lun. Sept. 12 15:30:00 2023 +0200

      Correction de bug dans la fonction de soustraction
  ```

- Chaque commit est identifié par son identifiant unique (SHA-1). Vous pouvez utiliser cet identifiant pour référencer spécifiquement un commit.

### . Pousser le fichier banque.py vers la branche compte_bancaire_binome2

Pour pousser votre branche nommée "compte_bancaire_binome2" vers le dépôt distant nommé "origin" dans Git, vous pouvez utiliser la commande suivante :

```
git push origin compte_bancaire_binome2
```

Cette commande va pousser les commits de votre branche locale "compte_bancaire_binome2" vers la branche "compte_bancaire_binome2" du dépôt distant appelé "origin".

10. Créez une branche et publiez la.
11. Ajoutez du text au fichier *chat.html.
12. Ajoutez le fichier a l'index Git.
13. Commitez les modifications avec le message "Ajout du text - Binome 2".
14. Poussez le dernier commit.
15. Créez un Pull Request.

### Binome 1
16. Acceptez le Pull Request.
17. Mettez a jour votre copie locale.
18. Créez une branche et publiez la.
19. Ajoutez du text au fichier *chat.html.
20. Ajoutez le fichier a l'index Git.
21. Commitez les modifications avec le message "Ajout du text - Binome 1".
22. Poussez le dernier commit.
23. Créez un Pull Request sur GitHub

### Binome 2
24. Acceptez le Pull Request.
25. Mettez a jour votre copie locale.

