---
tags:
  - math
---
# Probabilité discrètes
## Experience aléatoire-événements
Une expérience aléatoire est une expérience dont l'issue dépend du:: hasard.
<!--SR:!2023-10-22,21,290-->
L'ensemble des résultats possibles d'une expérience aléatoire est appelé:: univers.
<!--SR:!2023-10-21,20,290-->
On appelle événement:: toute partie de l'univers (sous-ensemble)
<!--SR:!2023-10-03,2,250-->

### Définitions
- Evénement élémentaire:: a une seule issue
<!--SR:!2023-10-19,18,290-->
- Evénement composé:: a plusieurs issues
<!--SR:!2023-10-20,19,290-->
- Evénement A et B (conjonction d'événement):: événement constitué des issues communes aux deux événements
<!--SR:!2023-10-03,2,250-->
- Evénement contraire a A noté A':: événement dont les issues n'appartiennent pas a A
<!--SR:!2023-10-07,8,250-->
- Evénement A ou B (disjonction d'événement):: événement constitué de toutes les issues des deux événements
<!--SR:!2023-10-15,14,270-->
- Evénement incompatible (mutuellement exclusif):: conjonction des deux événements avec aucune issue
<!--SR:!2023-10-03,2,250-->
- Evénement certain:: toutes les issues
<!--SR:!2023-10-20,19,290-->
- Evénement impossible:: aucune issue
<!--SR:!2023-10-18,17,290-->

## Calcul de probabilité
- La probabilité d'un événement est la somme:: des éléments élémentaires qui le compose.
<!--SR:!2023-10-21,20,290-->
- Lorsque les événements élémentaires ont meme probabilité, on dit qu'il y a:: équiprobabilité ou équi-répartition.
<!--SR:!2023-10-18,17,290-->

### Propriété
- $P(U)$=::1 
<!--SR:!2023-10-20,19,290-->
- $P(0)$=::0
<!--SR:!2023-10-21,20,290-->
- $P(A)+P(A')$=::1 
<!--SR:!2023-10-22,21,290-->
- $P(A\cup B)$=::$P(A)+P(B)-P(A\cap B)$
<!--SR:!2023-10-19,18,290-->
- $P(A/B)$=::$\frac{P(A\cap B)}{P(B)}=\frac{n(A\cap B)}{n(B)}$
<!--SR:!2023-10-18,17,290-->
- $P(A\cap B)$=::$P(A)\times P(B/A)$ ou $P(B)\times P(A/B)$
<!--SR:!2023-10-13,12,270-->
- Si deux événements sont indépendants alors $P(A/B)$=::$P(A)$
<!--SR:!2023-10-21,20,290-->
- $P(A')$=:: $1-P(A)$
<!--SR:!2023-10-19,18,290-->