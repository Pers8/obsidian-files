\begin{figure}[H]
\centering
\includegraphics[width=60mm]{Series-RLC-Circuit-Analysis-Example-Problems-660x330.jpg}
\caption{Un circuit CA RLC en série\cite{rlc}}
\label{fig9}
\end{figure}
Pour analyser un circuit CA RLC en série, nous considérons la combinaison de la résistance $R$, de l'inductance $L$ et du condensateur $C$ connectées en série avec une source de tension alternative $U(t)$ illustré dans la Figure \ref{fig9}. 
\\
Pour un circuit alimenté par une source de tension de fréquence f, les impédances des différents composants RLC sont données par :
$$\begin{equation}
    Z_R=R \hspace{2mm}, \hspace{2mm}  Z_C = \frac{1}{j\omega C} \hspace{2mm}, \hspace{2mm} Z_L=j\omega L
\end{equation}$$
La chose la plus importante à noter est que les réactances inductive et capacitive dépendent de la fréquence de la source de tension. Maintenant, nous allons utiliser entre $U_i$, $I$, $U_R$, $U_L$ et $U_C$ étudié antérieurement. 
 


En appliquant la loi des mailles de Kirchhoff\footnote{La loi des mailles de Kirchhoff stipule que la somme des différences de potentiel (tensions) autour d'une boucle fermée doit être nulle}sur la tension étendue aux impédances complexes, nous obtenons :
$$\begin{equation}
    U_i-U_R-U_L-U_C=0
\end{equation}$$
En appliquant la loi d'Ohm étendue aux impédances complexes, nous avons les relations ci-dessus :
$$\begin{equation}
    U_R=Z_R I
\end{equation}$$
$$\begin{equation}
    U_L=Z_L I
\end{equation}$$
$$\begin{equation}
    U_C=Z_C I
\end{equation}$$
En substituant ce qui précède à l'équation (En haut), on obtient :
$$\begin{equation}
    U_i=Z_R I+Z_L I+Z_C I
\end{equation}$$
En résolvant cette expression pour $I$, on obtient :
$$\begin{equation}
    I=\frac{V_i}{Z_R+Z_L+Z_C}
\end{equation}$$
Soit $Z$ l'impédance complexe équivalente du circuit RLC en série défini comme suit :
$$\begin{equation}
    Z=Z_R+Z_L+Z_C=R+j\left(\omega L-\frac{1}{\omega C}\right)
\end{equation}$$
Le module de $Z$ sera égale à :
$$\begin{equation}
    |Z|=\sqrt{R^2+\left(\omega L-\frac{1}{\omega C}\right)^2}
\end{equation}$$
L'argument de $Z$ :
$$\begin{equation}
    \theta=\arctan\left(\frac{\omega L-\frac{1}{\omega C}}{R}\right)
\end{equation}$$
Notez que le module et l'argument de l'impédance $Z$ dépendent tous deux de la fréquence de la tension de la source. Cette propriété est utile dans la conception de filtres et a de nombreuses autres applications dans les circuits électroniques.
Nous pouvons noter la forme polaire comme suit :
$$\begin{equation}
    Z=|Z| $ \angle $ $ \theta
\end{equation}$$


En exprimant la charge $q$ en termes de courant $i$ (puisque $q=\int idt$) et en considérant une source de tension sinusoïdale d'équation \ref{eq:5.2}, l'équation ci-dessus peut être réécrite en prenant la dérivée de la charge par rapport au temps pour obtenir le courant :
\begin{equation}
    iR + L\frac{di}{dt}+\frac{1}{C}\int{idt}=U_0\cos(\omega t)
\end{equation}
La solution de cette équation différentielle donne le courant en fonction du temps. Pour résoudre cette équation en utilisant des méthodes analytiques, nous pouvons utiliser des méthodes de nombres complexes en exprimant la tension et le courant sous forme de phasors. Ainsi, en prenant la notation phasorielle et en utilisant la forme d'Euler, nous pouvons transformer l'équation différentielle en une équation algébrique :
\begin{equation}
    \hat{U}(t)=\hat{I}(t)Z\footnotemark
\end{equation}
\footnotetext{$Z$ est l'impédance totale du circuit donnée par $Z= R+j\omega L - \frac{j}{\omega C}$}
L'impédance totale $Z$ est une quantité complexe qui combine les effets de $R$, $L$, et $C$. La résistance $R$ ajoute une composante réelle à l'impédance, tandis que $L$ et $C$ contribuent aux composantes imaginaires. La partie imaginaire positive est due à l'inducteur, et la partie imaginaire négative est due au condensateur. La résolution de l'impédance complexe fournit la grandeur et la phase de l'impédance :
\begin{equation}
    |Z| = \sqrt{R^2+(\omega L - \frac{1}{\omega C})^2}
\end{equation}
\begin{equation}
    \tan^{-1}\left(\frac{\omega L - \frac{1}{\omega C}}{R}\right) = \gamma
    \label{eq:10.5}
\end{equation}
Dans l'équation \ref{eq:10.5}, $\gamma$ est l'angle de phase de l'impédance. Le courant phasor dans le circuit est obtenu en divisant le phasor de tension par l'impédance complexe :
\begin{equation}
    \hat{I}(t) = \frac{\hat{U}(t)}{Z}
\end{equation}
Ceci nous donne l'amplitude et la phase du courant dans le circuit. Pour déterminer le courant instantané, nous prenons la partie réelle du phasor de courant :
\begin{equation}
    I(t) = Re\left(\frac{U_0}{|Z|}e^{j(\omega t + \gamma)}\right)
\end{equation}
