# Critère B : Design‎
## 1. Visualisation graphique

Les images ci-dessus illustrent le design de l'interface que j'avais en tête avant la conception du site web.
### 1.1. La page "Home"
<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\Comp sci IA img/Home.png" alt="Home" style="width:1000px;"/>
</div>

### 1.2. La page "Portfolio"
<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\Comp sci IA img/Portfolio.png" alt="Home" style="width:1000px;"/>
</div>

### 1.3. La page "Order"
<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\Comp sci IA img/Order 1.png" alt="Home" style="width:1000px;"/>
</div>
<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\Comp sci IA img/Order 2.png" alt="Home" style="width:1000px;"/>
</div>
<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\Comp sci IA img/Order 3.png" alt="Home" style="width:1000px;"/>
</div>
<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\Comp sci IA img/Order 4.png" alt="Home" style="width:1000px;"/>
</div>
<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\Comp sci IA img/Order 4.png" alt="Home" style="width:1000px;"/>
</div>
<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\Comp sci IA img/Order 5.png" alt="Home" style="width:1000px;"/>
</div>

### 1.4. La page "Cartoony GFX Course"
<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\Comp sci IA img/Cartoony GFX Course.png" alt="Home" style="width:1000px;"/>
</div>

## 2. Diagramme hiérarchique

Ce diagramme illustre comment les différentes pages du site et leurs éléments sont liés.

<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\CS code/Diagramme hiérarchique-2024-04-01-223718.svg" alt="Home" style="width:1000px;"/>
</div>


## 3. Diagramme de flux de données

Ce diagramme met en évidence le flux de données qui circule lorsque l'utilisateur interagi avec les différentes pages de mon site. Je l'ai montré avec à mon client pour qu'il ait une idée du fonctionnement interne de mon site web.

<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\CS code/Diagramme de flux de données-2024-04-01-224353.svg" alt="Home" style="width:500px;"/>
</div>


## 4. Organigrammes

### 4.1. Processus de commande

Cet organigramme met en évidence le processus lorsque l'utilisateur souhaite créer une commande à travers le site web. Cela décrit les différentes étapes à suivre pour la création de commande.

<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\CS code/1. Processus de commande-2024-04-02-093626.svg" alt="Home" style="width:500px;"/>
</div>

### 4.2. Authentification Discord

L'organigramme ci-dessous met en lumière le procédé d'authentification lorsque l'utilisateur clique le bouton "Login". Cela décrit comment l'authentification est effectuée pour récupérer les différentes informations de l'utilisateur afin d'afficher ces informations Discord (photo de profil, pseudonyme et bannière Discord) lorsque la connexion est réussie.

<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\CS code/2. Authentification Discord-2024-04-01-213644.svg" alt="Home" style="width:500px;"/>
</div>

### 4.3. Filtre pour le Portfolio

Cet organigramme illustre le procédé lorsque l'utilisateur veut filtrer les différents travaux par type (Miniature, Icône, Passe de jeu, etc.). Cela décrit les étapes que l'utilisateur doit suivre pour filtrer les travaux afin d'afficher seulement le type désiré.

<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\CS code/3. Filtre pour le Portfolio-2024-04-01-213705.svg" alt="Home" style="width:230px;"/>
</div>

### 4.4. Récupération et affichage du profil de l'utilisateur

L'organigramme ci-dessous illustre comment les informations de l'utilisateur sont récupérées et ainsi identifie si l'utilisateur est un administrateur ou pas, dans le but de lui ajouter une icône spéciale qui sera juste à côté du nom de l'utilisateur.

<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\CS code/4. Récupération et affichage du profil de l'utilisateur-2024-04-01-213927.svg" alt="Home" style="width:450px;"/>
</div>


## 5. Diagramme Entité-Relation

Le diagramme Entité-Relation ci-dessous illustre ma réflexion sur les différentes connexions entre les tables lorsque que la base de donnée sera créé pour le processus de commande. `PK` fait référence à la clé primaire et `FK` la clé étrangère. Référez au dictionnaire de données pour une description des tables.

