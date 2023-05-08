# GIT 

## Objectif
Apprendre comment commettre des changements dans des dépôts Git.

## Instructions

1. Créez votre compte Github en visitant le lien suivant : [GitHub](https://github.com/signup?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home)
2. Configurer Git.
```
git config --global user.name "Votre nom d'utilisateur"
git config --global user.email "Votre adresse e-mail"
```
Configurer le nom d'utilisateur et l'adresse e-mail pour les commits Git. Lorsque vous effectuez un commit Git, ces informations sont incluses pour que les autres développeurs sachent qui a effectué le commit et comment les contacter si nécessaire.

3. Créez un nouveau répertoire.
```
mkdir <nom_repo> && cd <nom_repo>
```

![image](https://user-images.githubusercontent.com/123757632/236469940-3c4f5651-8152-4c96-b5ae-c8c05e2fa818.png)

Cette commande permet de créer un nouveau répertoire avec un nom donné en utilisant **mkdir** et de se déplacer dans ce nouveau répertoire en utilisant **cd**.

4. Transformez-le en dépôt Git.
```
git init
```

![image](https://user-images.githubusercontent.com/123757632/236470579-2aea337d-c32f-4636-a459-d55a902a0688.png)

Cette commande initialise un nouveau dépôt Git dans le répertoire courant ou dans un répertoire spécifié en créant un dossier caché appelé **".git"**.

Après l'exécution de la commande **git init**, le répertoire est prêt à être utilisé comme un dépôt Git local pour suivre les changements, créer des commits, des branches, des tags, etc.

5. Créez un nouveau fichier nommé "file" contenant le texte "hello commit".
```
echo "hello_commit" > file
```

![image](https://user-images.githubusercontent.com/123757632/236479705-e0c7c87b-4f3c-4515-9bea-1ca271ea9000.png)

**echo "hello_commit" > file** est une commande Bash qui permet de créer un fichier nommé **"file"** dans le répertoire courant ou de le remplacer s'il existe déjà. 

Le contenu du fichier est **"hello_commit"**, qui est la chaîne de caractères passée en argument de la commande echo.

La redirection **>** permet de rediriger la sortie de la commande echo vers le fichier **"file"**. 

Ainsi, suite à l'exécution de cette commande, un fichier appelé **"file"** sera créé dans le répertoire courant contenant la chaîne de caractères **"hello_commit"**.

6. Ajoutez le fichier "file" a l'index Git.
```
git add file
```
**git add file** est une commande Git qui permet d'ajouter le fichier **"file"** à l'index Git. 

Cela signifie que le fichier est maintenant suivi par Git et que les modifications apportées à ce fichier seront incluses dans le prochain commit.

Il est important d'utiliser la commande **git add** avant de faire un commit pour que Git sache quels fichiers doivent être inclus dans ce commit.

7. Commitez votre nouveau fichier.
```
git commit -a -m "Mon premier Commit!"
```

![image](https://user-images.githubusercontent.com/123757632/236480104-edd0516e-61b9-4dd9-861e-9a6938070e69.png)

**git commit -a -m "Mon premier Commit!"** est une commande Git qui crée un nouveau commit avec un message de commit spécifié.

L'option **-a** permet d'ajouter automatiquement tous les fichiers modifiés ou supprimés dans l'index, mais cela ne fonctionne pas pour les nouveaux fichiers. 

L'option **-m** est utilisée pour spécifier le message de commit en ligne de commande, plutôt que d'ouvrir un éditeur de texte pour saisir le message.

Donc, après avoir exécuté cette commande, un nouveau commit sera créé contenant les modifications de tous les fichiers ajoutés à l'index, avec le message de commit **"Mon premier Commit!"**.

8. Exécutez une commande Git pour vérifier que votre commit a bien été enregistré.
```
git log
```

![image](https://user-images.githubusercontent.com/123757632/236480623-bca227f7-51be-464d-8003-558c0aa2ad8c.png)

**git log** est une commande Git qui affiche l'historique des commits dans l'ordre chronologique inverse, du plus récent au plus ancien.

Cette commande est utile pour visualiser l'historique des commits d'un dépôt Git et pour suivre les modifications apportées aux fichiers au fil du temps.
