---
tags: [physics]
---

?
Une pile convertit l'énergie chimique en énergie électrique avec dissipation/perte d'énergie sous forme de chaleur.

- Une pile est caractérisée par:: sa fem $e$ et sa résistance interne $r$. $e$ en volt et $r$ en ohm.
- $e$ fem =>:: force électromotrice; travail par unité de charge pour faire circular les charges

Formule de la tension aux bornes d'une pile est:
?
$$U=e-rI$$- $U$ = tension dans la puissance électrique
- $e$ = fem de la puissance chimique
- $r$ = résistance interne 
- $I$ = intensité
![[Pasted image 20230118004329.png]]

Caractéristique intensité-tension d'une pile (graphe)::
![[Pasted image 20230118004405.png]]

On peut retrouver la formule $U=e-rI$ en effectuant le montage suivant::
![[Pasted image 20230118004433.png]]

- $U=e$ si:: $I=0$
- $e$ c'est la tension aux bornes de la pile quand:: elle ne fournit pas de courant
- Un pile idéale est une pile qui:: n'a pas de résistance interne $r=0$ (le graphe intensité-tension est constante en $e$)

circuit équivalent d'une pile réel::
![[Pasted image 20230118004520.png]]

## Circuits simples comportant des piles, récepteurs et resistors

**Tension aux bornes d'un récepteur**:
?
Un récepteur (ex un moteur, un électrolyseur) est un appareil qui consomme plus d'énergie que n'a besoin l'effet joule.
Le récepteur est caractérisé oar 1 fcem $e'$ (force contre électromotrice) et par sa résistance interne. 

Formule de la tension  d'un récepteur::$$U_{recept}=e'+rI$$
- Une pile branchée en opposition se comporte comme:: un récepteur


Formule des fem et fcem dans un circuit avec piles et récepteurs (+branchement):
?
![[Pasted image 20230118004651.png]]

## Circuit avec des nœuds comportant des générateurs

Schema du sens de parcours (rouge) et sens du courant (bleu) pour les piles et les résistances:
?
![[Pasted image 20230118005133.png]]

## Association de piles
**En série** (Avantage, branchement et formule)
?
Pour avoir plus de tension.
![[Pasted image 20230118005203.png]]

$$V_{PN}=V_{PA}+V_{AB}+V_{BN}$$
$$V_{PN}=e_{1}-r_{1}I+e_{2}-r_{2}I+e_{3}-r_{3}I$$
$$V_{PN}=e_{1}+e_{2}+e_{3}-(r_{1}+r_{2}+r_{3})I$$
$$e_s=\sum{e}$$$$r_s=\sum\limits{r}$$

**En parallèle** (Avantage, branchement et formule)
?
Pour avoir plus d'intensité
![[Pasted image 20230118005301.png]]

$$U_{PN}=e-r\frac{I}{n}=e-r\frac{I}{n}=e-r\frac{I}{n}$$
$$e_{//}=e,\;r_{//}=\frac{r}{n}$$