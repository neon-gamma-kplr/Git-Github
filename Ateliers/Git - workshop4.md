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

#### Créer un nouveau repository Github Vide

Connectez-vous à votre compte GitHub et cliquez sur le bouton "New" pour créer un nouveau dépôt. Donnez un nom et une description au dépôt et choisissez les options appropriées, telles que la visibilité et le fichier README.md. Cliquez sur le bouton "Create repository" pour créer le nouveau dépôt.

![image](https://user-images.githubusercontent.com/123757632/221904279-c5a2d920-5b45-4193-b599-1cc21daae210.png)

#### Ajouter votre binome en tant que colaborateur
   
![image](https://github.com/kplr-training/Git-Github/assets/123757632/bf3433ae-bc21-4400-b16f-af728985461d)
![image](https://github.com/kplr-training/Git-Github/assets/123757632/861ec46f-7bfe-4e0b-abb3-82d831829b99)

#### Ouvrir le dépot Github directement sur Gitpod

#### Créer un ficher python banque.py

Créez un fichier Python vide dans le dossier :

```
$ touch banque.py
```

#### Ajoutez le dossier a l'index Git

```
$ git add .
```

La commande `git add .` est utilisée pour ajouter le fichier `devise.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

#### Création d'un premier commit

La commande "git commit -m 'Initial commit'" est utilisée pour créer un nouveau commit dans le référentiel Git. Un commit est une capture instantanée des modifications apportées aux fichiers du projet à un moment précis.

```
git commit -m "Initial commit"
```

#### Poussez vos modifications vers GitHub.

La commande "git push" est utilisée pour pousser (envoyer) les commits locaux vers un référentiel distant, généralement situé sur une plateforme de gestion de code telle que GitHub, GitLab ou Bitbucket.

```
git push 
```

Lorsque vous exécutez cette commande, Git compare les commits locaux que vous avez effectués avec ceux présents dans le référentiel distant. Il envoie uniquement les nouveaux commits locaux qui n'existent pas encore dans le référentiel distant

### Binome 2

#### Accepter l'invitation de votre binome 

  cliquer sur l'icone de la cloche qui se trouve dans la navbar a droite , puis cliquer sur "accepter l'invitation"
  
  ![image](https://github.com/kplr-training/Git-Github/assets/123757632/bdc164ea-2792-4217-ac9a-a2c74ae35cb7)
  
#### Ouvrir le dépot Github directement sur Gitpod en utilisant l'url du dépot de votre binome

#### Création de la nouvelle branche compte_bancaire_binome2

Une branche est une ligne de développement isolée qui permet aux utilisateurs de travailler sur des fonctionnalités, des correctifs ou des expérimentations sans affecter la branche principale du projet, généralement appelée "branche principale" ou "branche maître" (par convention, "master" en anglais).

```
git branch compte_bancaire_binome2
```
La commande "git branch compte_bancaire_binome2" est utilisée pour créer une nouvelle branche dans un référentiel Git avec le nom "compte_bancaire_binome2". 

#### Basculer vers la branche compte_bancaire_binome2

La commande "git checkout compte_bancaire_binome2" est utilisée pour basculer vers une branche spécifique dans un référentiel Git. Dans ce cas, la branche spécifique est "compte_bancaire_binome2".

```
git checkout compte_bancaire_binome2
```
Lorsque vous exécutez cette commande, Git met à jour votre répertoire de travail pour refléter l'état de la branche spécifiée. Cela signifie que les fichiers dans votre répertoire de travail seront modifiés pour correspondre à l'état de la branche "compte_bancaire_binome2". Les modifications non validées dans votre branche actuelle peuvent être perdues si elles ne sont pas sauvegardées ou validées avant de passer à une autre branche.

#### Ouvrez le fichier `banque.py` et ajoutez la fonction CompteBancaire

```
class CompteBancaire:
    def __init__(self, numero_compte, solde=0):
        self.numero_compte = numero_compte
        self.solde = solde
    
    def deposer(self, montant):
        self.solde += montant
    
    def retirer(self, montant):
        if self.solde >= montant:
            self.solde -= montant
        else:
            print("Solde insuffisant.")
    
    def transferer(self, compte_destinataire, montant):
        if self.solde >= montant:
            self.solde -= montant
            compte_destinataire.deposer(montant)
        else:
            print("Solde insuffisant.")
```

#### Ajoutez le fichier `banque.py` au suivi de Git en utilisant la commande suivante 

```
$ git add .
```

La commande `git add .` est utilisée pour ajouter le fichier `banque.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

#### Création du commit pour la classe `CompteBancaire` 

Créez un commit pour enregistrer la fonction `CompteBancaire` 

```
$ git commit -m "Ajout de la classe CompteBancaire"
```

La commande `git commit -m "Ajout de la classe CompteBancaire"` est utilisée pour créer un nouveau commit dans le dépôt Git. Un commit est une capture instantanée des modifications apportées aux fichiers suivis par Git.

Explication de la commande :

* `git commit` est la commande principale pour créer un commit.
* `-m "Ajout de la classe CompteBancaire"` est un paramètre qui permet de spécifier le message du commit. Le message doit être placé entre guillemets.

Une fois le commit créé, les modifications apportées aux fichiers sont enregistrées de manière permanente dans le dépôt Git. 

#### Afficher l'historique des commits et vérifier que votre commit a été enregistré avec succès

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

##### Pousser le fichier banque.py vers la branche compte_bancaire_binome2

Pour pousser votre branche nommée "compte_bancaire_binome2" vers le dépôt distant nommé "origin" dans Git, vous pouvez utiliser la commande suivante :

```
git push origin compte_bancaire_binome2
```

Cette commande va pousser les commits de votre branche locale "compte_bancaire_binome2" vers la branche "compte_bancaire_binome2" du dépôt distant appelé "origin".

#### Accédez au référentiel distant sur [GitHub](https://github.com/) 

Cliquez sur le bouton "Compare & Pull Request" (demande de tirage) pour créer une nouvelle demande de tirage.

![image](https://github.com/kplr-training/Git-Github/assets/123757632/03e9d5da-bdf9-43f6-8d8d-dda9570014bc)


Ajoutez une description pour votre demande de tirage et soumettez-la.

![image](https://github.com/kplr-training/Git-Github/assets/123757632/931e21e2-c6bc-4cb3-83c0-7ad1d1ea452b)

Votre collaborateur "binome1" peut maintenant examiner votre demande de tirage, ajouter des commentaires et demander des modifications supplémentaires si nécessaire.

### Binome 1 

#### Fusionner et confirmer le pull request 

![image](https://github.com/kplr-training/Git-Github/assets/123757632/915e65f5-53d8-47f5-b28b-1d825befd266)

![image](https://github.com/kplr-training/Git-Github/assets/123757632/613dc419-553d-4ca4-a7a6-9404bb9f0618)

Pour fusionner le pull request cliquer sur Merge pull request puis Confirm merge

![image](https://github.com/kplr-training/Git-Github/assets/123757632/3b5af0dd-f9f7-4c53-b3c3-6cb63bbb0918)

#### Verifier les commits dans votre repository 

![image](https://github.com/kplr-training/Git-Github/assets/123757632/7a4bb06f-889a-4ca9-83db-876ed451d82d)

#### Récupérer les dernières modifications à partir d'un dépôt distant

La commande git pull est utilisée pour récupérer les dernières modifications à partir d'un dépôt distant (par exemple, un référentiel Git distant tel que GitHub) et les fusionner avec votre branche locale.

```
git pull 
```

##### Création de la nouvelle branche gestion_compte_bancaire_binome1

Une branche est une ligne de développement isolée qui permet aux utilisateurs de travailler sur des fonctionnalités, des correctifs ou des expérimentations sans affecter la branche principale du projet, généralement appelée "branche principale" ou "branche maître" (par convention, "master" en anglais).

```
git branch gestion_compte_bancaire_binome1
```
La commande "git branch gestion_compte_bancaire_binome1" est utilisée pour créer une nouvelle branche dans un référentiel Git avec le nom "gestion_compte_bancaire_binome1". 

##### Basculer vers la branche gestion_compte_bancaire_binome1

La commande "git checkout gestion_compte_bancaire_binome1" est utilisée pour basculer vers une branche spécifique dans un référentiel Git. Dans ce cas, la branche spécifique est "gestion_compte_bancaire_binome1".

```
git checkout gestion_compte_bancaire_binome1
```
Lorsque vous exécutez cette commande, Git met à jour votre répertoire de travail pour refléter l'état de la branche spécifiée. Cela signifie que les fichiers dans votre répertoire de travail seront modifiés pour correspondre à l'état de la branche "gestion_compte_bancaire_binome1". Les modifications non validées dans votre branche actuelle peuvent être perdues si elles ne sont pas sauvegardées ou validées avant de passer à une autre branche.

##### Ouvrez le fichier `banque.py` et ajoutez la fonction gestion_compte_bancaire()

```
def gestion_compte_bancaire():
    compte1 = CompteBancaire("123456", 5000)
    compte2 = CompteBancaire("789012", 3000)

    print("Bienvenue dans le système de gestion des comptes bancaires.")

    while True:
        print("\nQue souhaitez-vous faire ?")
        print("1. Déposer de l'argent")
        print("2. Retirer de l'argent")
        print("3. Transférer de l'argent")
        print("4. Quitter")

        choix = input("Votre choix (1-4) : ")

        if choix == "1":
            montant = float(input("Montant à déposer : "))
            numero_compte = input("Numéro de compte bancaire : ")
            
            if numero_compte == compte1.numero_compte:
                compte1.deposer(montant)
                print(f"{montant}€ ont été déposés sur le compte {compte1.numero_compte}.")
            elif numero_compte == compte2.numero_compte:
                compte2.deposer(montant)
                print(f"{montant}€ ont été déposés sur le compte {compte2.numero_compte}.")
            else:
                print("Numéro de compte invalide.")

        elif choix == "2":
            montant = float(input("Montant à retirer : "))
            numero_compte = input("Numéro de compte bancaire : ")
            
            if numero_compte == compte1.numero_compte:
                compte1.retirer(montant)
                print(f"{montant}€ ont été retirés du compte {compte1.numero_compte}.")
            elif numero_compte == compte2.numero_compte:
                compte2.retirer(montant)
                print(f"{montant}€ ont été retirés du compte {compte2.numero_compte}.")
            else:
                print("Numéro de compte invalide.")

        elif choix == "3":
            montant = float(input("Montant à transférer : "))
            numero_compte_source = input("Numéro de compte bancaire source : ")
            numero_compte_destinataire = input("Numéro de compte bancaire destinataire : ")

            if numero_compte_source == compte1.numero_compte and numero_compte_destinataire == compte2.numero_compte:
                compte1.transferer(compte2, montant)
                print(f"{montant}€ ont été transférés du compte {compte1.numero_compte} au compte {compte2.numero_compte}.")
            elif numero_compte_source == compte2.numero_compte and numero_compte_destinataire == compte1.numero_compte:
                compte2.transferer(compte1, montant)
                print(f"{montant}€ ont été transférés du compte {compte2.numero_compte} au compte {compte1.numero_compte}.")
            else:
                print("Numéros de compte invalides.")

        elif choix == "4":
            print("Merci d'avoir utilisé notre système de gestion des comptes bancaires. Au revoir !")
            break

        else:
            print("Choix invalide. Veuillez sélectionner une option valide.")


if __name__ == "__main__":
    gestion_compte_bancaire()
```

#### Ajoutez le fichier `banque.py` au suivi de Git en utilisant la commande suivante 

```
$ git add .
```

La commande `git add .` est utilisée pour ajouter le fichier `banque.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

#### Création du commit pour la fonction `gestion_compte_bancaire` 

Créez un commit pour enregistrer la fonction `gestion_compte_bancaire` 

```
$ git commit -m "Ajout de la fonction gestion_compte_bancaire()"
```

La commande `git commit -m "Ajout de la fonction gestion_compte_bancaire()"` est utilisée pour créer un nouveau commit dans le dépôt Git. Un commit est une capture instantanée des modifications apportées aux fichiers suivis par Git.

Explication de la commande :

* `git commit` est la commande principale pour créer un commit.
* `-m "Ajout de la fonction gestion_compte_bancaire()"` est un paramètre qui permet de spécifier le message du commit. Le message doit être placé entre guillemets.

Une fois le commit créé, les modifications apportées aux fichiers sont enregistrées de manière permanente dans le dépôt Git. 

#### Afficher l'historique des commits et vérifier que votre commit a été enregistré avec succès

```
$ git log
```

La commande `git log` est utilisée pour afficher l'historique des commits dans le dépôt Git. Lorsque vous exécutez cette commande, Git affiche une liste des commits effectués, triés du plus récent au plus ancien.

#### Pousser le fichier banque.py vers la branche gestion_compte_bancaire_binome1

Pour pousser votre branche nommée "gestion_compte_bancaire_binome1" vers le dépôt distant nommé "origin" dans Git, vous pouvez utiliser la commande suivante :

```
git push origin gestion_compte_bancaire_binome1
```

Cette commande va pousser les commits de votre branche locale "gestion_compte_bancaire_binome1" vers la branche "gestion_compte_bancaire_binome1" du dépôt distant appelé "origin".

#### Accédez au référentiel distant sur [GitHub](https://github.com/) 

Cliquez sur le bouton "Compare & Pull Request" (demande de tirage) pour créer une nouvelle demande de tirage.

![image](https://github.com/kplr-training/Git-Github/assets/123757632/6f4597fe-dfc5-49c1-a9d3-35c08f1342f5)

Ajoutez une description pour votre demande de tirage et soumettez-la.

![image](https://github.com/kplr-training/Git-Github/assets/123757632/b61e53b8-3897-48da-95dc-c9f17c7d1606)

Votre collaborateur "binome1" peut maintenant examiner votre demande de tirage, ajouter des commentaires et demander des modifications supplémentaires si nécessaire.

### Binome 2

#### Fusionner et confirmer le pull request 

![image](https://github.com/kplr-training/Git-Github/assets/123757632/d82ea878-b68d-4edd-916f-d758a963a8db)

![image](https://github.com/kplr-training/Git-Github/assets/123757632/c745dc51-15b2-403b-b582-88014fe6ba10)

Pour fusionner le pull request cliquer sur Merge pull request puis Confirm merge

![image](https://github.com/kplr-training/Git-Github/assets/123757632/882fcdf7-dd68-4e0e-963b-b76af7ff77f4)

#### Verifier les commits dans votre repository 

![image](https://github.com/kplr-training/Git-Github/assets/123757632/8a3b5875-518b-48a2-a658-1cd52b327a38)

#### Basculer vers la branche principale 

La commande "git checkout main" est utilisée pour basculer vers la branche principale (ou branche maître) dans un référentiel Git. La branche principale est généralement utilisée pour représenter l'état stable du projet.

```
git checkout main
```

Lorsque vous exécutez cette commande, Git met à jour votre répertoire de travail pour refléter l'état de la branche principale. Cela signifie que les fichiers dans votre répertoire de travail seront modifiés pour correspondre à l'état de la branche "main". 


#### Récupérer les dernières modifications à partir d'un dépôt distant

La commande git pull est utilisée pour récupérer les dernières modifications à partir d'un dépôt distant (par exemple, un référentiel Git distant tel que GitHub) et les fusionner avec votre branche locale.

```
git pull 
```
