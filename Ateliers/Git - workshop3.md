# Git & GitHub Workshop 3
Dans cet atelier GitHub, nous allons vous guider à travers les étapes pour créer un nouveau dépôt, créer une branche, effectuer des commits, créer des demandes de retrait et cloner un dépôt existant , et pour finir nous allons créeation d'un référentiel distant.

# 1 . Création d'un nouveau dépôt 
Connectez-vous à votre compte GitHub et cliquez sur le bouton "New" pour créer un nouveau dépôt. Donnez un nom et une description au dépôt et choisissez les options appropriées, telles que la visibilité et le fichier README.md. Cliquez sur le bouton "Create repository" pour créer le nouveau dépôt.

![image](https://user-images.githubusercontent.com/123757632/221904279-c5a2d920-5b45-4193-b599-1cc21daae210.png)
# 2 . Ajouter un collaborateur 
Pour ajouter un collaborateur à un dépôt GitHub, suivez les étapes suivantes:

Allez dans votre nouveau dépôt puis cliquez sur le bouton "Settings" en haut de la page du dépôt , cliquez sur "Collaborators" puis "Add people" , entrez le nom d'utilisateur ou l'adresse e-mail du collaborateur que vous souhaitez inviter et cliquez sur le bouton " Add collaborator to this repository" .

Le collaborateur recevra alors une invitation par e-mail. Il devra l'accepter pour accéder au dépôt. Une fois qu'il aura accepté l'invitation, le collaborateur pourra cloner le repo et y contribuer en fonction de son niveau d'accès.

![image](https://user-images.githubusercontent.com/123757632/222380018-39212414-882d-412f-a6a4-63348bba1ce6.png)

# 3 . Création d'une branche 
Pour créer une nouvelle branche, Allez dans votre nouveau dépôt. Appuyez sur le bouton principal et entrez le nom de votre nouvelle branche de fonctionnalité. Cliquez sur Créer une branche

![image](https://user-images.githubusercontent.com/123757632/221905296-bb65ad5a-09f5-4745-87b4-2d15b57b3826.png)

# 4 . Effectuer et valider un changement 
Voici comment effectuer et valider un changement :

Accédez à la branche de fonctionnalité en cliquant sur principal et en sélectionnant votre branche nouvellement créée dans le menu déroulant 
![image](https://user-images.githubusercontent.com/123757632/221906014-974748a8-ac15-4911-9233-fbd221e7a4ef.png)

Cliquez sur l’icône « crayon » pour commencer à modifier le fichier. Une fois que vous avez terminé, écrivez une brève description des modifications apportées. Cliquez sur Commiter les modifications.

![image](https://user-images.githubusercontent.com/123757632/221906262-19d84614-65db-49e2-8494-f9f35dcb765a.png)

# 5 . Création de demandes de retrait 

Si vous souhaitez apporter des modifications à une branche existante et que ces modifications doivent être fusionnées avec une autre branche, vous pouvez créer une demande de retrait. 

Cliquez sur le bouton "New pull request" sur la page de la branche, sélectionnez la branche de destination et créez la demande de retrait.
![image](https://user-images.githubusercontent.com/123757632/221906794-9f97735b-0c60-4483-94e9-ae0f5dec781b.png)

Examinez les modifications une fois de plus et cliquez sur Créer une pull request. Sur la nouvelle page, écrivez le titre et fournissez une courte description de ce sur quoi vous avez travaillé pour encourager la fusion. Cliquez sur Créer une pull request . 
Pour faire une requête pull, suivez les étapes ci-dessous :
![image](https://user-images.githubusercontent.com/123757632/221907414-c00476f9-50dc-4312-a908-ac532c3bb27c.png)


# 6 . Clonage d'un dépôt 

Pour cloner un dépôt existant, accédez à la page du dépôt sur GitHub, cliquez sur le bouton "Clone or download" et copiez l'URL du dépôt.
![image](https://user-images.githubusercontent.com/123757632/221907903-06ae3b01-5648-4438-bf1d-5f5c72946693.png)


Utilisez la commande "git clone" pour cloner le dépôt sur votre ordinateur.
```
git clone https://github.com/USERNAME/NOM-REFERENTIEL.git
```

# 7 . Création d'un référentiel distant 

Pour créer un référentiel distant, ajouter un remote au dépôt local à l'aide de la commande "git remote add". 
```
git remote add origin url_du_référentiel_distant
git push -u origin nom_de_la_branche
```


Cela termine notre atelier GitHub. Vous avez maintenant appris à créer un nouveau dépôt, créer une branche, effectuer des commits, créer des demandes de retrait et cloner un dépôt existant. Enfin, nous avons créé un référentiel distant pour synchroniser vos modifications avec les dépôts en ligne.





