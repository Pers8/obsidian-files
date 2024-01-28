**Question :** *Dans quelle mesure l'architecture des réseaux de neurones convolutifs ResNet est t-elle meilleure que l'architecture VGG16 en terme de performance et de précision dans la classification et reconnaissance des images ?*

***Table des matières :***
```markdown
1. Introduction 
2. Contexte Théorique
    1. Réseaux Neuronaux
    2. Réseaux de neurones convolutifs
    3. Architectures ResNet et VGG16
3. Méthodologie Expérimentale
    1. Procédure expérimentale
    2. Datasets utlisés
    3. Configuration des modèles
4. Résultats Expérimentaux
    1. Table des résultats
    2. Graphes des résultats
5. Analyse et conclusion
	1. Mesure d'évaluation
	2. Analyse des résultats
	3. Contraintes et limitations
	4. Conclusion
```

# 1. Introduction

L’intelligence artificielle (IA) a révolutionné de nombreux domaines de la science et de la technologie, et l’apprentissage automatique, en particulier l’apprentissage profond, est à l’avant-garde de cette révolution. Les réseaux de neurones convolutifs (CNN), avec leur capacité à apprendre des caractéristiques hiérarchiques à partir de données visuelles, ont transformé la classification et la reconnaissance d’images, rendant possible des applications allant de la détection de visages à la conduite autonome [1]. Parmi les architectures de CNN, ResNet et VGG16 se distinguent par leur influence et leurs performances. ResNet, acronyme de Residual Network, a été une percée majeure, introduisant des connexions résiduelles qui permettent aux signaux de contourner certaines couches du réseau, facilitant ainsi l’apprentissage de réseaux très profonds sans succomber au problème de disparition du gradient [2]. VGG16, quant à lui, est célèbre pour sa simplicité et son efficacité, ayant établi des records de performance sur le benchmark ImageNet, un ensemble de données de référence pour la classification d’images [3]. La question de savoir laquelle de ces architectures est supérieure en termes de performance et de précision est complexe et dépend de nombreux facteurs, y compris la nature des données, les ressources de calcul disponibles et les tâches spécifiques à accomplir. Des études comparatives ont montré que ResNet peut surpasser VGG16 dans certains contextes, offrant une meilleure précision avec une complexité calculatoire moindre. D’autres recherches suggèrent que les deux architectures ont leurs propres avantages et peuvent être choisies en fonction des exigences spécifiques du projet.
Dans cet essai, nous explorerons en profondeur les architectures ResNet et VGG16, en examinant leur conception, leur fonctionnement et leur efficacité dans divers scénarios de classification et de reconnaissance d’images. Nous analyserons les innovations clés qui permettent à ResNet de réaliser des performances impressionnantes et nous discuterons des avantages et des inconvénients de chaque architecture. Enfin, nous évaluerons **dans quelle mesure ResNet est effectivement supérieur à VGG16 en termes de performance et de précision**, en nous appuyant sur des études de cas et des benchmarks de l’industrie. Cette recherche vise non seulement à éclairer le débat sur la supériorité relative de ces architectures mais aussi à fournir des orientations pratiques pour les praticiens de l’IA qui cherchent à optimiser leurs systèmes de vision par ordinateur. En comprenant les forces et les faiblesses de ResNet et VGG16, nous pouvons mieux choisir les outils adaptés à nos besoins et continuer à repousser les frontières de ce que l’IA peut accomplir.

## 2. Contexte Théorique

### 2.1 Réseau neuronaux

Les réseaux neuronaux (NN) sont des modèles d’apprentissage automatique qui s’inspirent du fonctionnement du cerveau humain pour traiter des informations et apprendre à partir de données. Ils sont constitués de plusieurs couches de nœuds interconnectés, qui propagent les données d’une couche d’entrée à une couche de sortie. Chaque nœud, ou neurone artificiel, est connecté à chaque nœud de la couche suivante, et chaque connexion entre les nœuds se voit attribuer une valeur de poids. Ces poids déterminent l’importance relative de l’information transmise entre les nœuds connectés. Dans un NN, les données d’entrée sont multipliées par les poids et sont sommées. Cette somme pondérée est ensuite ajustée par un biais, qui est relatif à la facilité avec laquelle un neurone peut être activé. La somme pondérée plus le biais est ensuite passée à travers une fonction d’activation, qui est une représentation mathématique du potentiel d’action d’un neurone. Si la somme pondérée plus le biais est suffisamment grande, la fonction d’activation s’active, ce qui entraîne l’activation du nœud et la transmission des données à la couche suivante. La couche de sortie d’un NN est également composée de nœuds, et chaque nœud peut être assigné pour représenter une classe différente. Lorsqu’un vecteur de données est introduit dans le réseau, les données se propagent à travers le réseau et arrivent finalement à la couche de sortie, où le nœud représentant la classe correcte s’active. Si plusieurs nœuds s’activent ou si le bon nœud ne s’active pas du tout, le NN utilise le gradient négatif de la fonction d’erreur pour ajuster les variables internes, telles que les poids et les biais, pendant la période d’entraînement.

