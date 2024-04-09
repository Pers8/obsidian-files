\begin{figure}[H]
\centering
\includegraphics[width=60mm]{Series-RLC-Circuit-Analysis-Example-Problems-660x330.jpg}
\caption{Un circuit CA RLC en série\cite{rlc}}
\label{fig9}
\end{figure}
Pour analyser un circuit CA RLC en série, nous considérons la combinaison de la résistance $R$, de l'inductance $L$ et du condensateur $C$ connectées en série avec une source de tension alternative $U(t)$ illustré dans la Figure \ref{fig9}. 
\\
Pour un circuit alimenté par une source de tension de fréquence $f$, les impédances des différents composants RLC sont données par :
\begin{equation}
    Z_R=R \hspace{2mm}, \hspace{2mm}  Z_C = \frac{1}{j\omega C} \hspace{2mm}, \hspace{2mm} Z_L=j\omega L
    \label{eq:10.1}
\end{equation}
La chose la plus importante à noter est que les réactances inductive et capacitive dépendent de la fréquence de la source de tension. Maintenant, nous allons utiliser entre $U_i$, $I$, $U_R$, $U_L$ et $U_C$ étudié antérieurement. En appliquant la loi des mailles de Kirchhoff\footnote{La loi des mailles de Kirchhoff stipule que la somme des différences de potentiel (tensions) autour d'une boucle fermée doit être nulle}sur la tension étendue aux impédances complexes, nous obtenons :
\begin{equation}
    U_i-U_R-U_L-U_C=0
\end{equation}
En utilisant les relations d’Ohm étendues aux impédances complexes, nous avons :
\begin{equation}
    \begin{split}
        U_R=Z_R I \\
        U_L=Z_L I \\
        U_C=Z_C I
    \end{split}
\end{equation}
En substituant ces expressions dans l’équation ci-dessus, nous trouvons :
\begin{equation}
    U_i=Z_R I+Z_L I+Z_C I
\end{equation}
En résolvant pour le courant $I$, nous obtenons :
\begin{equation}
    I=\frac{V_i}{Z_R+Z_L+Z_C}
\end{equation}
L’impédance totale $Z$ du circuit RLC en série sera ainsi donnée par :
\begin{equation}
    Z=Z_R+Z_L+Z_C=R+j\left(\omega L-\frac{1}{\omega C}\right)
\end{equation}
Le module de $Z$ sera égale à :
\begin{equation}
    |Z|=\sqrt{R^2+\left(\omega L-\frac{1}{\omega C}\right)^2}
\end{equation}
L'argument de $Z$ peut être noté comme suit :
\begin{equation}
    \phi=\arctan\left(\frac{\omega L-\frac{1}{\omega C}}{R}\right)
\end{equation}
Nous pouvons réécrire $Z$ en utilisant la forme d'Euler évoqué antérieurement et cela donne :
$$\begin{equation}
    \begin{split}
        Z= |Z|e^{j\phi}
    \end{split}
\end{equation}$$
Nous avons ainsi :
$$\begin{equation}
    Z = \sqrt{R^2+\left(\omega L-\frac{1}{\omega C}\right)^2}\hspace{2mm}e^{\hspace{0.5mm}j\arctan\left(\frac{\omega L-\frac{1}{\omega C}}{R}\right)}
\end{equation}$$


Notez que le module et l'argument de l'impédance $Z$ dépendent tous deux de la fréquence de la tension de la source. Cette propriété est utile dans la conception de filtres et a de nombreuses autres applications dans les circuits électroniques.