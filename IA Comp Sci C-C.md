# Criterion A

### Scenario/Solution

Mon client est un freelancer professionnel basé aux Philippines. Il opère à l'échelle internationale, collaborant principalement avec les meilleurs développeurs Roblox des États-Unis. L'un des défis majeurs qu'il rencontre dans son travail est le délai de réponse. Cela est principalement dû aux différences substantielles de fuseaux horaires entre lui et ses clients. Ce problème a été un obstacle à la fourniture d'un service efficace, ce qui l'a amené à m'engager pour automatiser son site web, dans le but de résoudre ce problème et d'améliorer ses opérations commerciales.

La solution dont nous avons discuté implique la création d'un site web automatisé. Ce site n'est pas seulement un outil qui lui permettra de gagner du temps, mais aussi une plateforme qui lui permettra de toucher davantage de clients grâce à son design attrayant. Le site web servira de portfolio numérique où il pourra présenter son travail. Il permettra également aux clients de passer des commandes en fonction de leurs besoins spécifiques, tels que les icônes, les vignettes, etc. De plus, le site web permettra aux clients de gérer directement leurs commandes. Cette fonction sera accessible à la fois sur le site web et via Discord, offrant flexibilité et commodité aux clients. Le site web comprendra également un système de connexion sécurisé. Ce système lui permettra de mettre à jour son portfolio, d'ajouter de nouvelles offres et même de proposer des réductions à ses clients. Cette solution globale vise à améliorer sa prestation de services et, en fin de compte, à améliorer l'expérience globale du client. En réglant le problème du fuseau horaire et en fournissant une plateforme d'interaction transparente, le site web devrait propulser son nombre de commandes vers de nouveaux sommets.

### Rationale

J'ai choisi d'utiliser HTML, CSS et JavaScript pour la solution car ces technologies sont indépendantes de la plate-forme, ce qui signifie qu'il n'y aurait aucune restriction quant au type d'appareil utilisé par mon client ou ses clients. De plus, en stylisant le site web, on le rendra plus esthétique et plus simple à utiliser pour mon client et ses clients. J'ai choisi d'utiliser Visual Studio Code comme éditeur de code parce qu'il prend en charge ces technologies de manière native et offre une interface moderne et conviviale.

Mon client a mentionné qu'elle avait utilisé d'autres plateformes en ligne pour présenter son travail et gérer les commandes, mais que pour que ces plateformes offrent la personnalisation et l'accès hors ligne, elle devait passer à un abonnement payant. Elle souhaitait donc disposer d'une alternative appropriée qui réponde à ses besoins et fonctionne hors ligne, d'où la nécessité d'un site web personnalisé. Le site web aidera la cliente à présenter son travail, à gérer les commandes et à proposer des réductions, tout en améliorant l'expérience globale de l'utilisateur.

### Success Criteria

1. L'utilisateur peut voir les prix et tous mes travaux sur un seul site web.
2. Le site est automatisé et lié à un serveur Discord.
3. Les commandes peuvent être gérées et créées directement à partir du site web.
4. L'utilisateur peut facilement commander plusieurs articles à la fois.

# Criterion B

(In progress)





**FLOWCHART 1 - LOGIN** : Click on the login button, Redirect the user to the OAuth2 URL, which will prompt them to authorize your application and grant the requested permissions such having accept to the user's profile picture and username, If the user's discord ID correspond to an admin's user discord id then the user who's an admin can add new works (Images from their work in the portfolio page) directly to assigned topic, should be able to add game link + visit count from the website. They can add discounts that will adjust prices automatically. They will be able to see all current orders and able to see past order logs. If it's not an admin, the user will be able to create an order which he couldn't be he wasn't log in. 
**FLOWCHART 2 - ORDER** : If you aren't log in and you try to click the "Order Here" button, it will notify the user by saying "You need to log in in order to create an order.". If you are log in you can create an order in the order page. When you click the order button in the order page, it will redirect you to the TOS section. When you finish reading the TOS section, you can click back and it will bring you to the previous section which is the main order page. If you click the next button, it will bring you to the Fill form section where you can choose what do you want (Icon, Gamepass, Vector and Thumbnail) with the price when you hover, The references and details you want and you can attach an image for more precision, The payment type (Robux or Paypal) and the preferred deadline. When you finish filling the Fill form section, you can click back and it will bring you to the previous section which is the TOS section. If you click the next button, it will bring you to the Final price section. In that section, depending on what you chose on the Fill section it will display it as the title (If I chose 1 item which is "Icon" for example when it asks what do you want, it will display as the title of the Final price section). If you selected multiple elements when it asks what do you want in the fill form section, it will display all the one you selected with a margin and each item is a flexbox. When you selected something in the Final price section, under the title it will ask for the style (Cartoony, Rendered, Anime, Custom) and below it will ask if the user wants Fast Delivery. If yes he can click the checkbox and it will add 10 000 Robux/35 USD to the final price, if he doesn't click nothing happens and it will not add 10 000 Robux/35 USD to the final price. Below he can check the checkbox if he wants the PSD (photoshop) file to be included and don't check if you don't want it to be included. Below it there will be the final price of that the user will pay. When you finish checking the Final prie section, you can click back and it will bring you to the previous section which is the Fill Form section. If you click the next button, it will bring the user to a the final section. It will says that the order proceed if everything was filled and it will display the discord server where you can join and directly talk to my Client about the order. If everything is not filled and checked, it will ask you to fill everything. **Don't forget that you will only use words and a group of words for the flowchart**

