# GIT 

## Objectif
Apprendre comment commettre des changements dans des dépôts Git.

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
$ touch calculatrice.py
```

### 4. Ouvrez le fichier `calculatrice.py` et ajoutez les fonctions de calculatrice  

```
def addition(a, b):
  return a + b
```

### 5. Ajoutez le fichier `calculatrice.py` au suivi de Git en utilisant la commande suivante 

```
$ git add .
```

La commande `git add .` est utilisée pour ajouter le fichier `calculatrice.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### 6. Création d'un premier commit pour la fonction `addition` 

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

### 7. Afficher l'historique des commits et vérifier que votre commit a été enregistré avec succès

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

### 8. Ajout d'autres fonctions :

Ajoutez d'autres fonctions de calculatrice dans le fichier `calculatrice.py`, par exemple une fonction `soustraction` :

```
def soustraction(a, b):
  return a - b
```

 ### 9. Ajoutez le fichier modifié au suivi :
 
```
git add .
```
La commande `git add .` est utilisée pour ajouter le fichier `calculatrice.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### 10. Créez un nouveau commit pour enregistrer la fonction `soustraction` :

```
git commit -m "Ajout de la fonction de soustraction"
```
Une fois le commit créé, les modifications apportées aux fichiers sont enregistrées de manière permanente dans le dépôt Git. 

### 11. Vérification de l'historique des commits :

Affichez l'historique des commits en utilisant la commande suivante :

```
git log
```

L'historique des commits affiché par `git log` vous permet de visualiser les modifications apportées aux fichiers au fil du temps, ainsi que les auteurs et les messages associés à chaque commit. Cela vous aide à comprendre l'évolution du projet et à revenir à des versions spécifiques si nécessaire.

### 12. Ajout d'autres fonctions :

Ajoutez d'autres fonctions de calculatrice dans le fichier `calculatrice.py`, par exemple une fonction `multiplication` :

```
def multiplication(a, b):
    return a * b
```

 ### 13. Ajoutez le fichier modifié au suivi :
 
```
git add .
```
La commande `git add .` est utilisée pour ajouter le fichier `calculatrice.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### 14. Créez un nouveau commit pour enregistrer la fonction `multiplication` :

```
git commit -m "Ajout de la fonction de multiplication"
```
Une fois le commit créé, les modifications apportées aux fichiers sont enregistrées de manière permanente dans le dépôt Git. 

### 15. Vérification de l'historique des commits :

Affichez l'historique des commits en utilisant la commande suivante :

```
git log
```

L'historique des commits affiché par `git log` vous permet de visualiser les modifications apportées aux fichiers au fil du temps, ainsi que les auteurs et les messages associés à chaque commit. Cela vous aide à comprendre l'évolution du projet et à revenir à des versions spécifiques si nécessaire.

### 16. Ajout d'autres fonctions :

Ajoutez d'autres fonctions de calculatrice dans le fichier `calculatrice.py`, par exemple une fonction `division` :

```
def division(a, b):
    if b != 0:
        return a / b
    else:
        return "Erreur : Division par zéro"

```

 ### 17. Ajoutez le fichier modifié au suivi :
 
```
git add .
```
La commande `git add .` est utilisée pour ajouter le fichier `calculatrice.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### 18. Créez un nouveau commit pour enregistrer la fonction `division` :

```
git commit -m "Ajout de la fonction de division"
```
Une fois le commit créé, les modifications apportées aux fichiers sont enregistrées de manière permanente dans le dépôt Git. 

### 19. Vérification de l'historique des commits :

Affichez l'historique des commits en utilisant la commande suivante :

```
git log
```

L'historique des commits affiché par `git log` vous permet de visualiser les modifications apportées aux fichiers au fil du temps, ainsi que les auteurs et les messages associés à chaque commit. Cela vous aide à comprendre l'évolution du projet et à revenir à des versions spécifiques si nécessaire.

### 20. Ajout d'autres fonctions :

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

 ### 21. Ajoutez le fichier modifié au suivi :
 
```
git add .
```
La commande `git add .` est utilisée pour ajouter le fichier `calculatrice.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### 22. Créez un nouveau commit pour enregistrer la fonction `calculatrice` :

```
git commit -m "Ajout de la fonction de calculatrice"
```
Une fois le commit créé, les modifications apportées aux fichiers sont enregistrées de manière permanente dans le dépôt Git. 

### 23. Vérification de l'historique des commits 

Affichez l'historique des commits en utilisant la commande suivante :

