
**Question :** Comment la vitesse influence-t-elle la portance d’une aile d’avion ?
# ***Table des matières***
<br>
1-

```markdown
1. Introduction
2. Question de recherche 
3. Contexte théorique et Hypothèse
5. Variables
6. Diagramme
7. Apparatus
8. Méthodologie
9. Risques liés à l'expérience
10. Collecte et traitement des données
	10.1. Données brutes
	10.2. Données traités
11. Graphiques
12. Collection des données et Analyse (Pas pris en compte)
	8.1. Tableau des données
	8.2. Table des données 
	8.3. Traitement des données 
	8.4. Incertitudes
	8.5. Analyse des données
	8.6. Analyse des erreurs
9. Analyse et Conclusion
10. Evaluation
11. Références
```

<br>
La portance est la force qui permet à un avion de s’élever dans l’air grâce à la forme de ses ailes. Elle s’oppose au poids de l’avion et dépend de plusieurs facteurs, dont la vitesse du vent relatif, la densité de l’air, l’angle d’attaque de l’aile, la surface alaire et le coefficient de portance. La portance peut être calculée par la formule suivante :
<br>

$$P=\frac{1}{2}\rho V^2SC_L$$
<br>
Où $P$ est la portance, $\rho$ est la densité de l’air, $V$ est la vitesse du vent relatif, $S$ est la surface alaire et $C_L$ est le coefficient de portance. Le coefficient de portance dépend de la forme du profil de l’aile et de l’angle d’attaque. Il atteint une valeur maximale avant le décrochage de l’aile, qui correspond à la perte de portance due au décollement des filets d’air sur l’extrados.
<br>
Pour étudier l’influence de la vitesse sur la portance, je peux réaliser une expérience en utilisant une voiture et un anémomètre. Je peux fixer une aile d’avion miniature sur un support et la placer dans le flux d’air généré par la soufflerie ou par le déplacement de la voiture. Je peux mesurer la vitesse du vent relatif avec un anémomètre et la portance avec un dynamomètre. Je peux faire varier la vitesse du vent relatif en modifiant la vitesse de la soufflerie ou de la voiture, et enregistrer les valeurs de portance correspondantes. Je peux tracer un graphique de la portance en fonction de la vitesse et vérifier si la relation est linéaire ou non. Je peux aussi calculer le coefficient de portance à partir de la formule et le comparer avec les valeurs théoriques données par les courbes de polarisation des profils d’aile.
<br>
Si je n'ai pas la possibilité de faire une expérience réelle, je peux aussi utiliser une simulation numérique pour modéliser le comportement de l’aile dans l’air. Il existe des logiciels gratuits qui me permettent de créer ton propre profil d’aile, de choisir les paramètres de l’écoulement et de visualiser les forces de portance et de traînée. Par exemple, tu peux utiliser le logiciel XFLR5, qui est basé sur la méthode des panneaux et la théorie de la ligne portante.



Profil d'aile, angle de décrochage (angle où il n'a presque plus de portance)


# Introduction 

La fascination pour le vol et l'ingénierie aéronautique a été le moteur de mon intérêt pour la physique, un champ d'étude qui explique de manière captivante les phénomènes naturels et technologiques. Ce choix de sujet pour mon exploration dans le programme IB de physique découle de cette passion pour l'aviation, combinée à un désir de comprendre les principes scientifiques qui la rendent possible. Cette étude est particulièrement importante car elle incorpore des concepts de mécanique des fluides et de dynamique, et illustre l'application de la physique dans des situations concrètes. En se concentrant sur l'effet de la vitesse sur la portance, cette recherche répond non seulement à une question pratique critique en aéronautique, mais elle met également en lumière l'application des lois de la physique dans des contextes réels, enrichissant ma compréhension de la matière et son rapport au monde technologique. La question que j'ai choisie d'explorer est : “Comment la vitesse influence-t-elle la portance d’une aile d’avion ?”, avec un focus particulier sur un modèle simplifié : un avion en papier. Cette question se concentre sur l'interaction entre la vitesse et la portance, deux facteurs fondamentaux en aéronautique. Mon hypothèse, adaptée à mon modèle d'avion en papier, est que l'augmentation de la vitesse de l'avion en papier, estimée à l'aide d'un chronomètre, augmentera également la portance. Cette hypothèse se base sur une compréhension élémentaire des principes de la dynamique des fluides et du principe de Bernoulli, suggérant qu'une vitesse accrue de l'air autour de l'avion en papier diminuera la pression sur le dessus de l'aile, augmentant ainsi la portance.
Pour examiner cette hypothèse, j'utiliserai un avion en papier comme modèle d'étude, avec la vitesse de l'avion en papier comme variable indépendante et la portance comme variable dépendante. La vitesse sera mesurée en lançant l'avion en papier dans des conditions contrôlées et en utilisant un chronomètre pour estimer sa vitesse. Cette méthode simple, mais efficace, permettra d'établir un lien direct entre la vitesse de l'avion en papier et la portance qu'il génère, offrant ainsi une compréhension approfondie de la dynamique de vol dans un cadre expérimental accessible.


