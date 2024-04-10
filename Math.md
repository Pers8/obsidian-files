





Considérons un circuit CA RLC en série alimenté par une source de tension sinusoïdale $U(t) = U_0 \cos(\omega t)$, où $U_0 = 10V$ est l'amplitude de la tension, et la fréquence de la source $f = 50Hz$. Les valeurs des composants du circuit sont les suivantes: une résistance $R = 100\Omega$, une capacité $C = 100\mu F$, et une inductance $L = 100mH$.

**Question 1:** Calculer l'impédance totale $Z$ du circuit en utilisant la forme d'Euler, sachant que $\omega = 2\pi f$.

**Question 2:** À partir de l'impédance trouvée, calculer le courant maximum $I_{max}$ dans le circuit. Ensuite, dessiner un graphe qui montre la différence de phase entre le courant et la tension, limitant la période à $\pi/2$.

### Solution:

**Question 1:**

D'abord, calculons $\omega = 2\pi f = 2\pi \times 50 = 100\pi , rad/s$.

Ensuite, utilisons les formules pour calculer l'impédance totale $Z$ en série:

$$Z = R + j(\omega L - \frac{1}{\omega C})$$

Remplaçons les valeurs données:

$$Z = 100 + j(100\pi \times 0.1 - \frac{1}{100\pi \times 100 \times 10^{-6}})$$

$$Z = 100 + j(31.4 - 31.8)$$

$$Z = 100 - j0.4 , \Omega$$

La forme d'Euler de $Z$ est obtenue en calculant le module et l'angle de $Z$:

$$|Z| = \sqrt{100^2 + (-0.4)^2} \approx 100$$

$$\phi = \arctan\left(\frac{-0.4}{100}\right) \approx -0.004 , rad$$

Donc, $Z$ en forme d'Euler est:

$$Z \approx 100e^{-j0.004}$$

**Question 2:**

Le courant maximum $I_{max}$ est obtenu lorsque la tension est à son maximum, donc:

$$I_{max} = \frac{U_0}{|Z|} = \frac{10}{100} = 0.1A$$

Pour le graphe montrant la différence de phase entre le courant et la tension, on sait que la tension et le courant sont déphasés de $\phi \approx -0.004 , rad$. Ce petit déphasage indique que le courant est presque en phase avec la tension, avec un léger retard. Sur un graphe de la tension et du courant en fonction du temps, limité à $\pi/2$, ce retard serait à peine perceptible.











Après avoir fini la partie théorique, je vais dans les lignes qui suivent parler de la pratique à travers un exemple concret. Cet exemple nous permettra d'appliquer les formules et concepts abordés précédemment, illustrant ainsi leur utilité dans des situations réelles. En résolvant un problème spécifique, nous verrons comment les impédances des composants RLC en série interagissent pour déterminer le comportement global du circuit face à une source de tension alternative. Cela nous aidera à mieux comprendre l'impact de chaque paramètre (résistance, inductance, et capacité) sur l'impédance totale du circuit et, par conséquent, sur le courant circulant à travers celui-ci.

Prenons comme exemple un circuit RLC en série alimenté par une source de tension alternative de fréquence $(f = 50 Hz)$, avec les valeurs suivantes pour chaque composant : $(R = 100 \Omega)$, $(L = 200 mH)$ et $(C = 100 \mu F)$. Notre objectif est de calculer l'impédance totale du circuit, le courant total circulant dans le circuit, et enfin, d'analyser l'effet de la fréquence sur ces paramètres.

1. **Calcul de l'impédance totale (Z)**

D'abord, convertissons la fréquence en pulsation $(\omega = 2\pi f)$, ce qui nous donne $(\omega = 2\pi \times 50 = 314.16 rad/s)$.

Ensuite, calculons les impédances de chaque composant :

- $(Z_R = R = 100 \Omega)$
- $(Z_L = j\omega L = j314.16 \times 0.2 = j62.832 \Omega)$
- $(Z_C = \frac{1}{j\omega C} = \frac{1}{j314.16 \times 100 \times 10^{-6}} = -j31.83 \Omega)$

L'impédance totale du circuit est donc : $Z = Z_R + Z_L + Z_C = 100 + j62.832 - j31.83 = 100 + j31.002 \Omega$

2. **Calcul du module et de l'argument de (Z)**

Le module de (Z) est : $|Z| = \sqrt{R^2 + ( \omega L - \frac{1}{\omega C})^2} = \sqrt{100^2 + 31.002^2} \approx 104.8 \Omega$

L'argument de (Z) est : $\phi = \arctan\left(\frac{\omega L - \frac{1}{\omega C}}{R}\right) = \arctan\left(\frac{31.002}{100}\right) \approx 17.3^\circ$

3. **Calcul du courant total (I)**

Si la source de tension $(U_i)$ est de $(220V)$, le courant total dans le circuit est : $I = \frac{U_i}{Z} = \frac{220}{104.8} \approx 2.1A$

Cet exemple illustre comment les valeurs des composants et la fréquence de la source de tension influencent l'impédance totale du circuit et, par conséquent, le courant qui y circule. En modifiant ces paramètres, on peut observer des variations significatives dans le comportement du circuit, ce qui est essentiel pour la conception de circuits électroniques, notamment dans le domaine des filtres et de la gestion des signaux.





















Considérons un circuit CA RLC en parallèle alimenté par une source de tension sinusoïdale $U(t) = 220\cos(\omega t)$ de fréquence $f = 50\,Hz$. Les valeurs des composants du circuit sont les suivantes : une résistance $R = 100\,\Omega$, une capacité $C = 100\,\mu F$, et une inductance $L = 100\,mH$.

\textbf{1)} Calculer l'impédance totale $Z$ du circuit en utilisant la forme d'Euler.\\


La fréquence angulaire $\omega$ est donnée par $\omega = 2\pi f = 2\pi \times 50 = 100\pi, \text{rad/s}$.

 

Pour un circuit RLC en parallèle, l'impédance totale $Z$ est donnée par:  $\frac{1}{Z} = \frac{1}{R} + \frac{1}{j\omega L} + j\omega C$ 
$\frac{1}{Z} = \frac{1}{100} + \frac{1}{j100\pi \times 0.1} + j100\pi \times 100 \times 10^{-6}$ 
$\frac{1}{Z} = 0.01 - j\frac{1}{10\pi} + j\frac{1}{10}$
$\frac{1}{Z} = 0.01 + j(0.1 - \frac{1}{10\pi})$ 
Calculons le module et l'argument de $\frac{1}{Z}$: [ |\frac{1}{Z}| = \sqrt{(0.01)^2 + (0.1 - \frac{1}{10\pi})^2} ] [ \phi = \arctan\left(\frac{0.1 - \frac{1}{10\pi}}{0.01}\right) ] Donc, [ Z = \frac{1}{|\frac{1}{Z}|}e^{-j\phi} ]