\section{Le circuit avec capacité}
\begin{figure}[H]
\centering
\includegraphics[width=50mm]{pure-capacitive-circuit.jpg}
\caption{Un circuit avec capacité\cite{capacite}}
\label{fig6}
\end{figure}
Comme nous pouvons le voir dans la Figure \ref{fig6} qui est un circuit avec capacité, son comportement est déterminé par la capacité $C$ qui est la capacité du circuit à stocker l'énergie sous forme de champ électrique. Lorsqu'il est soumis à une tension alternative, un condensateur présente une réactance capacitive qui s'oppose à la variation du courant provoquant un déphasage entre la tension et le courant.
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
    \Re e(U_0 e^{})
\end{equation}$$
Si on applique une tension sinusoïdale d'equation \ref{eq:5.2} à un condensateur, la dérivée temporelle de cette tension sera la suivante :
$$\begin{equation}
    \frac{dU}{dt} = -U_0\omega\sin(\omega t)
\end{equation}$$
Le courant dans le circuit qui est la charge accumulée par unité de temps dans le condensateur devient :
\begin{equation}
    I(t) = -CU_0\omega\sin(\omega t)
\end{equation}
On peut réécrire le courant comme une fonction sinusoïdale décalée de $\frac{\pi}{2}$ radians par rapport à la tension, signifiant que le courant précède la tension :
$$\begin{equation}
    I(t) = CU_0\omega\cos(\omega t + \frac{\pi}{2})
\end{equation}$$
En utilisant les nombres complexes pour représenter ce courant alternatif, nous introduisons le phasor du courant $\hat{I}(t)$ :
\begin{equation}
    \hat{I}(t) = j\omega CU_0e^{j\omega t}
\end{equation}
La présence du terme $j$ indique une avance de phase de $\frac{\pi}{2}$ par rapport à la tension appliquée. La réactance capacitive $X_C$ peut être définie comme l'inverse du produit de la fréquence angulaire et la capacité :
\begin{equation}
    X_C = \frac{1}{\omega C}
\end{equation}
La loi d'Ohm pour un circuit contenant uniquement un condensateur s'écrit ainsi :
\begin{equation}
    \hat{U}(t) = \hat{I}(t)X_C=j\hat{I}(t)\frac{1}{\omega C}
\end{equation}