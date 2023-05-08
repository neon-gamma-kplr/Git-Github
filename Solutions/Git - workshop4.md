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
1. Créez un nouveau repository Github.

Connectez-vous à votre compte GitHub et cliquez sur le bouton "New" pour créer un nouveau dépôt. Donnez un nom et une description au dépôt et choisissez les options appropriées, telles que la visibilité et le fichier README.md. Cliquez sur le bouton "Create repository" pour créer le nouveau dépôt.

![image](https://user-images.githubusercontent.com/123757632/236680232-fe9c3b4c-8f94-4ba7-a767-65df9e351072.png)

2. Récupérez le dossier et téléchargez-le.
3. Transformez-le en dépôt Git.
```
git init
```
4. Ajoutez le dossier a l'index Git.
```
git add .
```
5. Commitez votre nouveau dossier.
```
git commit -m "Initial commit"
```
6. Ajoutez un dépôt distant à votre dossier local.
```
git remote add origin https://github.com/<nom-utilisateur>/<nom-repo>
```
7. Poussez vos modifications vers GitHub.
```
git push -u origin master
```
8. Ajoutez votre binome en tant que colaborateur.

Pour ajouter un collaborateur à un dépôt GitHub, suivez les étapes suivantes:

Allez dans votre nouveau dépôt puis cliquez sur le bouton "Settings" en haut de la page du dépôt , cliquez sur "Collaborators" puis "Add people" , entrez le nom d'utilisateur ou l'adresse e-mail du collaborateur que vous souhaitez inviter et cliquez sur le bouton " Add collaborator to this repository" .

Le collaborateur recevra alors une invitation par e-mail. Il devra l'accepter pour accéder au dépôt. Une fois qu'il aura accepté l'invitation, le collaborateur pourra cloner le repo et y contribuer en fonction de son niveau d'accès.

![image](https://user-images.githubusercontent.com/123757632/222380018-39212414-882d-412f-a6a4-63348bba1ce6.png)

### Binome 2
9. Clonez le depot de votre binome. 
```
git clone https://github.com/<nom-utilisateur>/<nom-repo>
```
10. Créez une branche et publiez la.
```
git checkout -b <nom_branche>
```
```
git push -u origin <nom_branche>
```
11. Ajoutez du text au fichier *chat.html.

![image](https://user-images.githubusercontent.com/123757632/236679214-771003b6-f3ec-49d5-9c50-ca38bc1d7414.png)

12. Ajoutez le fichier a l'index Git.
```
git add chat.html
```
13. Commitez les modifications avec le message "Message de Binome 2".
```
git commit -m "Message de Binome 2"
```
14. Poussez le dernier commit.
```
git push
```
15. Créez un Pull Request.
Si vous souhaitez apporter des modifications à une branche existante et que ces modifications doivent être fusionnées avec une autre branche, vous pouvez créer une demande de retrait "Pull Request".

* Cliquez sur le bouton "New pull request" sur la page de la branche, sélectionnez la branche de destination et créez la demande de retrait.

![image (2)](https://user-images.githubusercontent.com/123757632/236679286-6c56f836-494d-49bb-93fc-5ec32f41c501.png)

* Puis choisissez la branche créée 

* Cliquez sur "Create pull request"

![image](https://user-images.githubusercontent.com/123757632/236679408-fd90a5da-2b48-4324-bf7a-822449a6e9f2.png)

* Veuillez saisir un message ou un commentaire a votre binome et cliquez sur " Create pull request"

![image](https://user-images.githubusercontent.com/123757632/236679520-2ace0c8f-30cc-41c5-ab0a-3d33cb4912be.png)

### Binome 1
16. Acceptez le Pull Request. 

* Pour accepter le Pull Request de votre binome cliquez sur "Pull requests" dans la bar de votre repository

![image](https://user-images.githubusercontent.com/123757632/236679653-7a935958-3137-4c44-bb83-f60bf267c85c.png)

* Puis cliquez sur la dernière pull request "Message de Binome 2"

![image](https://user-images.githubusercontent.com/123757632/236679719-d2a5a3d3-ef06-46d8-b6ab-b648f66148ac.png)

* Cliquez sur "Merge pull request" pour le fusioner

![image](https://user-images.githubusercontent.com/123757632/236680848-4b8f7181-00ca-4ecf-9aaf-f0bd24684c23.png)


* Après la verification du commentaire de votre binome , cliquez sur "Confirm merge"

![image](https://user-images.githubusercontent.com/123757632/236679857-f30c58cc-41a0-45de-a540-cf6d163069f5.png)

La dernière modification s'ajoutera automatiquement à la liste des dernières commits 

![image](https://user-images.githubusercontent.com/123757632/236679949-6d877c13-311d-48a0-aa42-accb22720b9d.png)


17. Mettez a jour votre copie locale.
```
git pull
```
18. Créez une branche et publiez la.
```
git checkout -b <nom_branche>
```
![image](https://user-images.githubusercontent.com/123757632/236680331-eaf61fe9-8410-4a72-a37b-8785f90be47a.png)

```
git push -u origin <nom_branche>
```

![image](https://user-images.githubusercontent.com/123757632/236680391-8224f2f9-0a2e-4864-be2c-501cf078bb14.png)

19. Ajoutez du text au fichier *chat.html.

![image](https://user-images.githubusercontent.com/123757632/236680425-51557953-f2a2-4b98-88d5-a86750b7d277.png)

20. Ajoutez le fichier a l'index Git.
```
git add chat.html
```
21. Commitez les modifications avec le message "Message de Binome 1".
```
git commit -m "Message de Binome 1"
```
![image](https://user-images.githubusercontent.com/123757632/236680499-e7f9bacf-6f4d-46bc-9398-2ea5197be423.png)

22. Poussez le dernier commit.
```
git push
```
![image](https://user-images.githubusercontent.com/123757632/236680550-256135e8-120e-4623-a3e6-aefd0248eadd.png)

23. Créez un Pull Request sur GitHub

![image](https://user-images.githubusercontent.com/123757632/236680594-3156fbcf-10dc-4663-b9dc-df5850f92ad8.png)

### Binome 2
24. Acceptez le Pull Request.

![image](https://user-images.githubusercontent.com/123757632/236680738-b609847a-7948-4a73-b7c5-cb0567245600.png)

![image](https://user-images.githubusercontent.com/123757632/236680874-1c3a02fc-ecb3-4f80-a6b0-43678ddb29d6.png)

![image](https://user-images.githubusercontent.com/123757632/236680691-4b89f787-800e-4631-b809-3af4a8d25cb1.png)

26. Mettez a jour votre copie locale.
```
git pull
```
