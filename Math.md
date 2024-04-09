\section{Le circuit avec capacité}
\begin{figure}[H]
\centering
\includegraphics[width=50mm]{pure-capacitive-circuit.jpg}
\caption{Un circuit avec capacité\cite{capacite}}
\label{fig6}
\end{figure}
Comme nous pouvons le voir dans la Figure \ref{fig6} qui est un circuit avec condensateur, son comportement est déterminé par le condensateur $C$ qui est le condensateur du circuit à stocker l'énergie sous forme de champ électrique. Lorsqu'il est soumis à une tension alternative, un condensateur présente une réactance capacitive qui s'oppose à la variation du courant provoquant un déphasage entre la tension et le courant.
\\
Pour un courant alternatif, la relation entre la tension $U(t)_C$ à travers un condensateur et le courant $I$ qui le traverse est donnée par la relation suivante :
$$\begin{equation}
    U(t)_C = \frac{1}{C}\intop{Idt}
\end{equation}$$
En utilisant la boucle illustrée ci-dessus, nous avons :
$$\begin{equation}
    U(t) = U(t)_C
\end{equation}$$
En se basant de l'équation 5.2, nous combinons tout ce qui précède pour écrire :
$$\begin{equation}
    \Re e(U_0 e^{j\omega t}) = \frac{1}{C} \intop{Idt}
\end{equation}$$
En prenant la dérivée des deux membres, nous avons :
$$\begin{equation}
    \frac{d}{dt}\left(\Re e(U_0 e^{j\omega t})\right) = \frac{d}{dt}\left(\frac{1}{C} \intop{Idt}\right)
\end{equation}$$
$$\begin{equation}
    \Re e\frac{d}{dt}\left(U_0 e^{j\omega t}\right) = \frac{d}{dt}\left(\frac{1}{C} \intop{Idt}\right)
\end{equation}$$
En simplifiant, nous obtenons :
$$\begin{equation}
    \Re e\left(j\omega U_0 e^{j\omega t}\right) = \frac{1}{C}I
\end{equation}$$
Sachant que la capacité $C$ est une quantité réelle, nous pouvons réécrire l'équation (en haut) comme suit :
$$\begin{equation}
     I = \Re e\left(j\omega C \hspace{1mm} U_0 e^{j\omega t}\right)
\end{equation}$$
Soit $U_C = U_0 e^{j\omega t}$ et définissons $Z_C$ comme l'impédance complexe d'un condensateur telle que :
$$\begin{equation}
     Z_C = \frac{1}{j\omega C}=-\frac{j}{\omega C}
\end{equation}$$
Sachant que $C$ est réel, l'impédance $Z_C$ du condensateur est un nombre imaginaire pur. Ainsi, $I$ peut être écrit comme suit :
$$\begin{equation}
     I = \Re e\left(\frac{U_C}{Z_C}\right)
\end{equation}$$
Nous avons ainsi :
$$\begin{equation}
     I = \frac{U_C}{Z_C}
\end{equation}$$
Ce principe est similaire à la loi d'Ohm dans les circuits à courant continu. Cette relation facilite grandement les calculs dans le sens où nous effectuons des calculs en utilisant des impédances, des tensions et des courants complexes, puis nous prenons la partie réelle comme réponse finale comme avec la résistance et l'inductance que nous allons voir tout de suite.