### 2.3 Réseaux de Neuronaux Convolutifs

Les réseaux de neurones convolutifs (CNN) sont une classe de modèles d’apprentissage profond qui ont révolutionné la vision par ordinateur et l’analyse d’images. Ces réseaux imitent le traitement de l’information visuelle du cerveau humain et sont particulièrement efficaces pour la reconnaissance automatique de motifs complexes dans les données visuelles, ce qui les rend idéaux pour la classification et la reconnaissance d’images. Un CNN est structuré en plusieurs couches qui transforment progressivement l’image d’entrée en une représentation de plus en plus abstraite. 

![[Img 1.png]]
La première couche, la couche convolutive, applique des filtres ou des noyaux à l’image pour détecter des caractéristiques telles que les bords ou les textures. Ces filtres sont des matrices de poids qui se déplacent sur l’image et effectuent une opération de convolution, qui est un produit scalaire entre le filtre et une région locale de l’image. Par exemple, un filtre conçu pour détecter les bords verticaux pourrait ressembler à la matrice suivante :

$$F = \begin{bmatrix} 1 & 0 & -1 \\ 1 & 0 & -1 \\ 1 & 0 & -1 \end{bmatrix}$$

Ce filtre, lorsqu’il est appliqué à l’image, produit une carte des caractéristiques qui met en évidence les régions où les bords verticaux sont présents. Après la convolution, les cartes des caractéristiques passent souvent par une opération de pooling, qui réduit leur dimensionnalité tout en préservant les caractéristiques les plus importantes. Le max pooling, qui sélectionne la valeur maximale d’une région de la carte des caractéristiques, est une forme courante de pooling.
Au fur et à mesure que l’image traverse les différentes couches du CNN, elle est transformée en une représentation de plus en plus abstraite. Les premières couches peuvent détecter des caractéristiques simples comme les bords et les textures, tandis que les couches plus profondes reconnaissent des motifs plus complexes.
Les CNN sont entraînés en utilisant un ensemble de données d’images étiquetées. Pendant l’entraînement, les poids des filtres sont ajustés pour minimiser une fonction de perte, qui mesure l’erreur entre les prédictions du réseau et les étiquettes réelles. Les algorithmes de descente de gradient, tels que l’algorithme de descente de gradient stochastique (SGD), sont utilisés pour optimiser ces poids. Pendant l’entraînement, les filtres apprennent à reconnaître des caractéristiques qui sont importantes pour la tâche de classification.
Pour visualiser le processus d’apprentissage, on peut utiliser des graphiques qui montrent la diminution de la fonction de perte au fil des époques d’entraînement. 

![[Line-plot-of-Mean-Squared-Error-Loss-over-Training-Epochs-When-Optimizing-the-Mean-Squared-Error-Loss-Function-768x576.png]]
**FIG. 2. Tracé de la perte d'erreur quadratique moyenne sur les périodes d'entraînement lors de l'optimisation de la fonction de perte d'erreur quadratique moyenne** [4]

Ces graphiques aident à comprendre comment le réseau s’améliore au fil du temps et devient meilleur pour prédire les étiquettes correctes des images. Les CNN ont de nombreuses applications dans divers domaines allant de la reconnaissance faciale à l’analyse d’images médicales. Ils sont également utilisés dans des systèmes de recommandation, la segmentation d’images, et le traitement du langage naturel. La capacité des CNN à apprendre des caractéristiques à partir de données brutes et à s’adapter pour améliorer la précision les rend inestimables pour les tâches de vision par ordinateur.


Références :

