Comme nous pouvons le voir dans la Figure \ref{fig7}, l'inductance dans un circuit joue un rôle clé dans la manière dont le circuit réagit au courant alternatif. Celle-ci, souvent désignée par le symbole $L$, est la propriété qui détermine la tension induite due à un changement du flux de courant.
\\
La relation qui régit le courant $I$ et la tension $U(t)_L$ aux bornes de l'inducteur d'inductance $L$ est donnée par la loi de Faraday qui stipule que la tension induite dans un inducteur est proportionelle au taux de changement du courant qui le traverse :
$$\begin{equation}
    U(t)_L=L\frac{dI}{dt}
\end{equation}$$
En utilisant la boucle unique montrée ci-dessus, nous avons :
$$\begin{equation}
    U(t)=U(t)_L
\end{equation}$$
En se basant de l'équation \label{eq:5.2}, on peut réécrire l'équation (haut) et cela donne :
$$\begin{equation}
    \Re e\left(U_0e^{j\omega t}\right)=L\frac{dI}{dt}
\end{equation}$$
Prenons l'intégrale des deux membres :
$$\begin{equation}
    \intop{\Re e\left(U_0e^{j\omega t}\right)dt}=\intop{L\frac{dI}{dt}dt}
\end{equation}$$
$$\begin{equation}
    \Re e\intop{U_0e^{j\omega t}dt}=\intop{L\frac{dI}{dt}dt}
\end{equation}$$
Calculons les intégrales des deux côtés :
$$\begin{equation}
    \Re e\left(\frac{1}{j\omega}U_0e^{j\omega t}\right)= LI
\end{equation}$$
Sachant que l'inductance $L$ est une quantité réel, nous obtenons :
$$\begin{equation}
    I=\Re e\left(\frac{1}{j\omega L}U_0e^{j\omega t}\right)
\end{equation}$$
Soit $U_L = U_0e^{j\omega t}$ et $Z_L$ pouvant être définie comme l'impédance d'un inducteur tel que :
$$\begin{equation}
    I=\Re e\left(\frac{1}{j\omega L}U_0e^{j\omega t}\right)
\end{equation}$$




Pour une tension appliquée sinusoïdale d'équation \ref{eq:5.2}, le courant ne peut pas changer instantanément à cause de l'inertie du champ magnétique dans l'inducteur. Cela entraîne un déphasage entre la tension et le courant, où le courant est en retard de phase de $\frac{\pi}{2}$ radians par rapport à la tension.
\\
En considérant une tension sinusoïdale appliquée à l'inducteur, nous pouvons calculer le courant comme suit :
\begin{equation}
    U_L=L\frac{dI}{dt}=U_0\cos(\omega t)
\end{equation}
En intégrant cette relation par rapport au temps pour trouver le courant $I(t)$, nous obtenons :
\begin{equation}
    I(t) = \frac{U_0}{\omega L}\sin(\omega t) + c
    \label{eq:9.3}
\end{equation}
Dans l'équation \ref{eq:9.3}, $c$ représente la constante d'intégration. Dans un circuit où le courant est nul au temps $t=0$, nous avons $\sin(0) = 0$ ce qui donne $c=0$. Ainsi le courant de l'inducteur est :
\begin{equation}
    I(t) = \frac{U_0}{\omega L}\sin(\omega t)
\end{equation}
Cela nous montre que le courant à travers l'inducteur est en retard de phase de $\frac{\pi}{2}$ par rapport à la tension appliquée. En notation complexe, les phasors pour la tension et le courant dans un circuit avec inductance sont exprimés comme suit :
\begin{equation}
    \hat{U}(t) = U_0e^{j\omega t}
\end{equation}
\begin{equation}
    \hat{I}(t) = U_0\frac{1}{j\omega L}\footnotemark e^{j\omega t}
\end{equation}
\footnotetext{L'expression $\frac{1}{j\omega L}$ est connue sous le nom de réactance inductive $X_L$ et elle représente l'opposition de l'inducteur au courant alternatif.}
En raison de la présence de $j$ dans le dénominateur, cela se traduit par un déphasage de $-\frac{\pi}{2}$ qui est cohérent avec notre compréhension antérieure.
