# Critère C : Développement 


## 1. Dépendances du Projet

**Backend**

| Dépendance   | Fonction                                                                                                     |
| ------------ | ------------------------------------------------------------------------------------------------------------ |
| `sqlite3`    | Utilisé pour interagir avec la base de données SQLite                                                        |
| `express`    | Framework de serveur web pour Node.js, gère les requêtes HTTP                                                |
| `cors`       | Middleware pour Express qui active les requêtes cross-origin                                                 |
| `dotenv`     | Charge les variables d'environnement à partir d'un fichier `.env`                                            |
| `discord.js` | Bibliothèque permettant d'interagir avec l'API de Discord                                                    |
| `node.js`    | Environnement d'exécution JavaScript côté serveur qui permet de construire le backend de mon application web |


**Frontend**

| Dépendance              | Fonction                                                                                                                   |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| `HTML5`                 | Langage de base pour la structure de la page web.                                                                          |
| `CSS3`                  | Utilisé pour styliser et présenter le contenu HTML.                                                                        |
| `JavaScript`            | Langage de script pour créer du contenu interactif.                                                                        |
| `jQuery`                | Bibliothèque JavaScript pour simplifier le HTML traversing, event handling, et l'animation.                                |
| `Font Awesome`          | Kit d'icônes et d'outils pour l'interface utilisateur.                                                                     |
| `SwiperJS`              | Bibliothèque tactile pour créer des sliders (carrousels) modernes et mobiles.                                              |
| `Lightbox`              | Plugin pour afficher des images et des vidéos en pleine taille.                                                            |
| `VanillaTilt.js`        | Bibliothèque JavaScript pour des effets de parallaxe en 3D.                                                                |
| `Waypoints + CounterUp` | Plugins jQuery pour déclencher une fonction lorsqu'on défile jusqu'à un élément et pour animer l'augmentation des nombres. |

## 2. Techniques de Développement Employées

### 2.1. Interface Graphique Utilisateur (GUI)

J'ai utilisé JavaScript pour créer une application basée sur le web pour la création et la gestion de commandes. Je récupère les entrées de l'utilisateur à partir de différents éléments de formulaire ci-dessous et les compile dans un format structuré pour l'envoyer sur Discord. 

![[site.png]]
![[code 1.png]]

Dans ce code, j'ai utilisé `addEventListener()` pour gérer les actions des utilisateurs telles que cliquer sur le bouton "Suivant" pour poursuivre le processus de création de commande. L'application collecte dynamiquement les données du formulaire, y compris les options sélectionnées, les détails de référence et le type de paiement, entre autres.

La complexité de l'interface graphique est encore démontrée par l'intégration de services tiers, tels qu'imgbb pour les téléchargements d'images, qui améliorent la capacité de l'utilisateur à fournir des spécifications de commande détaillées. J'ai utilisé la nature asynchrone de JavaScript, associée à l'API fetch, pour faciliter une communication fluide avec des services externes, sans jamais interrompre l'expérience utilisateur.
![[code 2.png]]

### 2.2. Héritage

 J'ai utilisé le concept d'héritage à travers la création et l'utilisation d'une classe nommée `OrderManager`. Cette classe est conçue pour gérer diverses opérations liées aux commandes, telles que la création, la mise à jour et la récupération des commandes d'une base de données SQLite.
 ![[code 3.png]]
 La classe `OrderManager` n'hérite pas d'une autre classe en utilisant le mot-clé `extends`, qui est couramment utilisé dans JavaScript pour un héritage de type classique. Cependant, le concept d'héritage est implicitement présent à travers la composition de l'instance `sqlite3.Database` passée au constructeur de `OrderManager`. Cette composition permet à `OrderManager` d'utiliser la connexion à la base de données et ses méthodes, "héritant" effectivement de ses capacités sans étendre directement une classe parente.

### 2.3. Structures de Données Complexes

 J'ai utilisé SQLite comme système de gestion de base de données pour stocker et gérer les données de manière structurée et efficace. SQLite est une bibliothèque logicielle qui fournit un système de base de données relationnelle accessible sans nécessiter un serveur de base de données distinct. Cette approche me permet de créer une base de données légère et autonome, idéale pour les applications de petite à moyenne taille comme la mienne.

Pour initialiser la base de données et établir la connexion, j'ai utilisé le code suivant :
![[code 4.png]]

Ici, j'ai importé le module `sqlite3` et créé une nouvelle instance de la base de données SQLite en spécifiant le chemin du fichier de base de données. L'option `verbose()` est utilisée pour obtenir des messages de journalisation détaillés, ce qui est utile pour le débogage.

Ensuite, j'ai structuré la base de données en créant trois tables principales : `users`, `channels`, et `orders`. Chaque table est conçue pour stocker des types spécifiques de données et est définie comme suit :
![[code 5.png]]

