
\section{Le circuit avec résistance}
\begin{figure}[H]
\centering
\includegraphics[width=50mm]{R.png}
\caption{Un circuit avec une résistance}
\label{fig3}
\end{figure}
Comme nous pouvons le voir dans la Figure \ref{fig3} qui est un circuit purement résistif, la résistance $R$ joue un rôle très important voir central dans la relation entre le courant $I(t)$ et la tension $U(t)$.  Dans le cadre de l'alternance de tension et de courant en courant alternatif où la tension et le courant varient de manière sinusoïdale, la résistance impose que la tension et le courant soient en phase, ce qui signifie qu'ils atteignent leurs valeurs maximales et zéro simultanément.

$U(t)_R$, $I$ et $R$ sont lié par la relation suivante :
$$
U(t)_R=RI
$$

En utilisant la boucle unique montrée ci-dessus, nous avons :
$$U(t) = U(t)_R$$
Donc sachant que $U(t)_R=U_0 \cos(\omega t)=\Re e(U_0e^{j\omega t})$, en combinant avec l'équation *u=ri*, on obtient :
$$
RI = \Re e(U_0e^{j\omega t})
$$
Soit $U_R = U_0e^{j\omega t}$ et en réécrivant l'équation (en haut) comme suit :
$$
RI = \Re e U_R
$$
Sachant que $R$ est une quantité réelle, nous pouvons réécrire ce qui précède sous cette forme :
$$
I= \Re e(\frac{U_R}{R})
$$
Nous pouvons ainsi définir l'impédance de la résistance comme
$$Z_R=R$$
Sachant que $R$ est un nombre réel, $Z_R$ l'ai aussi et donc nous pouvons réécrire $I$ comme suit :
$$I=\Re e\left(\frac{U_R}{Z_R}\right)$$
$$I=\frac{U_R}{Z_R}$$
Ces équations démontrent que dans le domaine des complexes, la tension et le courant sont directement proportionnels l'un à l'autre et ont la même phase ($e^{j\omega t}$) ce qui est une autre manière d'exprimer qu'ils sont en phase.

\begin{figure}[H]
\centering
\includegraphics[width=100mm]{U-I.png}
\caption{Diagramme de l'évolution sinusoïdale de la tension et du courant dans un circuit purement résistif}
\label{fig4}
\end{figure}

\begin{figure}[H]
\centering
\includegraphics[width=80mm]{U-I Complexe.png}
\caption{Diagramme de phasor montrant l'alignement de phase entre la tension et le courant dans un circuit résistif}
\label{fig5}
\end{figure}
Sur le diagramme de phasor comme illustré par la Figure \ref{fig5}, les vecteurs de tension et de courant pour un circuit résistif se superposeraient, indiquant qu'il n'y a pas de déphasage entre eux. La Figure \ref{fig4} montre comment la tension et le courant atteignent leurs valeurs extrêmes en même temps et traversent zéro ensemble.