+ trainée en fonction de $v_{air}$
+ portance en fonction de $v$
protocole de l'expérience : penser à une simulation



## Démarche pour le simulation

- Téléchargez et installez Physion sur votre ordinateur à partir du site officiel.
- Ouvrez le logiciel et cliquez sur le bouton "Nouveau" pour créer un nouveau projet.
- Dans le menu "Options", choisissez "Propriétés du monde" et réglez les paramètres du fluide, comme la masse volumique et la viscosité. Par exemple, vous pouvez choisir une masse volumique de 1.225 kg/m^3^ et une viscosité de 1.81e-5 Pa.s pour simuler l'air à 15°C.
- Dans le menu "Objets", choisissez "Polygone" et dessinez le contour de l'aile d'avion sur le plan de travail. Vous pouvez utiliser la grille et le zoom pour ajuster la taille et la forme de l'aile. Par exemple, vous pouvez choisir un profil NACA 0012, qui est un profil symétrique couramment utilisé en aérodynamique.
- Cliquez sur le bouton "Sélectionner" et sélectionnez l'aile. Dans le menu "Propriétés", réglez les propriétés de l'aile, comme la masse, le coefficient de restitution, le coefficient de frottement, etc. Par exemple, vous pouvez choisir une masse de 1 kg, un coefficient de restitution de 0.5, et un coefficient de frottement de 0.1.
- Dans le menu "Contraintes", choisissez "Ressort" et reliez l'aile à un point fixe sur le plan de travail. Ce ressort va permettre de faire varier l'angle d'incidence de l'aile en fonction de la force exercée par le fluide. Dans le menu "Propriétés", réglez les propriétés du ressort, comme la longueur, la constante, l'amortissement, etc. Par exemple, vous pouvez choisir une longueur de 0.5 m, une constante de 100 N/m, et un amortissement de 10 N.s/m.
- Dans le menu "Forces", choisissez "Force constante" et appliquez une force horizontale à l'aile. Cette force va représenter la vitesse du vent relatif. Dans le menu "Propriétés", réglez l'intensité et la direction de la force. Par exemple, vous pouvez choisir une intensité de 10 N et une direction de 0°.
- Cliquez sur le bouton "Démarrer" pour lancer la simulation. Vous pouvez observer le mouvement de l'aile, la déformation du ressort, et la valeur de la force constante. Vous pouvez aussi cliquer sur le bouton "Pause" pour arrêter la simulation, et sur le bouton "Réinitialiser" pour recommencer la simulation.
- Pour visualiser la portance et la traînée de l'aile, vous pouvez utiliser le menu "Mesures" et choisir "Force". Cliquez sur l'aile et déplacez le curseur pour afficher la résultante aérodynamique, la portance, et la traînée. Vous pouvez aussi cliquer sur le bouton "Graphique" pour tracer la courbe de ces forces en fonction du temps.
- Pour visualiser les champs de pression et de vitesse autour de l'aile, vous pouvez utiliser le menu "Affichage" et choisir "Champ de pression" ou "Champ de vitesse". Vous pouvez aussi régler la résolution et la couleur du champ dans le menu "Propriétés".
- Pour exporter les données de la simulation, vous pouvez utiliser le menu "Fichier" et choisir "Exporter les données". Vous pouvez choisir le format et le nom du fichier, et les données seront sauvegardées sur votre ordinateur.


