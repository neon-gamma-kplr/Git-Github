# GIT - Branch

## Objectif
L'objectif de cet atelier est d'approfondir vos compétences en travaillant avec les branches Git. 

Les branches sont utiles pour développer des fonctionnalités de manière isolée et collaborer efficacement sur un projet. Vous apprendrez à créer et à basculer entre les branches, à fusionner les modifications entre les branches, et à résoudre les éventuels conflits. 

## Instructions

### Créer un nouveau repository Github Vide

Connectez-vous à votre compte GitHub et cliquez sur le bouton "New" pour créer un nouveau dépôt. Donnez un nom et une description au dépôt et choisissez les options appropriées, telles que la visibilité et le fichier README.md. Cliquez sur le bouton "Create repository" pour créer le nouveau dépôt.

![image](https://user-images.githubusercontent.com/123757632/221904279-c5a2d920-5b45-4193-b599-1cc21daae210.png)

### Ouvrir le dépot Github directement sur Gitpod

Etapes pour création et utilisation de [Gitpod](https://github.com/kplr-training/Git-Github/blob/main/Ateliers/Gitpod%20101.md).

### Vérifier que la configuration de votre nom d'utilisateur et de votre adresse e-mail

Vous pouvez utiliser la commande `git config --global --list` pour afficher la liste des paramètres de configuration globale de Git, y compris votre nom d'utilisateur et votre adresse e-mail.

Exécutez la commande suivante dans votre terminal :

```
$ git config --global --list
```

Cela affichera une liste des paramètres de configuration globale, y compris votre nom d'utilisateur et votre adresse e-mail, si vous les avez configurés correctement.

Assurez-vous de rechercher les lignes contenant **`user.name` et `user.email`** dans la sortie de la commande pour confirmer que vos informations de configuration sont correctement enregistrées.

### Création d'un fichier Python

Créez un fichier Python vide dans le dossier :

```
$ touch gestion_eleves.py
```

### Ajoutez le fichier `gestion_eleves.py` au suivi de Git en utilisant la commande suivante 

```
$ git add .
```

La commande `git add .` est utilisée pour ajouter le fichier `gestion_eleves.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### Création d'un premier commit pour le fichier `gestion_eleves.py`

La commande "git commit -m 'Initial commit'" est utilisée pour créer un nouveau commit dans le référentiel Git. Un commit est une capture instantanée des modifications apportées aux fichiers du projet à un moment précis.

```
git commit -m "Initial commit"
```

### Pousser le changement vers le dépot distant 

La commande "git push" est utilisée pour pousser (envoyer) les commits locaux vers un référentiel distant, généralement situé sur une plateforme de gestion de code telle que GitHub, GitLab ou Bitbucket.

```
git push 
```

Lorsque vous exécutez cette commande, Git compare les commits locaux que vous avez effectués avec ceux présents dans le référentiel distant. Il envoie uniquement les nouveaux commits locaux qui n'existent pas encore dans le référentiel distant

### Création de la nouvelle branche ajouter_eleve

Une branche est une ligne de développement isolée qui permet aux utilisateurs de travailler sur des fonctionnalités, des correctifs ou des expérimentations sans affecter la branche principale du projet, généralement appelée "branche principale" ou "branche maître" (par convention, "master" en anglais).

```
git branch ajouter_eleve
```
La commande "git branch ajouter_eleve" est utilisée pour créer une nouvelle branche dans un référentiel Git avec le nom "ajouter_eleve". 

### Basculer vers la branche ajouter_eleve

La commande "git checkout ajouter_eleve" est utilisée pour basculer vers une branche spécifique dans un référentiel Git. Dans ce cas, la branche spécifique est "ajouter_eleve".

```
git checkout ajouter_eleve
```
Lorsque vous exécutez cette commande, Git met à jour votre répertoire de travail pour refléter l'état de la branche spécifiée. Cela signifie que les fichiers dans votre répertoire de travail seront modifiés pour correspondre à l'état de la branche "ajouter_eleve". Les modifications non validées dans votre branche actuelle peuvent être perdues si elles ne sont pas sauvegardées ou validées avant de passer à une autre branche.

### Ouvrez le fichier `gestion_eleves.py` et ajoutez la fonction pour ajouter un élève

```
def ajouter_élève():
    id_élève = input("Entrez l'identifiant de l'élève : ")
    nom_élève = input("Entrez le nom de l'élève : ")
    élèves[id_élève] = nom_élève
    print("Élève ajouté avec succès !")
```
La fonction ajouter_élève permet à l'utilisateur d'entrer l'identifiant et le nom d'un nouvel élève, puis ajoute ces informations au dictionnaire élèves.


### Ajoutez le fichier `gestion_eleves.py` au suivi de Git en utilisant la commande suivante 

```
$ git add .
```

La commande `git add .` est utilisée pour ajouter le fichier `gestion_eleves.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### Création du commit pour la fonction `ajouter_élève` 

Créez un commit pour enregistrer la fonction `ajouter_élève` 

```
$ git commit -m "Ajout de la fonction d'ajouter_élève"
```

La commande `git commit -m "Ajout de la fonction d'addition"` est utilisée pour créer un nouveau commit dans le dépôt Git. Un commit est une capture instantanée des modifications apportées aux fichiers suivis par Git.

Explication de la commande :

* `git commit` est la commande principale pour créer un commit.
* `-m "Ajout de la fonction d'addition"` est un paramètre qui permet de spécifier le message du commit. Le message doit être placé entre guillemets.

Résultat de l'exécution de la commande :

- Si le commit est créé avec succès, Git affiche des informations sur le commit, telles que l'identifiant unique du commit (SHA-1), l'auteur, la date et le message du commit.

- Par exemple :

```
[main f7fde4f] Ajout de la fonction d'addition
1 file changed, 10 insertions(+)
```
- Le commit est enregistré dans l'historique du dépôt Git, capturant ainsi les modifications apportées aux fichiers à ce stade.

Une fois le commit créé, les modifications apportées aux fichiers sont enregistrées de manière permanente dans le dépôt Git. 

### Afficher l'historique des commits et vérifier que votre commit a été enregistré avec succès

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

### Pousser le fichier gestion_eleves.py vers la branche ajouter_eleve

Pour pousser votre branche nommée "ajouter_eleve" vers le dépôt distant nommé "origin" dans Git, vous pouvez utiliser la commande suivante :

```
git push origin ajouter_eleve
```

Cette commande va pousser les commits de votre branche locale "ajouter_eleve" vers la branche "ajouter_eleve" du dépôt distant appelé "origin". 

### Basculer vers la branche principale 

La commande "git checkout main" est utilisée pour basculer vers la branche principale (ou branche maître) dans un référentiel Git. La branche principale est généralement utilisée pour représenter l'état stable du projet.

```
git checkout main
```

Lorsque vous exécutez cette commande, Git met à jour votre répertoire de travail pour refléter l'état de la branche principale. Cela signifie que les fichiers dans votre répertoire de travail seront modifiés pour correspondre à l'état de la branche "main". 

### Fudionner la branche "ajouter_eleve" avec la branche "main"

La commande "git merge ajouter_eleve" fusionne la branche "ajouter_eleve" dans la branche actuelle. Plus précisément, elle incorpore les modifications de la branche "ajouter_eleve" dans la branche courante.

```
git merge ajouter_eleve
```

Lorsque vous exécutez cette commande, Git examine les modifications entre la branche actuelle et la branche "ajouter_eleve". Il essaie de fusionner automatiquement les modifications, en appliquant les changements de la branche "ajouter_eleve" sur la branche courante.

En résumé, la commande "git merge ajouter_eleve" fusionne les modifications de la branche "ajouter_eleve" dans la branche courante, incorporant ainsi les changements effectués dans la branche "ajouter_eleve" dans votre branche de travail actuelle.

**REMARQUE : La fonction ajouter_eleve se trouve maintenant dans le ficher "gestion_eleve" dans la branche principale "main"**

### Création de la nouvelle branche modifier_eleve

```
git branch modifier_eleve
```
La commande "git branch modifier_eleve" est utilisée pour créer une nouvelle branche dans un référentiel Git avec le nom "modifier_eleve". 

### Basculer vers la branche modifier_eleve

La commande "git checkout modifier_eleve" est utilisée pour basculer vers une branche spécifique dans un référentiel Git. Dans ce cas, la branche spécifique est "modifier_eleve".

```
git checkout modifier_eleve
```

### Ouvrez le fichier `gestion_eleves.py` et ajoutez la fonction pour modifier un élève

```
def modifier_élève():
    id_élève = input("Entrez l'identifiant de l'élève à modifier : ")
    if id_élève in élèves:
        nouveau_nom = input("Entrez le nouveau nom de l'élève : ")
        élèves[id_élève] = nouveau_nom
        print("Élève mis à jour avec succès !")
    else:
        print("L'élève n'existe pas.")
```

La fonction modifier_élève permet à l'utilisateur d'entrer l'identifiant et le nom d'un nouvel élève, puis modifie ces informations au dictionnaire élèves.

### Ajoutez le fichier `gestion_eleves.py` au suivi de Git en utilisant la commande suivante 

```
$ git add .
```

La commande `git add .` est utilisée pour ajouter le fichier `gestion_eleves.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### Création d'un premier commit pour la fonction `modifier_élève` 

Créez un commit pour enregistrer la fonction `modifier_élève` 

```
$ git commit -m "Ajout de la fonction de modifier_élève"
```

La commande `git commit -m "Ajout de la fonction de modifier_élève"` est utilisée pour créer un nouveau commit dans le dépôt Git. Un commit est une capture instantanée des modifications apportées aux fichiers suivis par Git.

Explication de la commande :

* `git commit` est la commande principale pour créer un commit.
* `-m "Ajout de la fonction de modifier_élève"` est un paramètre qui permet de spécifier le message du commit. Le message doit être placé entre guillemets.

### Afficher l'historique des commits et vérifier que votre commit a été enregistré avec succès

```
$ git log
```

La commande `git log` est utilisée pour afficher l'historique des commits dans le dépôt Git. Lorsque vous exécutez cette commande, Git affiche une liste des commits effectués, triés du plus récent au plus ancien.

### Pousser le fichier gestion_eleves.py vers la branche modifier_eleve

Pour pousser votre branche nommée "modifier_eleve" vers le dépôt distant nommé "origin" dans Git, vous pouvez utiliser la commande suivante :

```
git push origin modifier_eleve
```

Cette commande va pousser les commits de votre branche locale "modifier_eleve" vers la branche "modifier_eleve" du dépôt distant appelé "origin". 

### Basculer vers la branche principale 

La commande "git checkout main" est utilisée pour basculer vers la branche principale (ou branche maître) dans un référentiel Git. La branche principale est généralement utilisée pour représenter l'état stable du projet.

```
git checkout main
```

Lorsque vous exécutez cette commande, Git met à jour votre répertoire de travail pour refléter l'état de la branche principale. Cela signifie que les fichiers dans votre répertoire de travail seront modifiés pour correspondre à l'état de la branche "main". 

### Fudionner la branche "modifier_eleve" avec la branche "main"

La commande "git merge modifier_eleve" fusionne la branche "modifier_eleve" dans la branche actuelle. Plus précisément, elle incorpore les modifications de la branche "modifier_eleve" dans la branche courante.

```
git merge modifier_eleve
```

Lorsque vous exécutez cette commande, Git examine les modifications entre la branche actuelle et la branche "modifer_eleve". Il essaie de fusionner automatiquement les modifications, en appliquant les changements de la branche "modifier_eleve" sur la branche courante.

**REMARQUE : La fonction modifier_eleve se trouve maintenant dans le ficher "gestion_eleve" dans la branche principale "main"**


### Création de la nouvelle branche supprimer_eleve

```
git branch supprimer_eleve
```
La commande "git branch modifier_eleve" est utilisée pour créer une nouvelle branche dans un référentiel Git avec le nom "modifier_eleve". 

### Basculer vers la branche supprimer_eleve

La commande "git checkout supprimer_eleve" est utilisée pour basculer vers une branche spécifique dans un référentiel Git. Dans ce cas, la branche spécifique est "supprimer_eleve".

```
git checkout supprimer_eleve
```

### Ouvrez le fichier `gestion_eleves.py` et ajoutez la fonction pour supprimer un élève

```
def supprimer_élève():
    id_élève = input("Entrez l'identifiant de l'élève à supprimer : ")
    if id_élève in élèves:
        del élèves[id_élève]
        print("Élève supprimé avec succès !")
    else:
        print("L'élève n'existe pas.")
```

La fonction supprimer_élève permet à l'utilisateur d'entrer l'identifiant et le nom d'un nouvel élève, puis le supprimer.

### Ajoutez le fichier `gestion_eleves.py` au suivi de Git en utilisant la commande suivante 

```
$ git add .
```

La commande `git add .` est utilisée pour ajouter le fichier `gestion_eleves.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### Création d'un premier commit pour la fonction `supprimer_élève` 

Créez un commit pour enregistrer la fonction `supprimer_élève` 

```
$ git commit -m "Ajout de la fonction de supprimer_élève"
```

La commande `git commit -m "Ajout de la fonction de supprimer_élève"` est utilisée pour créer un nouveau commit dans le dépôt Git. Un commit est une capture instantanée des modifications apportées aux fichiers suivis par Git.

Explication de la commande :

* `git commit` est la commande principale pour créer un commit.
* `-m "Ajout de la fonction de supprimer_élève"` est un paramètre qui permet de spécifier le message du commit. Le message doit être placé entre guillemets.

### Afficher l'historique des commits et vérifier que votre commit a été enregistré avec succès

```
$ git log
```

La commande `git log` est utilisée pour afficher l'historique des commits dans le dépôt Git. Lorsque vous exécutez cette commande, Git affiche une liste des commits effectués, triés du plus récent au plus ancien.

### Pousser le fichier gestion_eleves.py vers la branche supprimer_eleve

Pour pousser votre branche nommée "supprimer_eleve" vers le dépôt distant nommé "origin" dans Git, vous pouvez utiliser la commande suivante :

```
git push origin supprimer_eleve
```

Cette commande va pousser les commits de votre branche locale "supprimer_eleve" vers la branche "supprimer_eleve" du dépôt distant appelé "origin". 

### Basculer vers la branche principale 

La commande "git checkout main" est utilisée pour basculer vers la branche principale (ou branche maître) dans un référentiel Git. La branche principale est généralement utilisée pour représenter l'état stable du projet.

```
git checkout main
```

Lorsque vous exécutez cette commande, Git met à jour votre répertoire de travail pour refléter l'état de la branche principale. Cela signifie que les fichiers dans votre répertoire de travail seront modifiés pour correspondre à l'état de la branche "main". 

### Fudionner la branche "supprimer_eleve" avec la branche "main"

La commande "git merge supprimer_eleve" fusionne la branche "supprimer_eleve" dans la branche actuelle. Plus précisément, elle incorpore les modifications de la branche "supprimer_eleve" dans la branche courante.

```
git merge supprimer_eleve
```

Lorsque vous exécutez cette commande, Git examine les modifications entre la branche actuelle et la branche "supprimer_eleve". Il essaie de fusionner automatiquement les modifications, en appliquant les changements de la branche "supprimer_eleve" sur la branche courante.

**REMARQUE : La fonction supprimer_eleve se trouve maintenant dans le ficher "gestion_eleve" dans la branche principale "main"**

### Création de la nouvelle branche afficher_tous_les_eleves

```
git branch afficher_tous_les_eleves
```
La commande "git branch afficher_tous_les_eleves" est utilisée pour créer une nouvelle branche dans un référentiel Git avec le nom "modifier_eleve". 

### Basculer vers la branche afficher_tous_les_eleves

La commande "git checkout afficher_tous_les_eleves" est utilisée pour basculer vers une branche spécifique dans un référentiel Git. Dans ce cas, la branche spécifique est "afficher_tous_les_eleves".

```
git checkout afficher_tous_les_eleves
```

### Ouvrez le fichier `gestion_eleves.py` et ajoutez la fonction pour afficher tous les eleves

```
élèves = {}
def afficher_tous_les_élèves():
    if élèves:
        print("Liste complète des élèves :")
        for id_élève, nom_élève in élèves.items():
            print(f"ID : {id_élève}, Nom : {nom_élève}")
    else:
        print("Aucun élève dans la liste.")
```

La fonction afficher_tous_les_élèves permet à l'utilisateur d'entrer l'identifiant et le nom d'un nouvel élève, puis le supprimer.

### Ajoutez le fichier `gestion_eleves.py` au suivi de Git en utilisant la commande suivante 

```
$ git add .
```

La commande `git add .` est utilisée pour ajouter le fichier `gestion_eleves.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### Création d'un premier commit pour la fonction `afficher_tous_les_élèves()` 

Créez un commit pour enregistrer la fonction `afficher_tous_les_élèves` 

```
$ git commit -m "Ajout de la fonction afficher_tous_les_élèves"
```

La commande `git commit -m "Ajout de la fonction afficher_tous_les_élèves"` est utilisée pour créer un nouveau commit dans le dépôt Git. Un commit est une capture instantanée des modifications apportées aux fichiers suivis par Git.

Explication de la commande :

* `git commit` est la commande principale pour créer un commit.
* `-m "Ajout de la fonction afficher_tous_les_élèves"` est un paramètre qui permet de spécifier le message du commit. Le message doit être placé entre guillemets.

### Afficher l'historique des commits et vérifier que votre commit a été enregistré avec succès

```
$ git log
```

La commande `git log` est utilisée pour afficher l'historique des commits dans le dépôt Git. Lorsque vous exécutez cette commande, Git affiche une liste des commits effectués, triés du plus récent au plus ancien.

### Pousser le fichier gestion_eleves.py vers la branche afficher_tous_les_élèves

Pour pousser votre branche nommée "afficher_tous_les_élèves" vers le dépôt distant nommé "origin" dans Git, vous pouvez utiliser la commande suivante :

```
git push origin afficher_tous_les_élèves
```

Cette commande va pousser les commits de votre branche locale "afficher_tous_les_élèves" vers la branche "afficher_tous_les_élèves" du dépôt distant appelé "origin". 

### Basculer vers la branche principale 

La commande "git checkout main" est utilisée pour basculer vers la branche principale (ou branche maître) dans un référentiel Git. La branche principale est généralement utilisée pour représenter l'état stable du projet.

```
git checkout main
```

Lorsque vous exécutez cette commande, Git met à jour votre répertoire de travail pour refléter l'état de la branche principale. Cela signifie que les fichiers dans votre répertoire de travail seront modifiés pour correspondre à l'état de la branche "main". 

### Fudionner la branche "afficher_tous_les_eleves" avec la branche "main"

La commande "git merge afficher_tous_les_eleves" fusionne la branche "afficher_tous_les_eleves" dans la branche actuelle. Plus précisément, elle incorpore les modifications de la branche "afficher_tous_les_eleves" dans la branche courante.

```
git merge afficher_tous_les_eleves
```

Lorsque vous exécutez cette commande, Git examine les modifications entre la branche actuelle et la branche "afficher_tous_les_eleves". Il essaie de fusionner automatiquement les modifications, en appliquant les changements de la branche "afficher_tous_les_eleves" sur la branche courante.

**REMARQUE : La fonction afficher_tous_les_élèves se trouve maintenant dans le ficher "gestion_eleve" dans la branche principale "main"**

### Création de la nouvelle branche gestion_eleves

```
git branch gestion_eleves
```
La commande "git branch gestion_eleves" est utilisée pour créer une nouvelle branche dans un référentiel Git avec le nom "git branch gestion_eleves". 

### Basculer vers la branche gestion_eleves

La commande "git checkout gestion_eleves" est utilisée pour basculer vers une branche spécifique dans un référentiel Git. Dans ce cas, la branche spécifique est "gestion_eleves".

```
git checkout gestion_eleves
```

### Ouvrez le fichier `gestion_eleves.py` et ajoutez la fonction principale 

```
def gestion_eleves():
    print("Bienvenue dans la gestion des élèves !")
    while True:
        print("\nMenu :")
        print("1. Ajouter un élève")
        print("2. Modifier un élève")
        print("3. Supprimer un élève")
        print("4. Afficher la liste complète des élèves")
        print("5. Quitter")

        choix = input("Veuillez sélectionner une option (1-5) : ")

        if choix == "1":
            ajouter_élève()
        elif choix == "2":
            modifier_élève()
        elif choix == "3":
            supprimer_élève()
        elif choix == "4":
            afficher_tous_les_élèves()
        elif choix == "5":
            break
        else:
            print("Option invalide. Veuillez réessayer.")

if __name__ == "__main__":
    gestion_eleves()
```

La fonction gestion_eleves permet à l'utilisateur de selectionner une option afin d'executer les fonctions de gestion. 

### Ajoutez le fichier `gestion_eleves.py` au suivi de Git en utilisant la commande suivante 

```
$ git add .
```

La commande `git add .` est utilisée pour ajouter le fichier `gestion_eleves.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### Création un commit pour la fonction `gestion_eleves()` 

Créez un commit pour enregistrer la fonction `gestion_eleves()` 

```
$ git commit -m "Ajout de la fonction gestion_eleves()"
```

La commande `git commit -m "Ajout de la fonction gestion_eleves()"` est utilisée pour créer un nouveau commit dans le dépôt Git. Un commit est une capture instantanée des modifications apportées aux fichiers suivis par Git.

Explication de la commande :

* `git commit` est la commande principale pour créer un commit.
* `-m "Ajout de la fonction gestion_eleves()"` est un paramètre qui permet de spécifier le message du commit. Le message doit être placé entre guillemets.

### Afficher l'historique des commits et vérifier que votre commit a été enregistré avec succès

```
$ git log
```

La commande `git log` est utilisée pour afficher l'historique des commits dans le dépôt Git. Lorsque vous exécutez cette commande, Git affiche une liste des commits effectués, triés du plus récent au plus ancien.

### Pousser le fichier gestion_eleves.py vers la branche gestion_eleves

Pour pousser votre branche nommée "gestion_eleves" vers le dépôt distant nommé "origin" dans Git, vous pouvez utiliser la commande suivante :

```
git push origin gestion_eleves
```

Cette commande va pousser les commits de votre branche locale "gestion_eleves" vers la branche "gestion_eleves" du dépôt distant appelé "origin". 

### Basculer vers la branche principale 

La commande "git checkout main" est utilisée pour basculer vers la branche principale (ou branche maître) dans un référentiel Git. La branche principale est généralement utilisée pour représenter l'état stable du projet.

```
git checkout main
```

Lorsque vous exécutez cette commande, Git met à jour votre répertoire de travail pour refléter l'état de la branche principale. Cela signifie que les fichiers dans votre répertoire de travail seront modifiés pour correspondre à l'état de la branche "main". 

### Fudionner la branche "gestion_eleves" avec la branche "main"

La commande "git merge gestion_eleves" fusionne la branche "gestion_eleves" dans la branche actuelle. Plus précisément, elle incorpore les modifications de la branche "gestion_eleves" dans la branche courante.

```
git merge gestion_eleves
```

Lorsque vous exécutez cette commande, Git examine les modifications entre la branche actuelle et la branche "gestion_eleves". Il essaie de fusionner automatiquement les modifications, en appliquant les changements de la branche "gestion_eleves" sur la branche courante.

**REMARQUE : La fonction afficher_tous_les_élèves se trouve maintenant dans le ficher "gestion_eleve" dans la branche principale "main"**

### Vérification du dépot et des commits sur [GitHub](https://github.com/) 

Pour vérifier les commits dans un dépôt GitHub, vous pouvez suivre les étapes suivantes :

1. Dans l'onglet du dépôt, vous trouverez plusieurs onglets différents tels que "Code", "Issues", "Pull requests", etc. Cliquez sur l'onglet "Commits" pour afficher la liste des commits.

2. La page des commits affiche les commits dans l'ordre chronologique, du plus récent au plus ancien. Chaque commit est accompagné d'un message de commit, de l'auteur du commit, de l'heure et de la date du commit, ainsi que des statistiques sur les modifications ajoutées ou supprimées.

En utilisant l'interface GitHub, vous pouvez facilement visualiser l'historique des commits, examiner les modifications apportées aux fichiers et les commentaires associés à chaque commit. Cela vous permet de suivre l'évolution du dépôt et de comprendre les changements qui ont été effectués au fil du temps.




