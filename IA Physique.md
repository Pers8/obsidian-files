
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

Pour comprendre comment la portance se crée, il faut d’abord connaître le principe de conservation de la quantité de mouvement. Ce principe stipule que la somme des quantités de mouvement d’un système isolé reste constante, sauf s’il y a une force extérieure qui agit sur le système. La quantité de mouvement d’un corps est le produit de sa masse par sa vitesse. Par exemple, si un corps de masse $m$ se déplace à la vitesse $v$, sa quantité de mouvement est $p = mv$. Si le corps change de vitesse, sa quantité de mouvement change aussi, et il faut qu’il y ait une force qui provoque ce changement. La force est égale à la variation de la quantité de mouvement par unité de temps, c’est-à-dire $F = \frac{dp}{dt}$​.

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
4. Variables
5. Diagramme
6. Apparatus
7. Méthodologie
8. Risques liés à l'expérience
9. Collecte et traitement des données
	9.1. Données brutes
	9.2. Données traités
10. Graphiques
11. Analyse et Conclusion
12. Evaluation
13. Références
```


## Introduction
X

## Question de recherche 
Quelle est la relation entre la vitesse et les forces de portance et de trainée d'un aileron.











