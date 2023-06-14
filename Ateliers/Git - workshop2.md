# GIT

## Objectif
L'objectif de cet atelier est d'approfondir vos compétences en travaillant avec les branches Git. 

Les branches sont utiles pour développer des fonctionnalités de manière isolée et collaborer efficacement sur un projet. Vous apprendrez à créer et à basculer entre les branches, à fusionner les modifications entre les branches, et à résoudre les éventuels conflits. 

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

![image](https://github.com/kplr-training/Git-Github/assets/123757632/fa6ddeba-35ae-4e7d-9eba-d4782b868ece)

### 5. Création d'un fichier Python

Créez un fichier Python vide dans le dossier :

```
$ touch gestion_eleves.py
```

### 6. Création de la nouvelle branche ajouter_eleve

Une branche est une ligne de développement isolée qui permet aux utilisateurs de travailler sur des fonctionnalités, des correctifs ou des expérimentations sans affecter la branche principale du projet, généralement appelée "branche principale" ou "branche maître" (par convention, "master" en anglais).

```
git branch ajouter_eleve
```
La commande "git branch ajouter_eleve" est utilisée pour créer une nouvelle branche dans un référentiel Git avec le nom "ajouter_eleve". 

### 7. Basculer vers la branche ajouter_eleve

La commande "git checkout ajouter_eleve" est utilisée pour basculer vers une branche spécifique dans un référentiel Git. Dans ce cas, la branche spécifique est "ajouter_eleve".

```
git checkout ajouter_eleve
```
Lorsque vous exécutez cette commande, Git met à jour votre répertoire de travail pour refléter l'état de la branche spécifiée. Cela signifie que les fichiers dans votre répertoire de travail seront modifiés pour correspondre à l'état de la branche "ajouter_eleve". Les modifications non validées dans votre branche actuelle peuvent être perdues si elles ne sont pas sauvegardées ou validées avant de passer à une autre branche.

![image](https://github.com/kplr-training/Git-Github/assets/123757632/24c4ffde-b190-4022-8549-6a743cf26dc9)

### 8. Ouvrez le fichier `eleves.py` et ajoutez la fonction pour ajouter un elève

```
def ajouter_élève():
    id_élève = input("Entrez l'identifiant de l'élève : ")
    nom_élève = input("Entrez le nom de l'élève : ")
    élèves[id_élève] = nom_élève
    print("Élève ajouté avec succès !")
```
La fonction ajouter_élève permet à l'utilisateur d'entrer l'identifiant et le nom d'un nouvel élève, puis ajoute ces informations au dictionnaire élèves.

![image](https://github.com/kplr-training/Git-Github/assets/123757632/49aa3126-4234-4c07-8d80-8e5c0f462982)

### 9.




