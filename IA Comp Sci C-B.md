# Critère B : Design 


## 1. Visualisation graphique

### 1.1. La page "Home"
<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\Comp sci IA img/Home.png" alt="Home" style="width:1000px;"/>
</div>
### 1.2. La page "Portfolio"
<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\Comp sci IA img/Portfolio.png" alt="Home" style="width:1000px;"/>
</div>
### 1.3. La page "Orders"
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
<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\CS code/Diagramme hiérarchique-2024-04-01-223718.svg" alt="Home" style="width:1000px;"/>
</div>

## 3. Diagramme de flux de données
<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\CS code/Diagramme de flux de données-2024-04-01-224353.svg" alt="Home" style="width:1000px;"/>
</div>

## 4. Organigrammes
### 4.1. Processus de commande

<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\CS code/1. Processus de commande-2024-04-01-213617.svg" alt="Home" style="width:1000px;"/>
</div>
### 4.2. Processus de commande
<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\CS code/2. Authentification Discord-2024-04-01-213644.svg" alt="Home" style="width:1000px;"/>
</div>
### 4.3. Processus de commande
<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\CS code/3. Filtre pour le Portfolio-2024-04-01-213705.svg" alt="Home" style="width:1000px;"/>
</div>
### 4.4. Processus de commande
<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\CS code/4. Récupération et affichage du profil de l'utilisateur-2024-04-01-213927.svg" alt="Home" style="width:1000px;"/>
</div>

## 5. Diagramme UML
<div style="text-align: center; margin-top: 20px;">
    <img src="C:\Users\peres\OneDrive\Images\CS code/UML Diagram.svg" alt="Home" style="width:1000px;"/>
</div>


# 6. Plan de Test 

| Critères de succès                                                               | Description du test                                                                                                           | Méthode de test                                                                                                                                           | Résultat attendu                                                                                                                                                          |
| -------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. L'utilisateur peut voir les prix et tous mes travaux sur un seul site web.    | Vérifier que le site web affiche tous les services disponibles avec leurs prix et présente le portfolio des travaux réalisés. | Naviguer sur le site web jusqu'aux sections affichant les prix et les travaux passés.                                                                     | Tous les services proposés sont listés avec une tarification claire. La section portfolio affiche tous les travaux antérieurs.                                            |
| 2. Le site est automatisé et lié à un serveur Discord.                           | Tester l'intégration entre le site web et le serveur Discord pour des notifications ou actions automatisées.                  | Effectuer une action sur le site web qui devrait déclencher une notification ou une action sur le serveur Discord (par exemple, soumettre un formulaire). | Le serveur Discord reçoit la notification ou effectue l'action comme prévu, indiquant une intégration réussie.                                                            |
| 3. Les commandes peuvent être gérées et créées directement à partir du site web. | S'assurer que les utilisateurs peuvent passer des commandes via le site web et que ces commandes sont correctement traitées.  | Passer une commande sur le site web, en remplissant toutes les informations nécessaires et en la soumettant.                                              | La commande est créée avec succès et reflétée dans le système backend ou la base de données, et une confirmation est affichée ou envoyée à l'utilisateur.                 |
| 4. L'utilisateur peut facilement commander plusieurs articles à la fois.         | Tester la fonctionnalité du site web pour gérer les commandes de plusieurs articles en une seule transaction.                 | Ajouter plusieurs articles à un panier ou à un formulaire de commande sur le site web et soumettre la commande.                                           | Le site web traite correctement la commande, incluant tous les articles. Un résumé ou une confirmation montrant tous les articles commandés est présenté à l'utilisateur. |
