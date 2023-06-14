# GIT

## Objectif

L'objectif de cet atelier est de vous familiariser avec l'utilisation efficace des demandes de tirage (pull requests) dans les dépôts Git.

Vous découvrirez également comment créer une demande de tirage pour soumettre vos modifications aux collaborateurs et permettre leur 
examen avant de les fusionner avec la branche principale. Ce processus vous permettra de collaborer de manière plus efficace et organisée dans vos projets Git.

## Instructions

### 1. Configuration initiale :

Ouvrez votre terminal.

Configurez votre nom d'utilisateur en utilisant la commande suivante :

```
$ git config --global user.name "Votre nom d'utilisateur"
```
     
La commande git config --global user.name "Votre nom d'utilisateur" vous permet de définir votre nom d'utilisateur. Remplacez "Votre nom d'utilisateur" par votre nom d'utilisateur réel. 

Configurez votre adresse e-mail en utilisant la commande suivante :

```
$ git config --global user.email "Votre adresse e-mail"
```

La commande git config --global user.email "Votre adresse e-mail" vous permet de définir votre adresse e-mail. Remplacez "Votre adresse e-mail" par votre adresse e-mail réelle.

Assurez-vous de remplacer les valeurs entre guillemets par vos propres informations. Une fois que vous avez exécuté ces commandes, votre nom d'utilisateur et votre adresse e-mail seront configurés globalement dans Git.

### 2. Vérifier que la configuration de votre nom d'utilisateur et de votre adresse e-mail a été effectuée avec succès. 

Vous pouvez utiliser la commande `git config --global --list` pour afficher la liste des paramètres de configuration globale de Git, y compris votre nom d'utilisateur et votre adresse e-mail.

Exécutez la commande suivante dans votre terminal :

```
$ git config --global --list
```

Cela affichera une liste des paramètres de configuration globale, y compris votre nom d'utilisateur et votre adresse e-mail, si vous les avez configurés correctement.

Assurez-vous de rechercher les lignes contenant **`user.name` et `user.email`** dans la sortie de la commande pour confirmer que vos informations de configuration sont correctement enregistrées.

### 3. Création d'un fichier Python

Créez un fichier Python vide dans le dossier :

```
$ touch devise.py
```

### 4. Ajoutez le fichier `devise.py` au suivi de Git en utilisant la commande suivante 

```
$ git add .
```

La commande `git add .` est utilisée pour ajouter le fichier `devise.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### 5. Création d'un premier commit pour le fichier `devise.py`

La commande "git commit -m 'Initial commit'" est utilisée pour créer un nouveau commit dans le référentiel Git. Un commit est une capture instantanée des modifications apportées aux fichiers du projet à un moment précis.

```
git commit -m "Initial commit"
```

### 6. Pousser le changement vers le dépot distant 

La commande "git push" est utilisée pour pousser (envoyer) les commits locaux vers un référentiel distant, généralement situé sur une plateforme de gestion de code telle que GitHub, GitLab ou Bitbucket.

```
git push 
```

Lorsque vous exécutez cette commande, Git compare les commits locaux que vous avez effectués avec ceux présents dans le référentiel distant. Il envoie uniquement les nouveaux commits locaux qui n'existent pas encore dans le référentiel distant

### 4. Création de la nouvelle branche convertir

Une branche est une ligne de développement isolée qui permet aux utilisateurs de travailler sur des fonctionnalités, des correctifs ou des expérimentations sans affecter la branche principale du projet, généralement appelée "branche principale" ou "branche maître" (par convention, "master" en anglais).

```
git branch convertir
```
La commande "git branch convertir" est utilisée pour créer une nouvelle branche dans un référentiel Git avec le nom "convertir". 

### 5. Basculer vers la branche convertir

La commande "git checkout convertir" est utilisée pour basculer vers une branche spécifique dans un référentiel Git. Dans ce cas, la branche spécifique est "convertir".

```
git checkout convertir
```
Lorsque vous exécutez cette commande, Git met à jour votre répertoire de travail pour refléter l'état de la branche spécifiée. Cela signifie que les fichiers dans votre répertoire de travail seront modifiés pour correspondre à l'état de la branche "convertir". Les modifications non validées dans votre branche actuelle peuvent être perdues si elles ne sont pas sauvegardées ou validées avant de passer à une autre branche.

### 6. Ouvrez le fichier `devise.py` et ajoutez la fonction pour convertir une devise

```
def convertir(montant, taux):
    return montant * taux
```
La fonction convertir qui prend deux paramètres : montant et taux. Cette fonction effectue une opération de conversion de devise en multipliant le montant donné par le taux de change spécifié.

### 7. Ajoutez le fichier `devise.py` au suivi de Git en utilisant la commande suivante 

```
$ git add .
```

La commande `git add .` est utilisée pour ajouter le fichier `devise.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### 8. Création du commit pour la fonction `convertir` 

Créez un commit pour enregistrer la fonction `convertir` 

```
$ git commit -m "Ajout de la fonction convertir"
```

La commande `git commit -m "Ajout de la fonction convertir"` est utilisée pour créer un nouveau commit dans le dépôt Git. Un commit est une capture instantanée des modifications apportées aux fichiers suivis par Git.

Explication de la commande :

* `git commit` est la commande principale pour créer un commit.
* `-m "Ajout de la fonction convertir"` est un paramètre qui permet de spécifier le message du commit. Le message doit être placé entre guillemets.

Résultat de l'exécution de la commande :

- Si le commit est créé avec succès, Git affiche des informations sur le commit, telles que l'identifiant unique du commit (SHA-1), l'auteur, la date et le message du commit.

- Par exemple :

```
[main f7fde4f] Ajout de la fonction d'addition
1 file changed, 10 insertions(+)
```
- Le commit est enregistré dans l'historique du dépôt Git, capturant ainsi les modifications apportées aux fichiers à ce stade.

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

### . Pousser le fichier devise.py vers la branche convertir

Pour pousser votre branche nommée "convertir" vers le dépôt distant nommé "origin" dans Git, vous pouvez utiliser la commande suivante :

```
git push origin convertir
```

Cette commande va pousser les commits de votre branche locale "convertir" vers la branche "cconvertir" du dépôt distant appelé "origin". 

### . Accédez au référentiel distant sur [GitHub](https://github.com/) 

Cliquez sur le bouton "Compare & Pull Request" (demande de tirage) pour créer une nouvelle demande de tirage.

![image](https://github.com/kplr-training/Git-Github/assets/123757632/db164d57-5d69-4aa6-9509-2c7014f2a5c8)

Ajoutez une description pour votre demande de tirage et soumettez-la.

![image](https://github.com/kplr-training/Git-Github/assets/123757632/4d14936d-4e22-46ed-9784-25d43bdc7bb4)

Les collaborateurs peuvent maintenant examiner votre demande de tirage, ajouter des commentaires et demander des modifications supplémentaires si nécessaire.

Une fois que la demande de tirage est approuvée et que toutes les modifications demandées sont effectuées, vous pouvez la fusionner avec la branche principale (par exemple, "master") en cliquant sur le bouton "Merge" (fusionner).

Fusionner et confirmer la demande de tirage

Pour fusionner le pull request cliquer sur Merge pull request puis Confirm merge

![image](https://github.com/kplr-training/Git-Github/assets/123757632/5283789c-e846-4e0d-9be7-ee3b6a67ddc1)

### . Verifier les commits dans votre repository 

![image](https://github.com/kplr-training/Git-Github/assets/123757632/b08618ff-09cf-4b7f-8cb7-d41eb8908fc1)
