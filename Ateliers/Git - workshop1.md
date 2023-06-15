# GIT 

## Objectif

L'objectif de cet atelier est d'apprendre comment commettre des changements dans des dépôts Git de manière efficace.

Vous découvrirez comment utiliser les commandes git add pour préparer les fichiers modifiés, git commit pour créer un instantané des modifications, et git push pour pousser les commits vers un dépôt distant.

## Instructions

### Créer un nouveau repository Github Vide

Connectez-vous à votre compte GitHub et cliquez sur le bouton "New" pour créer un nouveau dépôt. Donnez un nom et une description au dépôt et choisissez les options appropriées, telles que la visibilité et le fichier README.md. Cliquez sur le bouton "Create repository" pour créer le nouveau dépôt.

![image](https://user-images.githubusercontent.com/123757632/221904279-c5a2d920-5b45-4193-b599-1cc21daae210.png)

### Ouvrir le dépot Github directement sur Gitpod

Etapes pour création et utilisation de [Gitpod](https://github.com/kplr-training/Git-Github/blob/main/Ateliers/Gitpod%20101.md).

### Configuration initiale :

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

### Vérifier que la configuration de votre nom d'utilisateur et de votre adresse e-mail a été effectuée avec succès. 

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
$ touch calculatrice.py
```

### Ouvrez le fichier `calculatrice.py` et ajoutez les fonctions de calculatrice  

```
def addition(a, b):
  return a + b
```

### Ajoutez le fichier `calculatrice.py` au suivi de Git en utilisant la commande suivante 

```
$ git add .
```

La commande `git add .` est utilisée pour ajouter le fichier `calculatrice.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### Création d'un premier commit pour la fonction `addition` 

Créez un commit pour enregistrer la fonction `addition` 

```
$ git commit -m "Ajout de la fonction d'addition"
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

### Poussez vos modifications vers GitHub.

La commande "git push" est utilisée pour pousser (envoyer) les commits locaux vers un référentiel distant, généralement situé sur une plateforme de gestion de code telle que GitHub, GitLab ou Bitbucket.

```
git push 
```

Lorsque vous exécutez cette commande, Git compare les commits locaux que vous avez effectués avec ceux présents dans le référentiel distant. Il envoie uniquement les nouveaux commits locaux qui n'existent pas encore dans le référentiel distant

### Ajout d'autres fonctions :

Ajoutez d'autres fonctions de calculatrice dans le fichier `calculatrice.py`, par exemple une fonction `soustraction` :

```
def soustraction(a, b):
  return a - b
```

### Ajoutez le fichier modifié au suivi :
 
```
git add .
```
La commande `git add .` est utilisée pour ajouter le fichier `calculatrice.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### Créez un nouveau commit pour enregistrer la fonction `soustraction` :

```
git commit -m "Ajout de la fonction de soustraction"
```
Une fois le commit créé, les modifications apportées aux fichiers sont enregistrées de manière permanente dans le dépôt Git. 

### Vérification de l'historique des commits :

Affichez l'historique des commits en utilisant la commande suivante :

```
git log
```

L'historique des commits affiché par `git log` vous permet de visualiser les modifications apportées aux fichiers au fil du temps, ainsi que les auteurs et les messages associés à chaque commit. Cela vous aide à comprendre l'évolution du projet et à revenir à des versions spécifiques si nécessaire.

### Poussez vos modifications vers GitHub.

La commande "git push" est utilisée pour pousser (envoyer) les commits locaux vers un référentiel distant, généralement situé sur une plateforme de gestion de code telle que GitHub, GitLab ou Bitbucket.

```
git push 
```

Lorsque vous exécutez cette commande, Git compare les commits locaux que vous avez effectués avec ceux présents dans le référentiel distant. Il envoie uniquement les nouveaux commits locaux qui n'existent pas encore dans le référentiel distant

### Ajout d'autres fonctions :

Ajoutez d'autres fonctions de calculatrice dans le fichier `calculatrice.py`, par exemple une fonction `multiplication` :

```
def multiplication(a, b):
    return a * b
```

### Ajoutez le fichier modifié au suivi :
 
```
git add .
```
La commande `git add .` est utilisée pour ajouter le fichier `calculatrice.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### Créez un nouveau commit pour enregistrer la fonction `multiplication` :

```
git commit -m "Ajout de la fonction de multiplication"
```
Une fois le commit créé, les modifications apportées aux fichiers sont enregistrées de manière permanente dans le dépôt Git. 

### Vérification de l'historique des commits :

Affichez l'historique des commits en utilisant la commande suivante :

```
git log
```

L'historique des commits affiché par `git log` vous permet de visualiser les modifications apportées aux fichiers au fil du temps, ainsi que les auteurs et les messages associés à chaque commit. Cela vous aide à comprendre l'évolution du projet et à revenir à des versions spécifiques si nécessaire.

### Poussez vos modifications vers GitHub.

La commande "git push" est utilisée pour pousser (envoyer) les commits locaux vers un référentiel distant, généralement situé sur une plateforme de gestion de code telle que GitHub, GitLab ou Bitbucket.

```
git push 
```

Lorsque vous exécutez cette commande, Git compare les commits locaux que vous avez effectués avec ceux présents dans le référentiel distant. Il envoie uniquement les nouveaux commits locaux qui n'existent pas encore dans le référentiel distant

### Ajout d'autres fonctions :

Ajoutez d'autres fonctions de calculatrice dans le fichier `calculatrice.py`, par exemple une fonction `division` :

```
def division(a, b):
    if b != 0:
        return a / b
    else:
        return "Erreur : Division par zéro"

```

### Ajoutez le fichier modifié au suivi :
 
```
git add .
```
La commande `git add .` est utilisée pour ajouter le fichier `calculatrice.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### Créez un nouveau commit pour enregistrer la fonction `division` :

```
git commit -m "Ajout de la fonction de division"
```
Une fois le commit créé, les modifications apportées aux fichiers sont enregistrées de manière permanente dans le dépôt Git. 

### Vérification de l'historique des commits :

Affichez l'historique des commits en utilisant la commande suivante :

```
git log
```

L'historique des commits affiché par `git log` vous permet de visualiser les modifications apportées aux fichiers au fil du temps, ainsi que les auteurs et les messages associés à chaque commit. Cela vous aide à comprendre l'évolution du projet et à revenir à des versions spécifiques si nécessaire.

### Poussez vos modifications vers GitHub.

La commande "git push" est utilisée pour pousser (envoyer) les commits locaux vers un référentiel distant, généralement situé sur une plateforme de gestion de code telle que GitHub, GitLab ou Bitbucket.

```
git push 
```

Lorsque vous exécutez cette commande, Git compare les commits locaux que vous avez effectués avec ceux présents dans le référentiel distant. Il envoie uniquement les nouveaux commits locaux qui n'existent pas encore dans le référentiel distant

### Ajout d'autres fonctions :

La fonction calculatrice() qui affiche une liste de choix à l'utilisateur, lui permet de saisir deux nombres, effectue le calcul correspondant et affiche le résultat.

```
def calculatrice():
    print("Bienvenue dans la calculatrice !")
    print("Veuillez choisir une opération :")
    print("1. Addition")
    print("2. Soustraction")
    print("3. Multiplication")
    print("4. Division")
    choix = input("Votre choix (1-4) : ")

    if choix == "1":
        a = float(input("Premier nombre : "))
        b = float(input("Deuxième nombre : "))
        resultat = addition(a, b)
        print("Résultat : ", resultat)
    elif choix == "2":
        a = float(input("Premier nombre : "))
        b = float(input("Deuxième nombre : "))
        resultat = soustraction(a, b)
        print("Résultat : ", resultat)
    elif choix == "3":
        a = float(input("Premier nombre : "))
        b = float(input("Deuxième nombre : "))
        resultat = multiplication(a, b)
        print("Résultat : ", resultat)
    elif choix == "4":
        a = float(input("Numérateur : "))
        b = float(input("Dénominateur : "))
        if b != 0:
            resultat = division(a, b)
            print("Résultat : ", resultat)
        else:
            print("Erreur : Division par zéro")
    else:
        print("Choix invalide.")

calculatrice()
```

 ### Ajoutez le fichier modifié au suivi :
 
```
git add .
```
La commande `git add .` est utilisée pour ajouter le fichier `calculatrice.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### Créez un nouveau commit pour enregistrer la fonction `calculatrice` :

```
git commit -m "Ajout de la fonction de calculatrice"
```
Une fois le commit créé, les modifications apportées aux fichiers sont enregistrées de manière permanente dans le dépôt Git. 

### Vérification de l'historique des commits 

Affichez l'historique des commits en utilisant la commande suivante :

```
git log
```

L'historique des commits affiché par `git log` vous permet de visualiser les modifications apportées aux fichiers au fil du temps, ainsi que les auteurs et les messages associés à chaque commit. Cela vous aide à comprendre l'évolution du projet et à revenir à des versions spécifiques si nécessaire.

### Poussez vos modifications vers GitHub.

La commande "git push" est utilisée pour pousser (envoyer) les commits locaux vers un référentiel distant, généralement situé sur une plateforme de gestion de code telle que GitHub, GitLab ou Bitbucket.

```
git push 
```

Lorsque vous exécutez cette commande, Git compare les commits locaux que vous avez effectués avec ceux présents dans le référentiel distant. Il envoie uniquement les nouveaux commits locaux qui n'existent pas encore dans le référentiel distant

### Vérification du dépot et des commits sur [GitHub](https://github.com/) 


Pour vérifier les commits dans un dépôt GitHub, vous pouvez suivre les étapes suivantes :

1. Dans l'onglet du dépôt, vous trouverez plusieurs onglets différents tels que "Code", "Issues", "Pull requests", etc. Cliquez sur l'onglet "Commits" pour afficher la liste des commits.

2. La page des commits affiche les commits dans l'ordre chronologique, du plus récent au plus ancien. Chaque commit est accompagné d'un message de commit, de l'auteur du commit, de l'heure et de la date du commit, ainsi que des statistiques sur les modifications ajoutées ou supprimées.


En utilisant l'interface GitHub, vous pouvez facilement visualiser l'historique des commits, examiner les modifications apportées aux fichiers et les commentaires associés à chaque commit. Cela vous permet de suivre l'évolution du dépôt et de comprendre les changements qui ont été effectués au fil du temps.

Cela conclut l'atelier d'initialisation Git avec l'ajout et le commit de chaque fonction de la calculatrice séparément. 