```
git log
```

L'historique des commits affiché par `git log` vous permet de visualiser les modifications apportées aux fichiers au fil du temps, ainsi que les auteurs et les messages associés à chaque commit. Cela vous aide à comprendre l'évolution du projet et à revenir à des versions spécifiques si nécessaire.


### 24. Publier le dépôt sur [GitHub](https://github.com/) 

Créez un nouveau dépôt vide sur une plateforme de gestion de code telle que GitHub.

#### Associez le dépôt local à votre dépôt distant en utilisant la commande suivante (remplacez l'URL par celle de votre dépôt distant) 
     
```
git remote add origin <URL_du_depot distant>
```

La commande `git remote add origin <URL_du_depot_distant>` est utilisée pour associer un dépôt distant à votre dépôt Git local. L'argument `<URL_du_depot_distant>` doit être remplacé par l'URL du dépôt distant auquel vous souhaitez vous connecter. Cela peut être une URL HTTPS ou SSH, dépendant de votre configuration.

Explication de la commande :

- `git remote` est la commande pour gérer les dépôts distants.
- `add origin` est utilisé pour ajouter un nouveau dépôt distant avec le nom "origin". "origin" est souvent utilisé par convention pour désigner le dépôt distant principal.
- `<URL_du_depot_distant>` est l'URL du dépôt distant que vous souhaitez associer à votre dépôt local. Par exemple, si vous utilisez GitHub, l'URL peut ressembler à `https://github.com/votre-utilisateur/votre-depot.git`.

Résultat de l'exécution de la commande :

- Si la commande est exécutée avec succès, elle n'affiche généralement aucun message.
- L'URL du dépôt distant est enregistrée sous le nom "origin" dans votre dépôt local. Cela vous permet de référencer facilement le dépôt distant lors de l'exécution de commandes telles que `git push` ou `git pull`.


#### Poussez votre dépôt local vers le dépôt distant :

```
git push -u origin master
```

La commande `git push -u origin master` est utilisée pour pousser les commits de la branche "master" vers le dépôt distant associé à l'alias "origin". L'option `-u` est utilisée pour configurer la branche locale "master" pour qu'elle suive la branche distante "master" sur le dépôt distant "origin".

Explication de la commande :

- `git push` est la commande pour pousser les commits vers un dépôt distant.
- `-u` est une option qui permet de configurer la branche locale pour qu'elle suive la branche distante.
- `origin` est l'alias donné au dépôt distant au moment de l'association avec `git remote add origin <URL_du_depot_distant>`.
- `master` est le nom de la branche locale que vous souhaitez pousser vers le dépôt distant.

Résultat de l'exécution de la commande :

- Si la commande est exécutée avec succès et qu'il n'y a pas de problèmes de connectivité ou d'autorisations, Git pousse les commits de la branche locale "master" vers la branche distante "master" sur le dépôt distant "origin".
- Git affiche des informations sur les commits poussés, ainsi que des statistiques sur les modifications ajoutées ou supprimées.
- Par exemple :
  ```
  Enumerating objects: 5, done.
  Counting objects: 100% (5/5), done.
  Delta compression using up to 4 threads
  Compressing objects: 100% (3/3), done.
  Writing objects: 100% (3/3), 300 bytes | 300.00 KiB/s, done.
  Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
  To <URL_du_depot_distant>
     f7fde4f..2cfd3b1  master -> master
  ```
 

### 25. Vérification du dépot et des commits sur [GitHub](https://github.com/) 


Pour vérifier les commits dans un dépôt GitHub, vous pouvez suivre les étapes suivantes :

1. Dans l'onglet du dépôt, vous trouverez plusieurs onglets différents tels que "Code", "Issues", "Pull requests", etc. Cliquez sur l'onglet "Commits" pour afficher la liste des commits.

2. La page des commits affiche les commits dans l'ordre chronologique, du plus récent au plus ancien. Chaque commit est accompagné d'un message de commit, de l'auteur du commit, de l'heure et de la date du commit, ainsi que des statistiques sur les modifications ajoutées ou supprimées.


En utilisant l'interface GitHub, vous pouvez facilement visualiser l'historique des commits, examiner les modifications apportées aux fichiers et les commentaires associés à chaque commit. Cela vous permet de suivre l'évolution du dépôt et de comprendre les changements qui ont été effectués au fil du temps.

Cela conclut l'atelier d'initialisation Git avec l'ajout et le commit de chaque fonction de la calculatrice séparément. 
