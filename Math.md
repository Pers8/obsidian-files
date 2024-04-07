
\section{Le circuit avec résistance}
\begin{figure}[H]
\centering
\includegraphics[width=50mm]{R.png}
\caption{Un circuit avec une résistance}
\label{fig3}
\end{figure}
Comme nous pouvons le voir dans la Figure \ref{fig3} qui est un circuit purement résistif, la résistance $R$ joue un rôle très important voir central dans la relation entre le courant $I(t)$ et la tension $U(t)$.  Dans le cadre de l'alternance de tension et de courant en courant alternatif où la tension et le courant varient de manière sinusoïdale, la résistance impose que la tension et le courant soient en phase, ce qui signifie qu'ils atteignent leurs valeurs maximales et zéro simultanément.

Mathématiquement pour une tension sinusoïdale d'équation \ref{eq:5.2}, le courant dans un circuit résistif est donnée par :
$$\begin{equation}
    I(t) = \frac{U(t)}{R}=\frac{U_0}{R}\cos(\omega t)
    \label{eq:7.1}
\end{equation}$$
Dans l'équation \ref{eq:7.1}, $U_0$ correspond à l'amplitude de la tension. En termes de nombres complexes, nous pouvons exprimer la tension et le courant sous forme de phasors. Un phasor est une représentation complexe d'une grandeur sinusoïdale, où l'amplitude et la phase sont codées dans un nombre complexe. Dans ce cas pour un circuit avec résistance, les phasors associés à la tension d'équation \ref{eq:5.1} et au courant d'équation :
$$\begin{equation}
    \hat{I}(t) = \frac{U_0}{R}e^{j\omega t}
\end{equation}$$
Ces équations démontrent que dans le domaine des complexe, la tension et le courant sont directement proportionnels l'un à l'autre et ont la même phase ($e^{j\omega t}$) ce qui est une autre manière d'exprimer qu'ils sont en phase.

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