

---

```markdown
1. Introduction
2. Question de recherche 
3. Contexte théorique
4. Hypothèse
5. Variables
6. Diagramme
7. Apparatus
8. Méthodologie
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

Le vol d'un avion est orchestré en grande partie par l'interaction entre la vitesse et les forces aérodynamiques. L'aile est soumise à diverses forces déterminant la dynamique de vol. Les deux forces fondamentales agissant sur un profil aérodynamique sont la portance, qui agit perpendiculairement à la direction du mouvement, et la traînée, qui agit parallèlement et en sens opposé au mouvement comme nous pouvons le voir ci-dessous.
![[portance et trainée]]
**Figure 1 :** Schéma représentant les forces de portance et de traînée agissant sur un profil aérodynamique.

Comme montré sur la Figure 1, La portance est le résultat de la forme du profil aérodynamique et de son angle d'attaque noté $a$, créant une différence de pression entre les surfaces supérieure et inférieure. Selon le principe de Bernoulli, l'air se déplaçant plus rapidement au-dessus du profil aérodynamique conduit à une pression plus basse, générant ainsi de la portance. Cela peut être représenté par le coefficient de portance $C_L$​, qui est un nombre sans dimension décrivant la portance produite par un profil aérodynamique à un angle d'attaque donné.
La traînée est la force aérodynamique qui s'oppose au mouvement de l'avion dans l'air. Elle se compose de divers composants, mais principalement de la traînée de forme (due à la forme) et de la traînée de frottement (due à la rugosité de la surface). Le coefficient de traînée $C_D​$, similaire au coefficient de portance, est une quantité sans dimension qui quantifie la traînée ou la résistance d'un objet dans un environnement fluide.

La relation entre la vitesse $v$, la portance $F_l$ et la traînée $F_d$ peut être décrite par les équations suivantes :
$$F_d=\frac{1}{2}\rho v^2 A C_d$$
$$F_l=\frac{1}{2}\rho v^2 A C_l$$
où $\rho$ est la densité de l'air, $A$ est l'aire de référence et $v$ la vitesse du profil par rapport à l'air.

À mesure que la vitesse du profil aérodynamique augmente, la portance générée augmente également en supposant un angle d'attaque constant. Cependant, la force de traînée augmentera également, présentant un compromis que les concepteurs doivent naviguer pour optimiser la performance. L'interaction entre la portance et la traînée est nécessaire pour déterminer les capacités de vol d'un avion car des vitesses plus élevées entraînent généralement plus de portance mais aussi une plus grande traînée. Pendant le vol, les changements de vitesse modifient le nombre de Reynolds, qui caractérise l'écoulement de l'air sur le profil aérodynamique et indique si l'écoulement est laminaire ou turbulent. L'apparition de la turbulence peut grandement affecter la portance et la traînée vécues par le profil aérodynamique.

## 4. Hypothèse

En se basant sur les théories aérodynamiques et les équations susmentionnées, je peux postuler que la relation entre la vitesse de l'aileron et les forces de portance et de traînée sera directement proportionnelle au carré de la vitesse. Cela signifie qu'à mesure que la vitesse double, les forces de portance et de traînée augmenteront de quatre fois. On anticipera donc une augmentation exponentielle de ces forces avec l'accroissement de la vitesse, ce qui aura des implications significatives sur la conception et le comportement des ailerons en conditions réelles.

## 5. Variables

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

### 7.1. Matériels utilisés

- Ventilateur de radiateur automobile 17 pouces.
- Boîtes de carton recyclé
- Balance $\pm 0,5 g$
- Anémomètre $\pm 0,05 km/h$
- Batterie de voiture
- Variateur de tension
- Fils électriques et vis
- Ailette triangulaire incurvée de dimensions $17 cm$ par $20 cm$

### 7.2 Procédure expérimentale

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

### 7.3. Risques liés à l'expérience

**Sécurité** : Compte tenu des risques associés à l'utilisation d'une soufflerie et de composants électriques, des procédures de sécurité strictes ont été suivies. Un périmètre de sécurité a été établi autour de l'équipement pour empêcher tout accès non autorisé pendant le fonctionnement de la soufflerie. Des équipements de protection individuelle, comme des lunettes de sécurité et des gants ont été portés à tout moment. De plus, un extincteur était à portée de main en cas d'urgence.

**Environnementaux** : Pour minimiser l'impact environnemental, l'expérience a été effectuée dans un circuit fermé, limitant ainsi la consommation d'énergie. L'appareillage a été conçu pour être réutilisable, réduisant le besoin de matériaux jetables et l'empreinte carbone de l'expérience.

**Éthiques** : Toutes les données ont été traitées avec la plus grande intégrité, sans altération ni exagération des résultats. La transparence était la pierre angulaire de cette expérience, garantissant que les conclusions tirées étaient fondées sur des observations vérifiables et reproductibles.

## 8. Collecte et traitement des données

### 8.1.1. Données brutes 

Pour cette expérience, les mesures ont été prises à différents régimes de la soufflerie pour observer l'impact sur un aileron. Ces mesures ont été effectuées avec les incertitudes associées fournies par les instruments de mesure : ±0.05 km/h pour la vitesse et ±0.0005 kg pour la masse.

| Vitesse du vent dans la soufflerie (±0.05 km/h) | Masse (kg) ±0.0005 |
| :---------------------------------------------- | ------------------ |
| 10                                              | 0.038              |
| 20                                              | 0.138              |
| 30                                              | 0.307              |
| 40                                              | 0.543              |
| 50                                              | 0.831              |
| 60                                              | 1.213              |
**Tableau 1 :** Données Brutes de l'Expérience sur les Forces Aérodynamiques


### 8.1.2. Données traitées

Lors de l'expérimentation, la balance a été utilisée pour mesurer une force perçue comme un poids. En réalité, cette force n'est autre que la force de portance négative $F_L$ qui a été interprétée à tort par la balance comme étant un poids. La masse affichée par la balance est donc une masse fictive qui nous permet de calculer la force de portance réelle.
La formule classique pour déterminer le poids est égale à :$$
P = m \times g$$
où $m$ est la masse en kilogrammes et $g$ est l'accélération due à la gravité approximativement 9.81 $m/s^2$. Cependant, dans notre cas, le poids mesuré n'est pas un poids réel, mais la force de portance négative causée par la soufflerie sur l'aileron. Ainsi, la formule est ajustée pour refléter cette réalité :
$$F_L=m\times g$$
L'incertitude de la force de portance se calculera comme suit :
$$\Delta F_L=\Delta m \times g$$
Calcul de l'échantillon pour $m = 0.038 \hspace{1mm} kg$ :
$$F_L= 0.038 \times 9.81 \approx 0.373\hspace{1mm}$$$$\Delta F_L= 0.0005 \times 9.81 \approx 0.005\hspace{1mm}$$
$$F_L = 0.373 \pm 0.005 \hspace{1mm} N$$

| Vitesse du vent dans la soufflerie (±0.01 m/s) | Force de Portance (± 0.005 N) | Vitesse du vent dans la soufflerie au carré $v^2$ (m/s) |
| :--------------------------------------------: | :---------------------------: | ------------------------------------------------------- |
|                      2.8                       |             0,373             | 7,8                                                     |
|                      5.6                       |             1,35              | 31                                                      |
|                      8.3                       |             3,01              | 69                                                      |
|                       11                       |             5,33              | $1,2 \times 10^2$                                       |
|                       14                       |             8,15              | $2,0 \times 10^2$                                       |
|                       17                       |             11,9              | $2,9 \times 10^2$                                       |