(1) Portance d'une aile - L'avionnaire. https://www.lavionnaire.fr/AerodynPortance.php.
(2) L'aile dans un flux d'air - L'avionnaire. https://www.lavionnaire.fr/AerodynFluxAile.php.
(3) Déterminer portance d'un drone par le calcul. https://forumdrone.fr/topic/636-d%C3%A9terminer-portance-dun-drone-par-le-calcul/.
(4) Simulation d'un profil d'une aile d'avion by meriem borgi - Prezi. https://prezi.com/jzfurvyqwfum/simulation-dun-profil-dune-aile-davion/.

## Contexte théorique

La portance est la force qui permet à un avion de voler. Elle s’exerce perpendiculairement à la direction du vent relatif, c’est-à-dire la vitesse de l’air par rapport à l’aile. La portance dépend de plusieurs facteurs, dont la forme du profil de l’aile, l’angle d’incidence, la vitesse du vent relatif, la densité de l’air, et la rugosité de la surface de l’aile. Dans cette exploration, nous allons nous intéresser à l’influence de la vitesse sur la portance d’une aile d’avion, en utilisant une simulation numérique.

Pour comprendre comment la portance se crée, il faut d’abord connaître le principe de conservation de la quantité de mouvement. Ce principe stipule que la somme des quantités de mouvement d’un système isolé reste constante, sauf s’il y a une force extérieure qui agit sur le système. La quantité de mouvement d’un corps est le produit de sa masse par sa vitesse. Par exemple, si un corps de masse $m$ se déplace à la vitesse $v$, sa quantité de mouvement est $p = mv$. Si le corps change de vitesse, sa quantité de mouvement change aussi, et il faut qu’il y ait une force qui provoque ce changement. La force est égale à la variation de la quantité de mouvement par unité de temps, c’est-à-dire $F = \frac{dp}{dt}$. 

Quand une aile d’avion se déplace dans l’air, elle modifie la vitesse et la direction de l’air qui la traverse. L’air qui passe au-dessus de l’aile (l’extrados) accélère et prend une direction plus basse que l’air qui passe en dessous de l’aile (l’intrados). L’air qui quitte l’aile a donc une quantité de mouvement différente de l’air qui arrive sur l’aile. Il y a donc une variation de la quantité de mouvement de l’air, et donc une force qui s’exerce sur l’air. D’après la troisième loi de Newton, il y a aussi une force égale et opposée qui s’exerce sur l’aile. Cette force est la portance.

Une relation entre la portance et la différence de pression entre l’extrados et l’intrados de l’aile existe à partir de la relation suivante : la portance est égale au produit de la différence de pression par la surface de l’aile, c’est-à-dire $L = (p_{\text{inf}} - p_{\text{sup}})S$, où $L$ est la portance, $p_{\text{inf}}$​ est la pression sur l’intrados, $p_{\text{sup}}$ est la pression sur l’extrados, et $S$ est la surface de l’aile. La pression est la force exercée par unité de surface. Quand l’air accélère, sa pression diminue, et inversement. L’air qui passe au-dessus de l’aile a donc une pression plus faible que l’air qui passe en dessous de l’aile. La différence de pression crée une force qui pousse l’aile vers le haut.

Une autre relation entre la portance et le coefficient de portance existe à partir de la relation suivante : le coefficient de portance est une grandeur sans dimension qui caractérise la performance aérodynamique d’un profil. Le coefficient de portance dépend de la forme du profil, de l’angle d’incidence, et du nombre de Reynolds, qui est un nombre sans dimension qui mesure le rapport entre les forces d’inertie et les forces de viscosité dans un écoulement. Le coefficient de portance est défini par la formule $C_L = \frac{L}{\frac{1}{2} \rho V^2 S}$​, où $C_L$ est le coefficient de portance, $L$ est la portance, $\rho$ est la densité de l’air, $V$ est la vitesse du vent relatif, et $S$ est la surface de l’aile. Le coefficient de portance varie avec l’angle d’incidence, et atteint un maximum avant de diminuer brusquement. Ce phénomène correspond au décrochage de l’aile, qui se produit quand l’air se détache de l’extrados et crée une zone de turbulence.