La table des utilisateurs (`users`) ci-dessus stocke les informations sur les utilisateurs. Chaque utilisateur est identifié par un `userId` (Leur `userId` Discord) unique.
![[code 6.png]]

La table des canaux Discord (`channels`) ci-dessus conserve les détails des canaux Discord. Chaque canal est identifié par un `channelId` unique.
![[code 7.png]]

La table des commandes (`orders`) ci-dessus enregistre les détails des commandes passées par les utilisateurs dans les différents canaux. Cette table utilise une clé primaire auto-incrémentée `id` pour identifier chaque commande de manière unique. Elle contient également des clés étrangères référençant les `userId` et `channelId` pour lier les commandes aux utilisateurs et aux canaux appropriés. 

### 2.4. Débogage 

 J'ai utilisé plusieurs techniques pour identifier et corriger les erreurs dans mon code, notamment pour gérer les messages d'erreur comme `errorMessage`.
  ![[code 8.png]]
 J'ai utilisé une structure `try...catch` pour gérer les erreurs potentielles lors de l'envoi des données de commande au serveur. Si la requête échoue pour une raison quelconque (par exemple, le serveur ne répond pas ou renvoie une erreur), le bloc `catch` est exécuté. J'affiche alors un message d'erreur à l'utilisateur en modifiant la propriété `style.display` de l'élément `errorMessage` pour le rendre visible. Cela informe l'utilisateur qu'une erreur s'est produite lors de la création de la commande comme nous pouvons le voir ci-dessous.
 ![[Pasted image 20240401151311.png]]
### 2.5. Validation des Données 

 J'ai limité les types de fichiers acceptés à des images, comme indiqué dans l'attribut `accept` de l'élément d'entrée de fichier.
 ![[code 9.png]]
 J'ai utilisé des validations côté client pour s'assurer que les utilisateurs remplissent correctement le formulaire avant de soumettre leur commande. Par exemple, j'ai vérifié si l'utilisateur a sélectionné au moins une option et rempli tous les champs nécessaires.
 ![[code 10.png]]
 
### 2.6. Intégration avec des Systèmes Externes (Discord)

L'intégration avec Discord a été réalisée grâce à la bibliothèque `discord.js`. Cette bibliothèque me permet de créer et de gérer un bot Discord, qui peut interagir avec les utilisateurs sur un serveur Discord. J'ai créé l'instance `Client` qui permet au bot d'écouter et de répondre à des messages dans les serveurs Discord.
![[code 11.png]]

## 3. Pensée Computationnelle

###  3.1. Abstraction et Encapsulation

Pour l'abstraction, j'ai défini la classe `OrderManager` qui encapsule toute la logique liée à la gestion des commandes dans l'application. Cette classe offre des méthodes publiques comme `createOrder`, `updateOrderStatus`, et `fetchOrder`, permettant d'interagir avec la base de données sans exposer les détails de l'implémentation SQL dans le code de la section **Héritage**. L'encapsulation est mise en œuvre à travers l'utilisation de propriétés et de méthodes privées au sein de ces classes. En encapsulant les détails de l'implémentation, j'ai pu modifier l'implémentation interne sans affecter les parties du code qui utilisent ces classes, facilitant ainsi la maintenance et l'évolution du projet.

### 3.2. Algorithmes de Conversion et Traitement des Données

J'ai utilisé plusieurs techniques pour manipuler et convertir les données de manière efficace tel qu'un algorithme pour traiter les données saisies par l'utilisateur et les préparer pour une insertion dans la base de données via une API.

![[code 12.png]]

Pour le traitement des images téléchargées, j'ai utilisé une boucle `for` pour parcourir chaque fichier sélectionné par l'utilisateur, puis j'ai envoyé ces fichiers à un service externe (imgbb) pour le stockage des images. 
![[code 13.png]]

### 3.3. Sécurité et Confidentialité des Données

J'ai utilisé le package `dotenv` pour charger les variables d'environnement à partir d'un fichier `.env`. Cela me permet de stocker des informations sensibles, telles que le token du bot Discord (`process.env.BOT_TOKEN`), en dehors du code source. Cela réduit le risque d'exposer des données sensibles et facilite la configuration de l'application dans différents environnements.
![[code 14.png]]

Pour la communication entre le client et le serveur, j'utilise le protocole HTTPS (non illustré dans les extraits de code fournis) pour chiffrer les données échangées, protégeant ainsi les informations sensibles des utilisateurs lors de leur transmission sur Internet.

### 3.3. Pensée logique

J'ai utilisé SQLite et la pensée logique pour structurer une requête préparée pour insérer une nouvelle commande dans la table `orders`, en utilisant l'identifiant de l'utilisateur et les détails de la commande fournis. L'utilisation de `datetime('now')` pour le champ `orderDate` permet d'enregistrer automatiquement la date et l'heure de la création de la commande, assurant ainsi la traçabilité des commandes.
![[code 15.png]]


**Mots :** 1008 


## Références