1 - [The Future of AI: How AI Is Changing the World | Built In](https://builtin.com/artificial-intelligence/artificial-intelligence-future)

2 - [ResNet Architecture and Its Variants: An Overview | Built In](https://builtin.com/artificial-intelligence/resnet-architecture)

3 - [Understanding VGG16: Concepts, Architecture, and Performance (datagen.tech)](https://datagen.tech/guides/computer-vision/vgg16/)
4 - [How to Choose Loss Functions When Training Deep Learning Neural Networks - MachineLearningMastery.com](https://machinelearningmastery.com/how-to-choose-loss-functions-when-training-deep-learning-neural-networks/)
5 - [What are Neural Networks? | IBM](https://www.ibm.com/topics/neural-networks)




$$
\begin{bmatrix}
w_1 & w_2 & w_3 & w_4\\
w_1 & w_2 & w_3 & w_4\\
w_1 & w_2 & w_3 & w_4
\end{bmatrix}
\begin{bmatrix}
x_1 \\
x_2 \\
x_3 \\
x_4
\end{bmatrix}
+
\begin{bmatrix}
b \\
b \\
b 
\end{bmatrix}
=
\begin{bmatrix}
w_1x_1 + w_2x_2 + w_3x_3 + w_4x_4 + b \\
w_1x_1 + w_2x_2 + w_3x_3 + w_4x_4 + b \\
w_1x_1 + w_2x_2 + w_3x_3 + w_4x_4 + b
\end{bmatrix}_{activation}
\rightarrow
\begin{bmatrix}
a_1 \\
a_2 \\
a_3
\end{bmatrix}
$$




---

$$\LARGE IA$$

# Critère A

## Problème

Le client, un artiste freelance basé aux Philippines, travaille principalement avec des développeurs Roblox de premier plan aux États-Unis. En raison de la nature internationale de son travail, il est confronté à des problèmes de délai de réponse dus aux différences de fuseaux horaires, ce qui l’empêche de répondre rapidement à la plupart de ses clients. Cela a motivé le client à engager un développeur pour construire et automatiser son site web.

Ce site web ne sera pas seulement un gain de temps, mais il servira également de vitrine pour son portefeuille d’œuvres d’art, augmentant ainsi ses chances d’obtenir plus de commandes. Le design attrayant du site est censé attirer de nouveaux clients, ce qui contribuera à élargir la présence du client sur le marché international.

Le site web vise à fournir une plateforme où les clients potentiels peuvent immédiatement voir le talent et la créativité du client, leur permettant de passer des commandes à tout moment, indépendamment des contraintes de temps. En fin de compte, ce site web représente une opportunité pour le client de connecter son art avec un public plus large, tout en gérant efficacement les communications et les transactions avec ses clients existants et futurs.


## Rationale

Continuant sur l’introduction fournie, nous allons approfondir notre compréhension des réseaux neuronaux et leur rôle crucial dans les architectures de CNN telles que ResNet et VGG16. Les réseaux neuronaux sont des modèles computationnels qui imitent le fonctionnement du cerveau humain pour traiter des données et reconnaître des motifs complexes, ce qui est essentiel dans la classification et la reconnaissance d’images.

**Réseaux Neuronaux et Traitement de l’Information**

Les réseaux neuronaux sont composés de couches de neurones interconnectés qui transforment les données d’entrée en sorties significatives. Chaque neurone calcule une somme pondérée de ses entrées et applique une fonction d’activation pour générer une sortie. Par exemple, si nous avons un vecteur d’entrée ( \mathbf{x} ) et un vecteur de poids ( \mathbf{w} ), la sortie ( y ) d’un neurone est donnée par: $y = f\left(\sum_{i}(w_i \cdot x_i) + b\right)$ où ( f ) est la fonction d’activation et ( b ) est le biais.

**Apprentissage et Optimisation**

L’apprentissage dans les réseaux neuronaux se fait par l’ajustement des poids synaptiques pour minimiser une fonction de perte, qui mesure l’écart entre les prédictions du réseau et les valeurs réelles. La rétropropagation est une méthode courante pour mettre à jour les poids, où l’erreur est propagée à travers le réseau pour ajuster les poids de manière à réduire l’erreur lors des futures prédictions.

**Fonctions d’Activation**

Les fonctions d’activation introduisent des non-linéarités dans le réseau, permettant de capturer des relations complexes entre les données. Des exemples courants incluent la fonction ReLU, définie par ( $f(x) = \max(0, x)$ ), et la fonction sigmoïde, ( $f(x) = \frac{1}{1 + e^{-x}}$ ).

**Réseaux de Neurones Convolutifs (CNN)**

Les CNN sont spécialement conçus pour traiter des données structurées comme les images. Ils utilisent des filtres convolutifs pour extraire des caractéristiques spatiales et des opérations de pooling pour réduire la dimensionnalité des données, tout en préservant les caractéristiques importantes.

**Architectures ResNet et VGG16**

ResNet se distingue par ses connexions résiduelles qui permettent de former des réseaux très profonds sans le problème de disparition du gradient. VGG16, avec ses couches convolutives empilées, est reconnu pour sa simplicité et son efficacité.

**Performance et Précision**

La performance et la précision des CNN dépendent de leur architecture et de leur capacité à apprendre des caractéristiques pertinentes. ResNet, grâce à ses connexions résiduelles, peut souvent atteindre une meilleure précision que VGG16, en particulier dans les tâches de classification d’images complexes.

**Visualisation et Compréhension**

Les graphiques de la fonction de perte et les matrices de confusion sont des outils essentiels pour évaluer la performance des réseaux neuronaux. Les graphiques de la fonction de perte montrent comment l’erreur diminue au fil de l’apprentissage, tandis que les matrices de confusion révèlent la précision de la classification.

En conclusion, les réseaux neuronaux sont au cœur des avancées dans la classification et la reconnaissance d’images. Les architectures comme ResNet et VGG16 montrent comment des conceptions innovantes peuvent améliorer la performance et la précision, ce qui est crucial pour les applications pratiques de l’IA.

[Pour une exploration plus approfondie des réseaux neuronaux et des architectures CNN, je vous recommande de consulter les ressources suivantes](https://www.ibm.com/fr-fr/topics/neural-networks)[1](https://www.ibm.com/fr-fr/topics/neural-networks)[2](https://fr.wikipedia.org/wiki/R%C3%A9seau_de_neurones_artificiels)[3](https://datascientest.com/fonctionnement-des-reseaux-neurones). Ces sources fournissent des informations détaillées sur le fonctionnement et l’optimisation des réseaux neuronaux, ainsi que sur les spécificités des architectures ResNet et VGG16.










L’intelligence artificielle (IA) a révolutionné de nombreux domaines de la science et de la technologie, et l’apprentissage automatique, en particulier l’apprentissage profond, est à l’avant-garde de cette révolution. Les réseaux de neurones convolutifs (CNN), avec leur capacité à apprendre des caractéristiques hiérarchiques à partir de données visuelles, ont transformé la classification et la reconnaissance d’images, rendant possible des applications allant de la détection de visages à la conduite autonome. Parmi les architectures de CNN, ResNet et VGG16 se distinguent par leur influence et leurs performances. ResNet, acronyme de Residual Network, a été une percée majeure, introduisant des connexions résiduelles qui permettent aux signaux de contourner certaines couches du réseau, facilitant ainsi l’apprentissage de réseaux très profonds sans succomber au problème de disparition du gradient. VGG16, quant à lui, est célèbre pour sa simplicité et son efficacité, ayant établi des records de performance sur le benchmark ImageNet, un ensemble de données de référence pour la classification d’images. La question de savoir laquelle de ces architectures est supérieure en termes de performance et de précision est complexe et dépend de nombreux facteurs, y compris la nature des données, les ressources de calcul disponibles et les tâches spécifiques à accomplir. Des études comparatives ont montré que ResNet peut surpasser VGG16 dans certains contextes, offrant une meilleure précision avec une complexité calculatoire moindre. D’autres recherches suggèrent que les deux architectures ont leurs propres avantages et peuvent être choisies en fonction des exigences spécifiques du projet. 
Dans cet essai, nous explorerons en profondeur les architectures ResNet et VGG16, en examinant leur conception, leur fonctionnement et leur efficacité dans divers scénarios de classification et de reconnaissance d’images. Nous analyserons les innovations clés qui permettent à ResNet de réaliser des performances impressionnantes et nous discuterons des avantages et des inconvénients de chaque architecture. Enfin, nous évaluerons \dans quelle mesure ResNet est effectivement supérieur à VGG16 en termes de performance et de précision, en nous appuyant sur des études de cas et des benchmarks de l’industrie. Cette recherche vise non seulement à éclairer le débat sur la supériorité relative de ces architectures mais aussi à fournir des orientations pratiques pour les praticiens de l’IA qui cherchent à optimiser leurs systèmes de vision par ordinateur. En comprenant les forces et les faiblesses de ResNet et VGG16, nous pouvons mieux choisir les outils adaptés à nos besoins et continuer à repousser les frontières de ce que l’IA peut accomplir.

Les réseaux neuronaux (NN) sont des modèles d’apprentissage automatique qui s’inspirent du fonctionnement du cerveau humain pour traiter des informations et apprendre à partir de données. Ils sont constitués de plusieurs couches de nœuds interconnectés, qui propagent les données d’une couche d’entrée à une couche de sortie comme nous pouvons le voir dans la Figure 1. Chaque nœud, ou neurone artificiel, est connecté à chaque nœud de la couche suivante, et chaque connexion entre les nœuds se voit attribuer une valeur de poids. Ces poids déterminent l’importance relative de l’information transmise entre les nœuds connectés. Dans un NN, les données d’entrée sont multipliées par les poids et sont sommées. Cette somme pondérée est ensuite ajustée par un biais, qui est relatif à la facilité avec laquelle un neurone peut être activé. La somme pondérée plus le biais est ensuite passée à travers une fonction d’activation, qui est une représentation mathématique du potentiel d’action d’un neurone. Si la somme pondérée plus le biais est suffisamment grande, la fonction d’activation s’active, ce qui entraîne l’activation du nœud et la transmission des données à la couche suivante. La couche de sortie d’un NN est également composée de nœuds, et chaque nœud peut être assigné pour représenter une classe différente. Lorsqu’un vecteur de données est introduit dans le réseau, les données se propagent à travers le réseau et arrivent finalement à la couche de sortie, où le nœud représentant la classe correcte s’active. Si plusieurs nœuds s’activent ou si le bon nœud ne s’active pas du tout, le NN utilise le gradient négatif de la fonction d’erreur pour ajuster les variables internes, telles que les poids et les biais, pendant la période d’entraînement.

Les réseaux de neurones convolutifs (CNN) sont une classe de modèles d’apprentissage profond qui ont révolutionné la vision par ordinateur et l’analyse d’images. Ces réseaux imitent le traitement de l’information visuelle du cerveau humain et sont particulièrement efficaces pour la reconnaissance automatique de motifs complexes dans les données visuelles, ce qui les rend idéaux pour la classification et la reconnaissance d’images. Un CNN est structuré en plusieurs couches qui transforment progressivement l’image d’entrée en une représentation de plus en plus abstraite. La première couche, la couche convolutive, applique des filtres ou des noyaux à l’image pour détecter des caractéristiques telles que les bords ou les textures. Ces filtres sont des matrices de poids qui se déplacent sur l’image et effectuent une opération de convolution, qui est un produit scalaire entre le filtre et une région locale de l’image. Par exemple, un filtre conçu pour détecter les bords verticaux pourrait ressembler à la matrice suivante :
Ce filtre, lorsqu’il est appliqué à l’image, produit une carte des caractéristiques qui met en évidence les régions où les bords verticaux sont présents. Après la convolution, les cartes des caractéristiques passent souvent par une opération de pooling, qui réduit leur dimensionnalité tout en préservant les caractéristiques les plus importantes. Le max pooling, qui sélectionne la valeur maximale d’une région de la carte des caractéristiques, est une forme courante de pooling.
Au fur et à mesure que l’image traverse les différentes couches du CNN, elle est transformée en une représentation de plus en plus abstraite. Les premières couches peuvent détecter des caractéristiques simples comme les bords et les textures, tandis que les couches plus profondes reconnaissent des motifs plus complexes.
Les CNN sont entraînés en utilisant un ensemble de données d’images étiquetées. Pendant l’entraînement, les poids des filtres sont ajustés pour minimiser une fonction de perte, qui mesure l’erreur entre les prédictions du réseau et les étiquettes réelles. Les algorithmes de descente de gradient, tels que l’algorithme de descente de gradient stochastique (SGD), sont utilisés pour optimiser ces poids. Pendant l’entraînement, les filtres apprennent à reconnaître des caractéristiques qui sont importantes pour la tâche de classification.
Pour visualiser le processus d’apprentissage, on peut utiliser des graphiques qui montrent la diminution de la fonction de perte au fil des époques d’entraînement. Ces graphiques aident à comprendre comment le réseau s’améliore au fil du temps et devient meilleur pour prédire les étiquettes correctes des images. Les CNN ont de nombreuses applications dans divers domaines allant de la reconnaissance faciale à l’analyse d’images médicales. Ils sont également utilisés dans des systèmes de recommandation, la segmentation d’images, et le traitement du langage naturel. La capacité des CNN à apprendre des caractéristiques à partir de données brutes et à s’adapter pour améliorer la précision les rend inestimables pour les tâches de vision par ordinateur.

L’essor de l’apprentissage profond en vision par ordinateur a été marqué par le développement de diverses architectures de réseaux de neurones convolutifs (CNN), parmi lesquelles ResNet et VGG16 se distinguent par leur innovation et performance. Ces architectures ont été conçues pour améliorer la précision de la classification et de la reconnaissance d'images, répondant ainsi aux exigences croissantes de diverses applications pratiques.

ResNet, acronyme de Residual Network, a été présenté par Microsoft Research en 2015 et a remporté le challenge ImageNet cette même année. Sa contribution majeure réside dans l’introduction de connexions résiduelles, permettant de contourner une ou plusieurs couches. Ces connexions aident à résoudre le problème de la disparition du gradient, un obstacle majeur dans l'entraînement de réseaux profonds. En conséquence, ResNet peut efficacement être formé avec un nombre beaucoup plus élevé de couches, allant jusqu’à 152 dans certaines versions, tout en maintenant une consommation de ressources gérable. Cette profondeur accrue permet une extraction de caractéristiques plus raffinée, se traduisant par une amélioration notable de la précision dans la classification d'images.

VGG16 a été introduit par l’équipe de recherche de Visual Graphics Group de l’Université d'Oxford en 2014. Cette architecture se caractérise par sa simplicité, utilisant une série de couches convolutives avec des filtres de petite taille (3x3) suivies d’une fonction d’activation ReLU. La régularité de cette structure permet une augmentation progressive de la profondeur du réseau, favorisant l’extraction de caractéristiques visuelles complexes. VGG16, comportant 16 couches, a démontré des performances remarquables sur plusieurs benchmarks, notamment sur le dataset ImageNet. Cependant, malgré son efficacité, VGG16 souffre de sa grande consommation de ressources computationnelles et de sa tendance à l'overfitting avec des datasets limités.

Sélection des Datasets : Choisir des ensembles de données standards pour la classification d'images en utilisant CIFAR-10 qui offrent une variété de catégories et de complexités d'images.
Prétraitement des Données : Normaliser les images (réglage de la taille, normalisation des couleurs) pour garantir des conditions de test cohérentes pour les deux architectures.
Configuration des Modèles : Configurer les architectures ResNet et VGG16 avec des paramètres initiaux standards. S'assurer d'utiliser la même initialisation pour les deux modèles pour garantir une comparaison équitable.
Entraînement des Modèles : Entraîner les deux architectures sur le dataset sélectionné.
Optimisation des Hyperparamètres : Ajuster les hyperparamètres tels que le taux d'apprentissage, le nombre de couches (dans le cas de ResNet), etc., pour optimiser les performances de chaque modèle.
Mesures de Performance : Évaluer les modèles en utilisant des métriques standard telles que la précision, la matrice de confusion, le rappel, et le score F1. Effectuez également une analyse des erreurs pour comprendre dans quelles conditions chaque modèle excelle ou échoue.
Comparaison des Résultats : Comparer les performances des deux architectures en termes de précision de classification, vitesse d'entraînement, et efficacité en ressources (comme la consommation de mémoire et de temps de calcul).
Discussion sur l'Architecture : Analyser comment les différences structurelles entre ResNet et VGG16 affectent leur performance. Par exemple, examiner l'impact des connexions résiduelles de ResNet sur la capacité du modèle à apprendre des caractéristiques profondes.
Applications Pratiques : Discuter des implications pratiques des résultats, comme le choix de l'architecture en fonction du type de tâche de classification d'images, des ressources disponibles, et des exigences en termes de précision.





	
You can use intersection types to limit the possible types of a generic type like for example if you have a type union Enforced = number | Vector2 | Vector3 you can use T & Enforce to mean that T must be one of those types and this way you can write a generic function that only accepts arguments of the same type and that type must be either number, Vector2, or Vector3