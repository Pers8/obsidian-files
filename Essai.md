**Question :** *Dans quelle mesure l'architecture des réseaux de neurones convolutifs ResNet est t-elle meilleure que l'architecture VGG16 en terme de performance et de précision dans la classification et reconnaissance des images ?*

***Table des matières :***
```markdown
1. Introduction 
2. Contexte Théorique
    1. Réseaux Neuronaux
    2. Apprentissage automatique
    3. Réseaux de neurones convolutifs
    4. Architectures ResNet et VGG16
3. Méthodologie Expérimentale
    1. Procédure expérimentale
    2. Datasets utlisés
    3. Configuration des modèles
4. Résultats Expérimentaux
    1. Table des résultats
    2. Graphes et interprétation
5. Analyse
    1. Mesure d'évaluation
    2. Analysse des résultats
    3. Réflexion sur l'expérience
6. Conclusion 
    1. Sythèse des découvertes
    2. Contraintes et limitations
    3. Conclusion
```

# 1. Introduction

L’intelligence artificielle (IA) a révolutionné de nombreux domaines de la science et de la technologie, et l’apprentissage automatique, en particulier l’apprentissage profond, est à l’avant-garde de cette révolution. Les réseaux de neurones convolutifs (CNN), avec leur capacité à apprendre des caractéristiques hiérarchiques à partir de données visuelles, ont transformé la classification et la reconnaissance d’images, rendant possible des applications allant de la détection de visages à la conduite autonome [1]. Parmi les architectures de CNN, ResNet et VGG16 se distinguent par leur influence et leurs performances. ResNet, acronyme de Residual Network, a été une percée majeure, introduisant des connexions résiduelles qui permettent aux signaux de contourner certaines couches du réseau, facilitant ainsi l’apprentissage de réseaux très profonds sans succomber au problème de disparition du gradient [2]. VGG16, quant à lui, est célèbre pour sa simplicité et son efficacité, ayant établi des records de performance sur le benchmark ImageNet, un ensemble de données de référence pour la classification d’images [3]. La question de savoir laquelle de ces architectures est supérieure en termes de performance et de précision est complexe et dépend de nombreux facteurs, y compris la nature des données, les ressources de calcul disponibles et les tâches spécifiques à accomplir. Des études comparatives ont montré que ResNet peut surpasser VGG16 dans certains contextes, offrant une meilleure précision avec une complexité calculatoire moindre. D’autres recherches suggèrent que les deux architectures ont leurs propres avantages et peuvent être choisies en fonction des exigences spécifiques du projet.
Dans cet essai, nous explorerons en profondeur les architectures ResNet et VGG16, en examinant leur conception, leur fonctionnement et leur efficacité dans divers scénarios de classification et de reconnaissance d’images. Nous analyserons les innovations clés qui permettent à ResNet de réaliser des performances impressionnantes et nous discuterons des avantages et des inconvénients de chaque architecture. Enfin, nous évaluerons **dans quelle mesure ResNet est effectivement supérieur à VGG16 en termes de performance et de précision**, en nous appuyant sur des études de cas et des benchmarks de l’industrie. Cette recherche vise non seulement à éclairer le débat sur la supériorité relative de ces architectures mais aussi à fournir des orientations pratiques pour les praticiens de l’IA qui cherchent à optimiser leurs systèmes de vision par ordinateur. En comprenant les forces et les faiblesses de ResNet et VGG16, nous pouvons mieux choisir les outils adaptés à nos besoins et continuer à repousser les frontières de ce que l’IA peut accomplir.

## 2. Contexte Théorique

### 2.1 Réseau neuronaux

Les réseaux de neurones (RN) sont un modèle d’apprentissage machine qui apprend à partir de données pour créer ou classifier des points de données. Ils sont composés de plusieurs couches de nœuds interconnectés (un nœud est pratiquement synonyme de neurone et de perception) qui propagent les données d’une couche d’entrée à une couche de sortie. Le modèle entier est représenté par une série d’opérations matricielles où les données de chaque couche sont d’abord additionnées, puis pondérées, puis ‘biaisées’, et enfin passées à travers une fonction d’activation. Ce processus, appelé processus de propagation avant, permet aux RN de réaliser des ‘décisions’ logiques complexes - par exemple, deux nœuds parallèles peuvent agir comme une opération logique XOR ou AND. Comme le comportement des nœuds peut être ajusté (appris), les RN peuvent trouver les motifs qui contribuent à une certaine classification.

