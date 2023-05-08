# GIT

## Objectif
Apprendre à travailler avec les branches Git

## Instructions

1. Choisissez un dépôt Git (ou créez-en un nouveau) avec au moins un commit
```
cd <nom_repo>
```
Cette commande permet de se déplacer dans le répertoire <nom_repo>.

2. Créez un nouveau fichier appelé "file1" et écrit la chaîne de caractères "master branch" à l'intérieur
```
echo "master branch" > file1
```

![image](https://user-images.githubusercontent.com/123757632/236496598-19176fb2-3165-4b5f-9482-f2fb035f37d5.png)

Cette commande crée un fichier appelé **file1** dans le répertoire courant et y ajoute le texte **"master branch"**. Si le fichier file1 existe déjà, son contenu sera remplacé par **"master branch"**.

3. Ajoutez le fichier "file1" à l'index Git pour préparer le commit
```
git add file1
```

Cette commande ajoute le fichier **"file1"** à la staging area de Git, ce qui signifie que le fichier est prêt à être inclus dans le prochain commit.

4. Créez un nouveau commit contenant tous les fichiers ajoutés ou modifiés 
```
git commit -a -m "added file1"
```

![image](https://user-images.githubusercontent.com/123757632/236497391-1eec3c90-9d75-4ffc-9d02-bdb9de46625c.png)

Cette commande crée **un commit** contenant toutes les modifications apportées aux fichiers suivis par Git. 

L'option **-a** permet d'inclure les modifications de tous les fichiers modifiés, sans avoir besoin de les ajouter individuellement avec la commande git add. 

L'option **-m** est utilisée pour ajouter un message au commit, ce qui permet de décrire brièvement les modifications apportées. 

Dans ce cas, le message est **"added file1"**.

5. Créez une nouvelle branche appelée "dev"
```
git checkout -b dev
```

![image](https://user-images.githubusercontent.com/123757632/236498111-5c36f97e-c878-4502-b4b5-ce3c9dfadc7b.png)

La commande **"git checkout -b dev"** crée une nouvelle branche appelée **"dev"** et la positionne en tant que branche de **travail active**. 

Cela signifie que toutes les modifications apportées seront enregistrées sur la branche **"dev"** et non sur la branche principale **"master"**.

6. Créez un nouveau fichier appelé "file2" et écrit la chaîne de caractères "dev branch" à l'intérieur
```
echo "dev branch" > file2
```

![image](https://user-images.githubusercontent.com/123757632/236498781-2626d6fc-3987-45b9-978f-55513ffc7b84.png)

Cette commande crée un nouveau fichier nommé **"file2"** contenant la chaîne de caractères **"dev branch"**.

7. Ajoutez le fichier "file2" à l'index Git pour préparer le commit
```
git add file2
```
Cette commande ajoute le fichier **"file2"** à la staging area de Git, ce qui signifie que le fichier est prêt à être inclus dans le prochain commit.

8. Créez un nouveau commit
```
git commit -a -m "added file2"
```
![image](https://user-images.githubusercontent.com/123757632/236498604-5a15c163-aa35-4fa3-b67e-87201c27665f.png)

La commande **"git commit -a -m "added file2""** permet de créer un nouveau commit dans le dépôt Git local avec un message de commit spécifique et d'inclure automatiquement tous les fichiers modifiés et supprimés dans ce commit.

Plus en détail, voici ce que chaque partie de cette commande fait :

* **"git commit"** crée un nouveau commit dans le dépôt Git local
* **"-a"** est un raccourci pour "--all", qui indique à Git d'inclure automatiquement tous les fichiers modifiés et supprimés dans le commit.
* **"-m"** est un raccourci pour "--message", qui permet de spécifier le message de commit en ligne de commande plutôt que d'ouvrir un éditeur de texte.
* **"added file2"** est le message de commit spécifique qui décrit les modifications apportées au dépôt.

9. Vérifiez que le commit que vous avez créé se trouve uniquement dans la branche "dev" (Vous devriez voir deux commits)
```
git log 
```
![image](https://user-images.githubusercontent.com/123757632/236501080-e05ba483-40cb-44f3-a422-75c0f3db6209.png)

La commande **"git log"** est utilisée pour afficher l'historique des commits dans le dépôt Git local. Cette commande affiche une liste de tous les commits en commençant par le plus récent et en remontant jusqu'au plus ancien.

10. Vérifiez la branche "master" (Vous devriez voir un commit)
```
git checkout master
````
![image](https://user-images.githubusercontent.com/123757632/236501513-8fe8bc93-5bb7-49d6-8c8a-a9b89c602a32.png)

La commande **"git checkout master"** est utilisée pour basculer vers la branche principale **(par défaut)** d'un dépôt Git.

```
git log 
```
![image](https://user-images.githubusercontent.com/123757632/236501830-bec3d9dd-553e-4ec1-941a-15550e93d02c.png)

