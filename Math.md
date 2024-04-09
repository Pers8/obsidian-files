\begin{figure}[H]
\centering
\includegraphics[width=70mm]{Practical-parallel-RLC-circuit.png}
\caption{Un circuit CA RLC en parallèle\cite{Ida}}
\label{fig11}
\end{figure}
Pour un circuit CA RLC en parallèle illustré dans la Figure \ref{fig11}, l'approche est différente de celle en série car chaque composant a la même tension appliquée à ses bornes mais le courant peut varier pour chaque élément. Dans un tel circuit, nous devons trouver les courants individuels qui traversent chaque composant pour ensuite les additionner et obtenir le courant total dans le circuit.
\\
Nous allons utiliser les relations des équations \ref{eq:10.1} 









Pour la résistance $R$, le courant $I_R(t)$ est donnée directement par la loi d'Ohm :
\begin{equation}
    U(t) = RI_R(t)
\end{equation}
\begin{equation}
    I_R(t) = \frac{U(t)}{R}
\end{equation}
Pour l'inducteur $L$, la tension aux bornes est proportionnelle à la dérivée du courant donc nous utilisons la relation suivante :
\begin{equation}
    U(t) = L\frac{dI_L}{dt}
\end{equation}
Pour le condensateur $C$, la tension aux bornes est le produit de la capacité et de l'intégrale du courant, d'où :
\begin{equation}
    U(t) = \frac{1}{C} \int{I_C(t)dt}
\end{equation}
Dans un circuit en parallèle, les courants à travers chaque composant peuvent être exprimés comme 
suit:
\begin{equation}
    I_L(t)=\frac{U_0}{\omega L}\sin(\omega t)
\end{equation}
\begin{equation}
    I_C(t)=-CU_0\omega\cos\left(\omega t + \frac{\pi}{2}\right)
\end{equation}
\begin{equation}
    I_R(t)=\frac{U_0}{R}\cos(\omega t)
\end{equation}
Ces équations démontrent que le courant à travers l'inducteur est en retard de $\frac{\pi}{2}$ par rapport à la tension tandis que le courant à travers le condensateur est en avance de $\frac{\pi}{2}$. Pour trouver le courant total $I(t)$ dans le circuit,  nous additionnons vectoriellement les trois courants en utilisant la notation phasorielle, où chaque courant est représenté par un phasor :
\begin{equation}
    \hat{I}_R(t)=\frac{\hat{U}(t)}{R}
\end{equation}
\begin{equation}
    \hat{I}_L(t)=\frac{\hat{U}(t)}{j\omega L}
\end{equation}
\begin{equation}
    \hat{I}_C(t)=-j\omega C\hat{U}(t)
\end{equation}
La somme des phasors de courant fournit le phasor du courant total :
\begin{equation}
    \hat{I}(t) = \hat{I}_R(t) + \hat{I}_L(t) + \hat{I}_C(t)
\end{equation}
Cette somme doit prendre en compte la direction et la magnitude de chaque phasor de courant. En termes de composantes réelles et imaginaires, cela revient à additionner les composantes sur les axes horizontal et vertical dans le plan complexe.
