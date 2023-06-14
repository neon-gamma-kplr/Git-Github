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

![image](https://github.com/kplr-training/Git-Github/assets/123757632/2fe54518-acb9-4214-acac-8fcf51071f14)

### 3. Initialisation d'un nouveau dépôt :

Créez un nouveau dossier vide pour votre dépôt :

```
$ mkdir mon-depot
```

Cette commande crée un nouveau dossier (répertoire) portant le nom "mon-depot". Le terme "mkdir" est une abréviation de "make directory", qui signifie créer un répertoire. Une fois cette commande exécutée, un nouveau dossier vide portant le nom "mon-depot" est créé dans le répertoire actuel.

```
$ cd mon-depot
```

Cette commande permet de changer de répertoire (se déplacer vers un autre dossier). Le terme "cd" est une abréviation de "change directory". Lorsque vous exécutez cette commande, vous vous déplacez dans le dossier "mon-depot" qui vient d'être créé. Toutes les commandes ultérieures seront exécutées dans ce nouveau dossier.

### 4. Initialisez le dépôt Git en utilisant la commande suivante :

```
$ git init
```

La commande `git init` est utilisée pour initialiser un nouveau dépôt Git dans un répertoire existant. Lorsque vous exécutez cette commande, Git crée un sous-répertoire caché appelé ".git" dans le répertoire courant. Ce sous-répertoire contient toute la structure et les fichiers nécessaires pour suivre l'historique des modifications, gérer les branches, effectuer des commits, etc.

Le résultat de l'exécution de la commande `git init` est le suivant :

Git affiche un message indiquant que le dépôt est initialisé :
  ```
  Initialized empty Git repository in /chemin/vers/le/repertoire/.git/
  ```
Après l'initialisation du dépôt, vous pouvez commencer à ajouter des fichiers au suivi de Git, créer des commits et effectuer d'autres opérations liées à la gestion des versions avec Git.

![image](https://github.com/kplr-training/Git-Github/assets/123757632/7f316a73-d9dd-467c-9e48-5d57843695fc)

### 5. Création d'un fichier Python

Créez un fichier Python vide dans le dossier :

```
$ touch calculatrice.py
```

### 6. Ouvrez le fichier `calculatrice.py` et ajoutez les fonctions de calculatrice  

```
def addition(a, b):
  return a + b
```

### 7. Ajoutez le fichier `calculatrice.py` au suivi de Git en utilisant la commande suivante 

```
$ git add .
```

La commande `git add .` est utilisée pour ajouter le fichier `calculatrice.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### 8. Création d'un premier commit pour la fonction `addition` 

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

![image](https://github.com/kplr-training/Git-Github/assets/123757632/e6be4c6d-7964-4196-9def-bd4c135e2778)


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


![image](https://github.com/kplr-training/Git-Github/assets/123757632/d6c432e5-6c36-4dae-92ad-6d966ae3ab91)

### 10. Ajout d'autres fonctions et création de commits séparés :

Ajoutez d'autres fonctions de calculatrice dans le fichier `calculatrice.py`, par exemple une fonction `soustraction` :

```
def soustraction(a, b):
  return a - b
```

 ### 11. Ajoutez le fichier modifié au suivi :
 
```
git add .
```
La commande `git add .` est utilisée pour ajouter le fichier `calculatrice.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### 12. Créez un nouveau commit pour enregistrer la fonction `soustraction` :

```
git commit -m "Ajout de la fonction de soustraction"
```
Une fois le commit créé, les modifications apportées aux fichiers sont enregistrées de manière permanente dans le dépôt Git. 

![image](https://github.com/kplr-training/Git-Github/assets/123757632/60035140-0ce6-47dc-8b24-27e24eea99b9)

### 13. Vérification de l'historique des commits :

Affichez l'historique des commits en utilisant la commande suivante :

```
git log
```

L'historique des commits affiché par `git log` vous permet de visualiser les modifications apportées aux fichiers au fil du temps, ainsi que les auteurs et les messages associés à chaque commit. Cela vous aide à comprendre l'évolution du projet et à revenir à des versions spécifiques si nécessaire.

![image](https://github.com/kplr-training/Git-Github/assets/123757632/289c8f86-8f64-440f-b0f4-f61aef8e3100)


7. Publier le dépôt sur un serveur distant (optionnel) :
   - Créez un nouveau dépôt vide sur une plateforme de gestion de code telle que GitHub, GitLab ou Bitbucket.
   - Associez le dépôt local à votre dépôt distant en utilisant la commande suivante (remplacez l'URL par celle de votre dépôt distant) :
     ```
     git remote add origin <URL_du_depot distant>
     ```
   - Poussez votre dépôt local vers le dépôt distant :
     ```
     git push -u origin master
     ```

Cela conclut l'atelier d'initialisation Git avec l'ajout et le commit de chaque fonction de la calculatrice séparément. Vous avez maintenant un dép