## Record of tasks
| Task number | Planned action | Planned outcome | Time estimate | Target completion date | Criterion |
| ----------- | -------------- | --------------- | ------------- | ---------------------- | --------- |
| 1           |                |                 |               |                        |           |
| 2           |                |                 |               |                        |           |



## Tableau des cas de test

| Actions à tester                                    | Méthode d'essai                                                                                                                                                                                                                                                           | Résultat attendu                                                                                                                 | Critères de réussite                                                                                                                                |
| --------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| Cliquer sur le bouton de connexion                  | Vérifier que le bouton est visible et cliquable                                                                                                                                                                                                                           | Vous êtes redirigé vers l'URL OAuth2                                                                                             | Le code de réponse HTTP est 200                                                                                                                     |
| Autoriser l'application et accordez les permissions | Suiver les instructions à l'écran et entrez vos identifiants discord                                                                                                                                                                                                      | Vous êtes redirigé vers le site web avec votre profil affiché                                                                    | Le code de réponse HTTP est 200 et votre ID discord est affiché                                                                                     |
| Vérifier votre statut d'administrateur              | Comparer votre ID discord avec la liste des administrateurs                                                                                                                                                                                                               | Vous avez accès aux fonctionnalités réservées aux administrateurs si votre ID discord correspond, ou pas si ce n'est pas le cas  | Les boutons "Ajouter un travail", "Ajouter un lien de jeu", "Ajouter une réduction" et "Voir les commandes" sont visibles ou pas selon votre statut |
| Cliquer sur le bouton "Commander ici"               | Vérifier que le bouton est visible et cliquable                                                                                                                                                                                                                           | Vous êtes redirigé vers la section CGU si vous êtes connecté, ou vous voyez un message d'erreur si vous ne l'êtes pas            | Le code de réponse HTTP est 200 et la section CGU ou le message d'erreur sont affichés                                                              |
| Liser les CGU                                       | Faire défiler le texte et cliquez sur le bouton "J'accepte"                                                                                                                                                                                                               | Vous revenez à la section précédente                                                                                             | Le code de réponse HTTP est 200 et la section précédente est affichée                                                                               |
| Cliquer sur le bouton suivant                       | Vérifier que le bouton est visible et cliquable                                                                                                                                                                                                                           | Vous êtes redirigé vers la section formulaire                                                                                    | Le code de réponse HTTP est 200 et la section formulaire est affichée                                                                               |
| Remplir le formulaire                               | Choisisser ce que vous voulez parmi les options proposées (Icon, Gamepass, Vector, Thumbnail), entrez les références et les détails que vous voulez, joignez une image si vous le souhaitez, choisissez le type de paiement (Robux ou Paypal) et la date limite souhaitée | Vous revenez à la section précédente                                                                                             | Le code de réponse HTTP est 200 et la section précédente est affichée                                                                               |
| Cliquer sur le bouton suivant                       | Vérifier que le bouton est visible et cliquable                                                                                                                                                                                                                           | Vous êtes redirigé vers la section prix final                                                                                    | Le code de réponse HTTP est 200 et la section prix final est affichée                                                                               |
| Vérifier le prix final                              | Vérifier que le prix final correspond à ce que vous avez choisi dans le formulaire, avec les éventuels frais supplémentaires pour la livraison rapide et le fichier PSD                                                                                                   | Vous revenez à la section précédente                                                                                             | Le code de réponse HTTP est 200 et la section précédente est affichée                                                                               |
| Cliquer sur le bouton suivant                       | Vérifier que le bouton est visible et cliquable                                                                                                                                                                                                                           | Vous êtes redirigé vers la section confirmation                                                                                  | Le code de réponse HTTP est 200 et la section confirmation est affichée                                                                             |
| Confirmer votre commande                            | Cliquer sur le bouton "Confirmer" si vous êtes satisfait de votre commande, ou sur le bouton "Annuler" si vous voulez la modifier ou l'annuler                                                                                                                            | Vous voyez un message de confirmation ou d'annulation de votre commande, et vous êtes redirigé vers le serveur discord du client | Le code de réponse HTTP est 200 et le message de confirmation ou d'annulation et le serveur discord sont affichés                                   |
|                                                     |                                                                                                                                                                                                                                                                           |                                                                                                                                  |                                                                                                                                                     |


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

Mots : 