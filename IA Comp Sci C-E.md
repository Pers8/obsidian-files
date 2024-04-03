# Critère E : Évaluation 


## 1. Évaluation du site

| Critère de Réussite                                                          | Réalisé? | Feedback du client                                                                                                         |
| ---------------------------------------------------------------------------- | -------- | -------------------------------------------------------------------------------------------------------------------------- |
| L'utilisateur peut voir les prix et tous mes travaux sur un seul site web    | Oui      | "Comme je le souhaitais"                                                                                                   |
| Le site est automatisé et lié à un serveur Discord                           | Oui      | "Le système d'automatisation du serveur Discord fonctionne parfaitement via un bot !"                                      |
| Les commandes peuvent être gérées et créées directement à partir du site web | Oui      | "Les commandes sont très utiles et très faciles à utiliser."                                                               |
| L'utilisateur peut facilement commander plusieurs articles à la fois.        | Oui      | "Le système de commande permet à mes clients de saisir très facilement plusieurs commandes à la fois (en une seule fois)." |

## 2. Recommandations d'amélioration

My client was happy with the final product and agreed that it met his needs, as evidenced by a round-up message review of the project. However, we have nonetheless identified the below features as areas to improve upon:
- **Low audio quality** : in the WeChat message, this was cited as the (only) main
frustration. I used the built-in browser 'Web Speech API' for text-to-speech synthesis, and it is quite robotic. An alternative would be to use a more natural sounding, third-party API.
- **Loading time is long** : opening articles takes ~3s/page, since every word in the article is individually fetched from the database. This makes it frustrating to read longer-form content An alternative approach, where article contents are fetched in chunks (e.g. when clicking on new pages), may mitigate this issue.
We also discussed a couple of unimplemented possible future features.
- **More languages could be supported** : Peter is learning Greek, and hopes to
eventually read in the language as well. Supporting this is reasonably straightfoward (assuming the UI remains in English), since Greek Python NLP libraries exist.
- **Reading streaks could be added to the homepage**, which Peter mentioned could improve motivation. Peter's daily reading time is already logged by the database, so this would merely involve analyzing and visualizing existing historical data.