<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\CS code/ERD.svg" alt="Home" style="width:500px;"/>
</div>

# 6. Dictionnaire de données

Vous trouverez ci-dessous toutes les informations sur les tables individuelles qui composeront la base de données SQLite que je vais créer.

#### Table `users`

Cette table contient des informations sur les utilisateurs. Chaque enregistrement représente un utilisateur unique identifié par un `userId`. C'est la clé primaire de la table.

| Nom du champ | Type de données | Contraintes  | Description                                |
| ------------ | --------------- | ------------ | ------------------------------------------ |
| `userId`     | TEXT            | CLÉ PRIMAIRE | Identifiant unique pour chaque utilisateur |

#### Table `channels`

Cette table stocke des informations sur les chaines Discord. Chaque enregistrement est identifié de manière unique par un `channelId`, qui sert de clé primaire.

| Nom du champ | Type de données | Contraintes  | Description                         |
| ------------ | --------------- | ------------ | ----------------------------------- |
| `channelId`  | TEXT            | CLÉ PRIMAIRE | Identifiant unique pour les chaines |

#### Table `orders`

La table `orders` contient des détails sur les commandes passées par les utilisateurs. Elle inclut un `id` unique pour chaque commande, `userId` pour lier à la table `users`, `channelId` pour lier à la table `channels`, `orderDetails` contenant les spécificités de la commande, `status` indiquant l'état actuel de la commande (avec une valeur par défaut de 'Pending'), et `orderDate` marquant quand la commande a été faite.

| Nom du champ   | Type de données | Contraintes                                 | Description                              |
| -------------- | --------------- | ------------------------------------------- | ---------------------------------------- |
| `id`           | INTEGER         | CLÉ PRIMAIRE AUTOINCREMENT                  | Identifiant unique pour les commandes    |
| `userId`       | TEXT            | CLÉ ÉTRANGÈRE RÉFÉRENCE users(userId)       | Identifiant liant à la table `users`     |
| `channelId`    | TEXT            | CLÉ ÉTRANGÈRE RÉFÉRENCE channels(channelId) | Identifiant liant à la table `channels`  |
| `orderDetails` | TEXT            |                                             | Détails de la commande                   |
| `status`       | TEXT            | DÉFAUT 'Pending'                            | Statut actuel de la commande             |
| `orderDate`    | TEXT            |                                             | Date à laquelle la commande a été passée |

# 7. Plan de Test 

| Critères de succès | Description du test                                                                                                           | Méthode de test                                                                                                                                           | Résultat attendu                                                                                                                                                          |
| ------------------ | ----------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1                  | Vérifier que le site web affiche tous les services disponibles avec leurs prix et présente le portfolio des travaux réalisés. | Naviguer sur le site web jusqu'aux sections affichant les prix et les travaux passés.                                                                     | Tous les services proposés sont listés avec une tarification claire. La section portfolio affiche tous les travaux antérieurs.                                            |
| 2                  | Tester l'intégration entre le site web et le serveur Discord pour des notifications ou actions automatisées.                  | Effectuer une action sur le site web qui devrait déclencher une notification ou une action sur le serveur Discord (par exemple, soumettre un formulaire). | Le serveur Discord reçoit la notification ou effectue l'action comme prévu, indiquant une intégration réussie.                                                            |
| 3                  | S'assurer que les utilisateurs peuvent passer des commandes via le site web et que ces commandes sont correctement traitées.  | Passer une commande sur le site web, en remplissant toutes les informations nécessaires et en la soumettant.                                              | La commande est créée avec succès et reflétée dans le système backend ou la base de données, et une confirmation est affichée ou envoyée à l'utilisateur.                 |
| 4                  | Tester la fonctionnalité du site web pour gérer les commandes de plusieurs articles en une seule transaction.                 | Ajouter plusieurs articles à un panier ou à un formulaire de commande sur le site web et soumettre la commande.                                           | Le site web traite correctement la commande, incluant tous les articles. Un résumé ou une confirmation montrant tous les articles commandés est présenté à l'utilisateur. |

**Mots :** 388