Chaque connexion entre les nœuds se voit attribuer une valeur de poids. Cette valeur correspond à l’importance accordée à l’information transitant entre les nœuds connectés. Si le poids est élevé, le nœud est plus affecté par l’activation - qui représente l’information - du nœud connecté. À partir de la couche d’entrée, les entrées sont multipliées par les poids et sont sommées. Cela se fait par un produit scalaire, de sorte que nous n’avons pas à traiter chaque nœud individuellement. L’information de chaque nœud est stockée sous forme d’éléments à l’intérieur de matrices - au lieu d’avoir des vecteurs de poids séparés pour chaque nœud, nous les regroupons dans une matrice. Chaque nœud a également un biais. Puisque les nœuds sont censés représenter des neurones, le biais est relatif à la facilité avec laquelle un neurone peut s’activer ; en ajoutant un biais à la somme pondérée, nous obtenons une probabilité plus élevée que la fonction d’activation ‘s’active’. La fonction d’activation est une représentation mathématique du potentiel d’action d’un neurone. Si la somme pondérée + biais est suffisamment grande, la fonction d’activation ‘s’active’ - s’active.

Comme la couche de sortie est également composée de nœuds, chaque nœud peut être assigné pour représenter une classe différente. Lorsqu’un vecteur de données est entré dans le réseau, les données se propagent à travers le réseau et arrivent finalement à la couche de sortie où le nœud représentant une classe correcte s’active. Si plusieurs nœuds s’activent ou si le nœud correct ne s’active pas du tout, le RN utilise le gradient négatif de la fonction d’erreur (choisie dans le cadre de l’architecture) pour ajuster les variables internes (ceci est fait pendant la période d’entraînement) - les poids et les biais décrits ci-dessus. Ma fonction d’erreur choisie fonctionne en trouvant la différence entre la sortie optimale et la sortie réelle (puis en sommant et en mettant au carré la différence). C’est pourquoi un RN est un modèle d’apprentissage machine.

Pour illustrer ces concepts, considérons un exemple simple de réseau de neurones avec une couche d’entrée, une couche cachée et une couche de sortie. Supposons que nous ayons un ensemble de données d’images étiquetées comme ‘chat’ ou ‘chien’. Notre objectif est de construire un RN capable de classifier correctement les images inédites en tant que ‘chat’ ou ‘chien’.

**1. Couche d’entrée :** Chaque image est convertie en un vecteur de valeurs de pixels, qui constitue notre couche d’entrée.

**2. Couche cachée :** Les valeurs de la couche d’entrée sont multipliées par une matrice de poids et additionnées à un vecteur de biais. La somme pondérée est ensuite passée à travers une fonction d’activation, telle que la fonction ReLU, qui introduit de la non-linéarité dans le modèle.

**3. Couche de sortie :** La sortie de la couche cachée est à nouveau multipliée par une matrice de poids et additionnée à un biais, puis passée à travers une fonction d’activation softmax, qui convertit les valeurs en probabilités pour chaque classe (‘chat’ ou ‘chien’).

**4. Entraînement :** Pendant l’entraînement, le RN ajuste les poids et les biais pour minimiser l’erreur entre les prédictions et les étiquettes réelles. Cela se fait généralement par rétropropagation et descente de gradient.

**5. Prédiction :** Une fois entraîné, le RN peut prendre une nouvelle image, la propager à travers le réseau et produire une prédiction de classe basée sur la sortie de la couche de sortie.

Pour visualiser ces opérations, nous pouvons utiliser des graphes qui montrent la propagation des données à travers le réseau et des matrices pour représenter les poids et les biais. Par exemple, un graphe pourrait montrer les valeurs d’activation à chaque couche pour une image donnée, tandis qu’une matrice de poids pourrait être représentée comme suit :
$$
\begin{bmatrix} 
w_{11} & w_{12} & \cdots & w_{1n}
\ w_{21} & w_{22} & \cdots & w_{2n} \ \vdots & \vdots & \ddots & \vdots \ w_{m1} & w_{m2} & \cdots & w_{mn} \end{bmatrix}$$