La portance est proportionnelle à la pression dynamique, qui est le produit de la densité de l’air par le carré de la vitesse du vent relatif, c’est-à-dire $\frac{1}{2} \rho V^2$. La densité de l’air dépend de la pression, de la température, et de l’humidité de l’air. La densité de l’air diminue avec l’altitude, ce qui réduit la portance. La vitesse du vent relatif dépend de la vitesse de l’avion et de la vitesse du vent. La vitesse du vent relatif augmente avec la vitesse de l’avion, ce qui augmente la portance. La rugosité de la surface de l’aile influence aussi la portance, car elle modifie l’écoulement de l’air sur l’aile. Une surface rugueuse crée plus de frottement et de turbulence qu’une surface lisse, ce qui réduit la portance.


Références :

- Anderson, J. D. (2017). _Fundamentals of aerodynamics_ (6th ed.). McGraw-Hill Education.






---

```markdown
1. Introduction
2. Question de recherche 
3. Contexte théorique et Hypothèse
	3.1. Trainée
	3.2. Portance
	3.3. Profil d'aile
	3.4. Hypothèse
4. Variables
5. Diagramme
6. Apparatus
7. Méthodologie
	7.1. Materiels utilisés
	7.2. Procédure expérimentale
	7.3. Risques liés à l'expérience
1. Collecte et traitement des données
	9.1. Données brutes
	9.2. Données traités
10. Graphiques
11. Analyse et Conclusion
12. Evaluation
13. Références
```

**Sujet :** Étudier la relation entre la vitesse et les forces de portance et de trainée d'un aileron

## 1. Introduction
X

## 2. Question de recherche 
Quelle est la relation entre la vitesse et les forces de portance et de traînée d'un aileron ?

## 3. Contexte théorique et Hypothèse

### 3.1. Trainée
La résistance qu'un fluide exerce sur un corps en mouvement est connue sous le nom de traînée comme illustré dans la figure ci-dessus. 
![[Pasted image 20240315125206.png]]
$$\text{Figure 1 - Trainée exercé sur un avion}$$
Cette force est principalement le résultat de deux phénomènes : la traînée de forme, liée à la manière dont le fluide s'écoule autour du corps, et la traînée de frottement, qui est la conséquence directe des forces visqueuses à la surface du corps. L'équation générale qui la décrit est :
$$F_d=\frac{1}{2}\rho v^2C_dA$$
où $\rho$ est la densité de l'air, $v$ la vitesse de l'objet, $C_d$​ le coefficient de traînée, et $A$ la surface de référence.

### 3.2. Portance
À l'inverse, la portance est la force qui agit perpendiculairement au flux de fluide. Pour un aileron, cette force est cruciale car elle permet de contrôler la manœuvrabilité et la stabilité de l'appareil. Mathématiquement, elle est représentée par:
$$F_L=\frac{1}{2}\rho v^2C_LA$$
Ici, $C_L$​ est le coefficient de portance qui dépendra fortement de l'angle d'attaque et de la forme du profil d'aile.

### 3.3. Profil d'aile
Le profil d'aile est sélectionné en fonction de l'application spécifique et du régime de vol désiré. Il influence directement les coefficients de portance et de traînée par sa forme et son épaisseur. La conception optimale d'un profil d'aile recherche un équilibre entre une portance élevée et une traînée minimale, permettant ainsi le meilleur rendement possible.

### 3.4. Hypothèse
En se basant sur les théories aérodynamiques et les équations susmentionnées, je peux postuler que la relation entre la vitesse de l'aileron et les forces de portance et de traînée sera directement proportionnelle au carré de la vitesse. Cela signifie qu'à mesure que la vitesse double, les forces de portance et de traînée augmenteront de quatre fois. On anticipera donc une augmentation exponentielle de ces forces avec l'accroissement de la vitesse, ce qui aura des implications significatives sur la conception et le comportement des ailerons en conditions réelles.

