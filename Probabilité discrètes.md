---
tags:
  - math
---
# Probabilité discrètes
## Experience aléatoire-événements
Une expérience aléatoire est une expérience dont l'issue dépend du:: hasard.
<!--SR:!2024-01-13,74,290-->
L'ensemble des résultats possibles d'une expérience aléatoire est appelé:: univers.
<!--SR:!2024-02-18,112,310-->
On appelle événement:: toute partie de l'univers (sous-ensemble)
<!--SR:!2023-10-12,9,270-->

### Définitions
- Evénement élémentaire:: a une seule issue
<!--SR:!2024-01-09,70,290-->
- Evénement composé:: a plusieurs issues
<!--SR:!2024-01-03,66,290-->
- Evénement A et B (conjonction d'événement):: événement constitué des issues communes aux deux événements
<!--SR:!2023-11-05,5,230-->
- Evénement contraire a A noté A':: événement dont les issues n'appartiennent pas a A
<!--SR:!2024-01-05,68,250-->
- Evénement A ou B (disjonction d'événement):: événement constitué de toutes les issues des deux événements
<!--SR:!2023-11-08,10,250-->
- Evénement incompatible (mutuellement exclusif):: conjonction des deux événements avec aucune issue
<!--SR:!2023-11-06,8,230-->
- Evénement certain:: toutes les issues
<!--SR:!2024-02-20,114,310-->
- Evénement impossible:: aucune issue
<!--SR:!2023-10-18,17,290-->

## Calcul de probabilité
- La probabilité d'un événement est la somme:: des éléments élémentaires qui le compose.
<!--SR:!2023-11-11,13,270-->
- Lorsque les événements élémentaires ont meme probabilité, on dit qu'il y a:: équiprobabilité ou équi-répartition.
<!--SR:!2024-01-01,64,290-->

### Propriété
- $P(U)$=::1 
<!--SR:!2024-02-19,113,310-->
- $P(0)$=::0
<!--SR:!2024-01-10,71,290-->
- $P(A)+P(A')$=::1 
<!--SR:!2024-01-09,70,290-->
- $P(A\cup B)$=::$P(A)+P(B)-P(A\cap B)$
<!--SR:!2023-11-09,11,270-->
- $P(A/B)$=::$\frac{P(A\cap B)}{P(B)}=\frac{n(A\cap B)}{n(B)}$
<!--SR:!2023-10-18,17,290-->
- $P(A\cap B)$=::$P(A)\times P(B/A)$ ou $P(B)\times P(A/B)$
<!--SR:!2023-11-21,37,270-->
- Si deux événements sont indépendants alors $P(A/B)$=::$P(A)$
<!--SR:!2024-01-07,70,290-->
- $P(A')$=:: $1-P(A)$
<!--SR:!2024-01-04,67,290-->

## Événements indépendants
Deux événements sont indépendants si: : l'occurrence de chacun d'eux n'affecte pas la probabilité que l'autre se produise. Un exemple de ceci est l'échantillonnage à 1s avec remplacement.

Pour des événements indépendants A et B, $P(A\cap B)$=:: $P(A)P(B)$
<!--SR:!2023-11-01,3,233-->

## Événements dépendants
Deux événements sont dépendants si:: la survenance de l'un d'entre eux affecte la probabilité que l'autre se produise. L'échantillonnage sans remplacement en est un exemple.
<!--SR:!2023-11-02,4,212-->

Pour les événements dépendants A et B, $P(A\cap B)$=::$P(A)\times P(B/A)$
<!--SR:!2023-11-29,31,273-->

## Probabilité conditionnelle
Pour deux événements A et B, $A/B$ représente l'événement "A sachant B", et $P(A/B)$=::$\frac{P(A\cap B)}{P(B)}$
<!--SR:!2023-10-11,3,273-->

Pour des événements indépendants, $P(A)$=::$P(A/B)=P(A/B')$
<!--SR:!2023-11-01,3,233-->

Axiom des probabilités totales, pour événement secondaire : $P(B)$=::$P(A\cap B)+P(A'\cap B)$
<!--SR:!2023-10-26,11,253-->

$P(A\cap B')$=::$P(A)-P(A\cap B)$
<!--SR:!2023-11-02,4,233-->


$P(A \le X \le B)$ =::$P(X \le A) - P(X \le B-1)$