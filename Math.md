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
    Z_L=j\omega L
\end{equation}$$
Comme $L$ est réel, l'impédance $Z_L$ est un imaginaire pur. Nous pouvons le courant $I$ comme suit :
$$\begin{equation}
    I=\Re e\left(\frac{V_L}{Z_L}\right)
\end{equation}$$
Ainsi, nous avons :
$$\begin{equation}
    I=\Re e\left(\frac{V_L}{Z_L}\right)
\end{equation}$$