où ( $W$ ) est la matrice de poids, ( $w_{ij}$ ) est le poids entre le i-ème nœud de la couche précédente et le j-ème nœud de la couche actuelle, ( $m$ ) est le nombre de nœuds dans la couche précédente, et ( $n$ ) est le nombre de nœds dans la couche actuelle.

Ces concepts sont essentiels pour comprendre comment les architectures de RN telles que ResNet et VGG16 fonctionnent et comment elles peuvent être utilisées pour la classification et la reconnaissance d’images avec une grande précision et performance. En analysant les opérations matricielles et les fonctions d’activation, nous pouvons saisir la complexité et la puissance de ces modèles d’apprentissage profond.

### 2.3 Réseaux Neuronaux 

L’un des principaux cas d’usage des CNN est la reconnaissance d’image. Les réseaux convolutifs apprennent plus rapidement et ont un meilleur taux d’erreur . Dans une moindre mesure, on les utilise aussi pour l’analyse vidéo. Ce type de réseau est aussi utilisé pour le traitement naturel du langage. Les modèles CNN sont très efficaces pour l’analyse sémantique, la modélisation de phrase, la classification ou la traduction.

La classification d’images a connu une avancée majeure en termes de performance, grâce à l’essor des réseaux de neurones convolutifs. De la classification d’images, au transfert de style, en passant par la détection d’objets, les applications au sein des entreprises se multiplient. Les CNN peuvent apprendre à reconnaître des motifs et des caractéristiques dans les images grâce à l’utilisation de couches de convolution, qui appliquent un ensemble de filtres aux données d’entrée pour détecter des motifs spécifiques.



Références :

1 - [The Future of AI: How AI Is Changing the World | Built In](https://builtin.com/artificial-intelligence/artificial-intelligence-future)

2 - [ResNet Architecture and Its Variants: An Overview | Built In](https://builtin.com/artificial-intelligence/resnet-architecture)

3 - [Understanding VGG16: Concepts, Architecture, and Performance (datagen.tech)](https://datagen.tech/guides/computer-vision/vgg16/)







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


Neural networks (NNs) are a type of machine learning model that learns from data to either create or classify data points. NNs are made up of several layers of interconnected nodes (node is practically synonymous with neuron and perception) that propagate data from an input layer to an output layer. The whole model is represented by a series of matrix operations (1) where the data at each layer is first summed, then weighed, then ’biased’, and then passed through an activation function. This process is called the feedforward process and allows NNs to carry out complicated logical ’decisions’ - for example, two parallel nodes can act as a XOR or an AND logical operation. Because the behavior of nodes can be adjusted (learned), NNs 6 can find the patterns that contribute to a certain classification. Each connection between nodes is assigned a weight value. This weight value corresponds to how much ’weight’ is placed on the information going between the connected nodes. If the weight is high, the node is more affected by the firing - which represents the information - of the connected node. Starting from the input layer, the inputs are multiplied by the weights and are summed. This is done through a dot product, so we don’t have to deal with each node individually. Each node’s information is stored as elements inside of matrices - instead of having separate vectors of weights for each node, we put them together into a matrix. Each node also has a bias. Since nodes are supposed to represent neurons, the bias is relative to how much easier it is for a neuron to fire; by adding a bias to the weighed sum, we get a higher probability of the activation function ’firing’. The activation function is a mathematical representation of the action potential of a neuron. If the weighed sum + bias is large enough, the activation function ’fires’ - activates. Because the output layer is also made up of nodes, each node can be assigned to represent a different class. When the network is inputted a data vector, the data propagates through the network and eventually arrives at the output layer where the node representing a correct class fires. If several nodes fire or if the correct node doesn’t fire at all, the NN uses the negative gradient of the error (chosen as part of the architecture) function to then adjust the inner variables (this is done during the training period) - the weights and biases described above. My chosen error function works by finding the difference between the optimal output and the real output (and then summing and squaring the difference). This is why a NN is a machine learning model.




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