## 4. Variables

**Variable indépendante**

- **Variable :** Vitesse de l'air $v$
- **Unités :** mètres par seconde $m/s$
- **Justification de la plage de valeurs :** La gamme de vitesses choisie pour la soufflerie est de $5-30 m/s$ pour couvrir le régime de vol allant des basses aux hautes vitesses, permettant d'observer la transition de l'écoulement laminaire à turbulent, et de capturer les effets de la traînée et de la portance sur des profils d'aileron.

**Variables dépendantes**

- **Variable :** Force de traînée ($F_d$)
- **Unités :** Newton ($N$)
- **Instrument de mesure :** Balance de précision avec capteur de force $\pm 0,01 N$
- **Variable :** Force de portance $F_L$
- **Unités :** Newton $N$
- **Instrument de mesure :** Balance de précision avec capteur de force $\pm 0,01 N$

**Variables contrôlées**

| Variable contrôlée   | Méthode de contrôle                         | Justification                                                         |
| -------------------- | ------------------------------------------- | --------------------------------------------------------------------- |
| Température de l'air | Utiliser une salle climatisée               | Maintenir la densité de l'air constante pour des mesures fiables      |
| Humidité de l'air    | Contrôler avec un déshumidificateur         | Éviter la variation de la masse volumique de l'air due à l'humidité   |
| Profil de l'aileron  | Utiliser le même modèle pour chaque test    | Assurer que seule la vitesse de l'air est modifiée                    |
| Angle d'attaque      | Fixer l'aileron dans une position constante | Isoler l'effet de la vitesse sur les forces de traînée et de portance |

## 5. Diagramme
X

## 6. Apparatus
X

## 7. Méthodologie

1. Préparation de la soufflerie aérodynamique en s'assurant que toutes les parties (entrée, chambre, sortie) sont correctement assemblées selon les spécifications techniques.
2. Vérification de l'ensemble électrique y compris la connexion du ventilateur à la batterie de voiture et la mise en place du variateur de tension pour le contrôle de la vitesse du vent.
3. Installation des ailettes (à la fois simples et incurvées) dans la soufflerie et réglage de leur position à l'angle d'attaque prédéterminé.
4. Calibration de la balance aérodynamique et de l'anémomètre pour mesurer respectivement la force d'appui et la force de traînée avec l'incertitude spécifiée.
5. Lancement des tests à différentes vitesses de vent en commençant par la vitesse la plus basse et en augmentant progressivement jusqu'à la vitesse la plus élevée prévue.
6. Réalisation de mesures répétées pour chaque configuration d'ailette afin d'obtenir des données fiables et reproductibles.
7. Observation et enregistrement des phénomènes de création de vortex et de séparation d'écoulement pour chaque type d'ailette.
8. Collecte des données de force d'appui et de traînée à partir des instruments de mesure pour chaque vitesse et type d'ailette.
9. Analyse préliminaire des données pour identifier des tendances ou des anomalies.
10. Finalisation des tests, révision des données collectées et préparation pour l'analyse détaillée.

## 8. Risques liés à l'expérience

**Sécurité** : Compte tenu des risques associés à l'utilisation d'une soufflerie et de composants électriques, des procédures de sécurité strictes ont été suivies. Un périmètre de sécurité a été établi autour de l'équipement pour empêcher tout accès non autorisé pendant le fonctionnement de la soufflerie. Des équipements de protection individuelle, comme des lunettes de sécurité et des gants ont été portés à tout moment. De plus, un extincteur était à portée de main en cas d'urgence.

**Environnementaux** : Pour minimiser l'impact environnemental, l'expérience a été effectuée dans un circuit fermé, limitant ainsi la consommation d'énergie. L'appareillage a été conçu pour être réutilisable, réduisant le besoin de matériaux jetables et l'empreinte carbone de l'expérience.

**Éthiques** : Toutes les données ont été traitées avec la plus grande intégrité, sans altération ni exagération des résultats. La transparence était la pierre angulaire de cette expérience, garantissant que les conclusions tirées étaient fondées sur des observations vérifiables et reproductibles.