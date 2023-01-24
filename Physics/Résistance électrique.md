---
tags: [physics]
---

?
Tout les matériaux ne conduisent pas le courant électrique de la même manière, on définit la résistance électrique comme étant la formule::$$R=\frac{\Delta V}{I}$$

La résistance d'un fil conducteur a comme formule:
?
$$R=\frac{\rho l}{A}$$
- $R$ est la résistance en Ohm ($\Omega$)
- $\rho$ est la résistivité du matériau en ohm-mètre
- $l$ est la longueur du fil
- $A$ est la surface du fil

## Loi d'Ohm et conducteur ohmique

Caractéristique intensité-tension du resistor a comme graphe::
![[Pasted image 20230118003635.png]]

- Formule de la loi d'Ohm::$$U=RI$$ car $U$ et $I$ sont proportionnelles.

- **Loi d'Ohm**:: A température constante la tension et l'intensité aux bornes d'un conducteurs sont proportionnelles
- **Un conducteur ohmique**:: est un conducteur qui obéit a la loi d'Ohm ($R$ est constant)
![[Pasted image 20230118003812.png]]

## Association de résistors
- Association en série formule::$$R_{eqs}=R_1+R_2+\text{...}$$ l'association en série de plusieurs résistors est équivalent a un résistor $R_{eqs}$ dont la résistance est égale a la somme des résistances
- Association en parallèle formule::$$\frac{1}{R_{eqp}}=\frac{1}{R_{1}}+\frac{1}{R_{2}}+\text{...}$$ $$R_{eqp}=\frac{R_{1}R_{2}}{R_{1}+R_{2}}$$
## Dissipation d'énergie électrique dans un resistor (effet joule)
?
Lorsque qu'un conducteur est parcouru par un courant électrique il y a un dégagement de chaleur: c'est l'effet joule. 
Pour lutter contre l'effet joule on prévoit des dispositifs d'aération ou de ventilation. L'effet joule est utilisé avantageusement dans les plaques chauffantes, les fusibles, les chauffe-eau.

La puissance dissipé par effet joule est proportionnelle:: au carré de l'intensité.

3 formules de puissance dissipé::$$P=UI=RI^2=\frac{U^{2}}{R}$$

## Utilisation des appareils de mesure
Un appareil de mesure modifie le circuit et a un effet sur la mesure. 

- Utilisation d'un ampèremètre: un ampèremètre idéal:: a une résistance interne nulle
- Utilisation d'un voltmètre: un voltmètre idéal:: a une résistance interne infinie

## Diviseur de tension et montage potentiométrique
Formule et circuit
?
![[Pasted image 20230118004007.png]]


$$U=(R_{1}+R_{2})\times I$$
donc
$$I=\frac{U}{R_{1}+R_{2}}$$
On sait que
$$U_{1}=R_{1}\times I$$
donc
$$U_{1}=R_{1}\times \frac{U}{R_{1}+R_{2}}=\boxed{\frac{R_1}{R_{1}+R_{2}}\times U}$$
## Montage potentiométrique
Un potentiomètre est:: un conducteur ohmique ayant trois bornes, deux borne fixe A et B et une borne mobile C appelé curseur. Si l'on branche le potentiomètre par les deux bornes fixes A et B, ce dernier se comporte comme une résistance fixe. 
![[Pasted image 20230118004142.png]]

**Montage potentiométrique** branchement, formules pour 3 cas:
?
![[Pasted image 20230118004212.png]]
$$U_{AC}=\frac{R_{AC}}{R_{AC}+R_{CB}}U_{AB}=\frac{R_{AC}}{R_{AB}} \hspace2mm U_{AB}$$
- si C est en A $$R_{AC}=R_{AA}=0,\;U_{ac}=0$$
- si C est en B $$R_{AC}=R_{AB},\;U_{AC}=\frac{R_{AB}}{R_{AB}}U_{AB}=U_{AB}$$
- si C est entre A et B $$0<U_{S}<U_{AB}$$