---
tags:
  - computer_science
---


- **Le CPU et ses éléments**:: Le CPU (unité centrale de traitement) est le composant matériel qui effectue les opérations arithmétiques, logiques ou d’entrée/sortie sur les données. Il contient les éléments suivants :

    - L’UC (unité de contrôle):: Elle contrôle le fonctionnement du CPU en extrayant, décodant et exécutant les instructions de la mémoire principale (RAM).
    
    - L’UAL (unité arithmétique et logique):: Elle effectue les calculs et les comparaisons sur les données fournies par l’UC.
    
    - Les registres:: Ce sont de petits circuits qui stockent temporairement les valeurs intermédiaires des calculs ou des instructions. Les plus importants sont le MAR (registre d’adresses mémoire), le MDR (registre de données mémoire) et l’accumulateur.
    
- **L’unité de mémoire des systèmes informatiques**:: C’est le composant qui stocke les données et les instructions sous forme de séquences de chiffres binaires (bits). Un bit ne peut avoir que deux valeurs : 1 ou 0. Huit bits forment un octet. La mémoire se mesure en octets ou en multiples d’octets (Mo, Go, etc.).
- **Le bus de mémoire**:: C’est la connexion qui permet au CPU de communiquer avec la mémoire principale. Il transporte les adresses mémoire et les données entre le CPU et la RAM.

- **La mémoire primaire**:: c’est la mémoire qui est directement accessible par le CPU (via les bus). Elle peut contenir à la fois des données et des instructions qui sont en cours d’exécution sur le système informatique. Ces données et instructions sont stockées sous forme de code machine binaire. La mémoire primaire est volatile, c’est-à-dire qu’elle perd son contenu en cas de coupure de courant.
 
- **La mémoire RAM**:: c’est un type de mémoire primaire qui contient les programmes et les données de l’utilisateur qui ont été chargés depuis le démarrage du système. RAM signifie Random Access Memory, ce qui signifie qu’on peut accéder à n’importe quelle adresse de la mémoire en un temps constant. La mémoire RAM est généralement évolutive, c’est-à-dire qu’on peut augmenter sa capacité en ajoutant des modules de mémoire supplémentaires.

- **La mémoire ROM**:: c’est un autre type de mémoire primaire qui contient le BIOS (Basic Input Output System), un petit programme qui permet à l’ordinateur de savoir quoi faire pour trouver le système d’exploitation afin de démarrer l’ordinateur après la remise sous tension. ROM signifie Read Only Memory, ce qui signifie que son contenu est statique et ne peut pas être modifié. La mémoire ROM est non-volatile, c’est-à-dire qu’elle conserve son contenu même en cas de coupure de courant. La mémoire ROM fait généralement partie de la carte mère et est difficile à mettre à niveau.
- **La mémoire cache**:: c’est une petite mémoire à grande vitesse située à l’intérieur de l’unité centrale, utilisée pour conserver les données fréquemment utilisées, de sorte que le CPU doit accéder moins fréquemment à la mémoire RAM, beaucoup plus lente. La mémoire cache est une RAM (SRAM) plus petite et plus rapide qui stocke temporairement des instructions et des données. Il existe deux principaux types de mémoire cache : le cache L1, qui est placé sur le microprocesseur lui-même, et le cache L2, qui est placé entre la mémoire principale et le microprocesseur.
- **La mémoire secondaire**:: c’est la mémoire qui n’est pas directement accessible par le CPU, mais qui permet de stocker des programmes et des données pour une utilisation ultérieure. Ce type de mémoire est non-volatile, c’est-à-dire qu’il ne perd pas son contenu lorsque l’ordinateur est éteint. Les ordinateurs à usage général, tels que les ordinateurs personnels et les tablettes, utilisent différents types de dispositifs de stockage secondaire, tels que les dispositifs de stockage à semi-conducteurs (clés USB), les dispositifs de stockage optiques (CD, DVD, disques Blu-ray) et les dispositifs de stockage magnétiques (disques durs).

- **Le cycle d’instruction de la machine**:: c’est l’opération de base d’un ordinateur, qui consiste à chercher une instruction dans la mémoire, la décoder, l’exécuter et stocker le résultat. Le cycle se répète jusqu’à l’arrêt de l’ordinateur.

- **Les bus**:: ce sont des ensembles de fils qui permettent le transfert de données entre les différents composants de l’ordinateur. Il existe trois types de bus : le bus de données (MDR), qui transporte les données, le bus d’adresses (MAR), qui transporte les adresses mémoire, et le bus de contrôle, qui transporte les signaux de commande.

- **Les registres**:: ce sont des mémoires temporaires situées dans l’UC, qui stockent les données et les instructions en cours de traitement. Il existe plusieurs types de registres, tels que le compteur ordinal (PC), qui contient l’adresse de la prochaine instruction à exécuter, ou le registre d’instruction (IR), qui contient l’instruction en cours de décodage.

- **Le jeu d’instructions**:: c’est l’ensemble des instructions que l’UC est capable de comprendre et d’exécuter. Chaque instruction est codée en binaire et comporte un code opération (opcode), qui indique l’action à effectuer, et un ou plusieurs opérandes, qui indiquent les données à utiliser.

Voici quelques exemples d’instructions en code machine :

- `0001 0000 0000 0010` : cette instruction signifie “charger dans le registre 0 la donnée située à l’adresse 2 de la mémoire”.
- `0010 0000 0000 0100` : cette instruction signifie “stocker dans la mémoire à l’adresse 4 la donnée contenue dans le registre 0”.
- `0100 0000 0001 0001` : cette instruction signifie “ajouter les données contenues dans les registres 0 et 1, et placer le résultat dans le registre 0”.
- `0111 0000 0000 0000` : cette instruction signifie “arrêter l’exécution du programme”.

Le cycle Fetch -:: Execute est le processus de base d’un ordinateur, qui consiste à chercher une instruction dans la mémoire, la décoder, l’exécuter et stocker le résultat. Le cycle se répète jusqu’à l’arrêt de l’ordinateur. 

Voici les étapes du cycle Fetch - Execute::
1. Le compteur ordinal (PC) contient l’adresse de la mémoire où se trouve la prochaine instruction à exécuter. Cette adresse est copiée dans le registre d’adresses mémoire (MAR) via le bus d’adresses.
2. Le contenu (instruction) de la mémoire à l’adresse indiquée par le MAR est copié dans le registre de données mémoire (MDR) via le bus de données.
3. Le contenu (instruction) du MDR est copié dans le registre d’instruction (IR) qui sert à stocker temporairement l’instruction en cours de traitement.
4. Le PC est incrémenté de 1 pour pointer vers l’adresse de la prochaine instruction à exécuter.
5. L’instruction dans l’IR est décodée par l’unité de contrôle (UC) qui envoie des signaux de commande aux différents composants de l’ordinateur via le bus de contrôle.
6. L’instruction est exécutée par l’unité arithmétique et logique (UAL) qui effectue les calculs et les opérations logiques sur les données fournies par l’UC.
7. Le résultat de l’exécution est stocké dans un registre ou dans la mémoire selon l’instruction.

- **Le besoin de stockage persistant**:: Cette partie explique pourquoi nous avons besoin de stocker les données et les résultats du traitement effectué dans le CPU sur une mémoire persistante, comme le disque dur ou le SSD. La raison est que la RAM est volatile et perd son contenu en cas de coupure de courant, tandis que le CPU n’a pas de stockage permanent (seulement des registres).
- **HDD/SSD Types de stockage**:: Cette partie présente les deux types principaux de stockage persistant : le disque dur (HDD) et le disque à état solide (SSD). Le HDD utilise des plateaux magnétiques et des têtes de lecture/écriture pour stocker et accéder aux données, tandis que le SSD utilise des puces de mémoire flash pour le faire. Le SSD est plus rapide, plus silencieux et plus résistant aux chocs que le HDD, mais il est aussi plus cher et a une durée de vie limitée.
- **Mémoire primaire et mémoire secondaire**:: Cette partie distingue la mémoire primaire de la mémoire secondaire. La mémoire primaire est la mémoire qui est directement accessible par le CPU, comme la cache, la RAM et la ROM. La mémoire secondaire est la mémoire qui n’est pas directement accessible par le CPU, mais qui peut être transférée vers la mémoire primaire, comme le disque dur, le CD/RW, le lecteur de bande ou la clé USB.
- **Mémoire externe**:: Cette partie décrit la mémoire externe, qui est un type de mémoire secondaire qui peut être connectée ou déconnectée de l’ordinateur, comme le CD/RW, le lecteur de bande ou la clé USB. La mémoire externe permet de stocker des données à long terme, de les transporter ou de les partager avec d’autres ordinateurs.

- Il définit et explique les concepts clés suivants :
    - **Architecture des ordinateurs** : la structure et le fonctionnement des composants matériels d’un ordinateur, tels que l’unité centrale, la mémoire, les périphériques, etc.
    - **Système d’exploitation** : un ensemble de logiciels qui contrôle les ressources matérielles de l’ordinateur et fournit des services aux programmes informatiques. Il sert d’intermédiaire entre les applications logicielles et le matériel informatique.
    - **Application logicielle** : un programme informatique conçu pour répondre aux besoins des utilisateurs. Il utilise les services du système d’exploitation pour interagir avec le matériel informatique.
- Il donne des exemples de systèmes d’exploitation (Windows, Linux, MacOS) et d’applications logicielles (traitements de texte, feuilles de calcul, SGBD, clients de messagerie, navigateurs web, CAO, logiciels de traitement graphique).
- Il illustre les fonctions principales d’un système d’exploitation, telles que :
    - **Interface utilisateur** : le lien entre l’utilisateur et le matériel informatique. Il peut être de différents types, tels que graphique, en ligne de commande, en langage naturel, ou à base de menus.
    - **Communication avec les périphériques** : la gestion des interactions entre le système d’exploitation et les composants matériels externes à l’unité centrale, tels que les claviers, écrans, souris, imprimantes, microphones, etc.
    - **Gestion de la mémoire** : la répartition et la protection de la mémoire disponible dans un système informatique. Elle vise à éviter qu’une application n’interfère avec la mémoire utilisée par une autre application.
    - **Contrôle des ressources et multitâche** : l’allocation efficace des ressources (mémoire, temps de processeur, etc.) aux applications qui fonctionnent sur un système informatique. Elle permet de donner l’impression que plusieurs applications effectuent des tâches simultanément, alors qu’elles partagent le temps de l’unité centrale.
    - **Mise en réseau** : la gestion des connexions et des interactions avec les réseaux d’autres systèmes informatiques. Elle permet le partage des ressources (fichiers, imprimantes, etc.) entre les systèmes informatiques connectés à un réseau local ou à l’Internet.
    - **Accès aux disques et gestion des données** : la gestion des données stockées en mémoire et sur les disques. Elle implique de garder la trace des fichiers, de savoir quels fichiers sont utilisés par quelles applications, et de coordonner le transfert des données des fichiers du disque vers la mémoire primaire et vice versa.
    - **Sécurité** : la protection globale d’un système informatique contre les menaces internes ou externes. Elle implique de fournir une forme d’identité à l’utilisateur qui permettra son authentification.

- **Définition d’un système d’exploitation (SE)** : un ensemble de logiciels qui contrôle les ressources matérielles de l’ordinateur et fournit des services aux programmes informatiques. Il sert d’intermédiaire entre les applications logicielles et le matériel informatique.
- **Les fonctions principales d’un SE** : interface utilisateur, communication avec les périphériques, gestion de la mémoire, contrôle des ressources et multitâche, mise en réseau, accès aux disques et gestion des données, sécurité.
- **Les types d’interfaces utilisateur** : interfaces utilisateur graphiques (GUI), interfaces en ligne de commande (CLI), interfaces en langage naturel (NLI), interfaces à base de menus (MBI).
- **Les périphériques** : tous les composants matériels du système informatique qui résident en dehors de l’unité centrale, tels que les claviers, écrans, souris, imprimantes, microphones, etc.
- **La gestion de la mémoire** : le processus par lequel le SE gère la façon dont la mémoire est utilisée par les applications et veille à ce qu’une application n’interfère pas avec la mémoire utilisée par une autre application.
- **Le contrôle des ressources et le multitâche** : le processus par lequel le SE alloue efficacement les ressources (telles que la mémoire et le temps de processeur) aux applications et leur permet de partager le temps de l’unité centrale afin d’atteindre leur objectif.
- **La mise en réseau** : le processus par lequel le SE gère les connexions et les interactions avec les réseaux d’autres systèmes informatiques afin de permettre le partage des ressources (telles que les fichiers et les imprimantes).
- **L’accès aux disques et la gestion des données** : le processus par lequel le SE accède aux données stockées en mémoire et sur les disques, qui sont organisées en fichiers, et coordonne le transfert des données des fichiers du disque vers la mémoire primaire et vice versa.
- **La sécurité** : le processus par lequel le SE protège le système informatique contre les menaces internes et externes, en fournissant une forme d’identité à l’utilisateur qui permettra son authentification.
- **Les exemples de SE** : Windows, Linux, MacOS / OSx.
- **Définition d’une application logicielle** : un programme ou un ensemble de programmes qui permet à un utilisateur de réaliser une tâche spécifique sur un système informatique.
- **Les types d’applications logicielles** : traitements de texte, feuilles de calcul, systèmes de gestion de bases de données (SGBD), clients de messagerie, navigateurs web, conception assistée par ordinateur (CAO), logiciels de traitement graphique.
- **Les caractéristiques communes des applications** : barres d’outils, menus, boîtes de dialogue, composants de l’interface graphique.

- **Représentation binaire** : C’est la façon dont les ordinateurs stockent les données en utilisant uniquement deux chiffres : 0 et 1. Chaque chiffre binaire, ou bit, est la plus petite unité de données en informatique. Un groupe de 8 bits est appelé un octet. Les bits et les octets peuvent être utilisés pour représenter des nombres, des caractères, des images, des sons, etc.
    - Exemple : Le nombre décimal 18 s’écrit 00010010 en binaire, et occupe un octet. Le caractère A s’écrit 01000001 en binaire, et occupe aussi un octet.
- **Système binaire** : C’est un système de numération qui utilise deux symboles : 0 et 1. On l’appelle aussi la numération base-2. Les nombres écrits en binaire se décomposent à l’aide des puissances de 2.
    - Exemple : Le nombre binaire 1101 se lit 1x2³ + 1x2² + 0x2¹ + 1x2⁰, et vaut 13 en décimal.
- **Conversion entre base binaire et base décimale** : C’est la méthode pour passer d’un système de numération à l’autre. Pour convertir un nombre décimal en binaire, on utilise l’algorithme d’Euclide et les restes successifs de la division euclidienne par 2. Pour convertir un nombre binaire en décimal, on utilise les puissances de 2.
    - Exemple : Pour convertir 43 en binaire, on fait les divisions suivantes : 43/2 = 21 reste 1, 21/2 = 10 reste 1, 10/2 = 5 reste 0, 5/2 = 2 reste 1, 2/2 = 1 reste 0. On écrit les restes du dernier au premier, et on obtient 101011. Pour convertir 10110 en décimal, on fait le calcul suivant : 1x2⁴ + 0x2³ + 1x2² + 1x2¹ + 0x2⁰, et on obtient 22.
- **Système hexadécimal** : C’est un système de numération qui utilise 16 symboles : 0123456789ABCDEF.
    - Exemple : Le nombre hexadécimal B2 se lit Bx16¹ + 2x16⁰, et vaut 178 en décimal. Le nombre décimal 49 s’écrit 31 en hexadécimal, car 49 = 3x16¹ + 1x16⁰.
- **Conversion entre base hexadécimale et base binaire** : C’est la méthode pour passer d’un système de numération à l’autre. Pour convertir un nombre hexadécimal en binaire, on fait correspondre un quartet (un groupe de 4 bits) à chaque chiffre hexadécimal. Pour convertir un nombre binaire en hexadécimal, on regroupe les bits par quartets, et on utilise la table de correspondance inverse.
    - Exemple : Pour convertir A1 en binaire, on utilise la table suivante : A = 1010, 1 = 0001. On obtient 10100001. Pour convertir 10110011 en hexadécimal, on regroupe les bits par 4 : 1011 0011. On utilise la table inverse : 1011 = B, 0011 = 3. On obtient B3.

- **Représentation binaire** : C’est la façon dont les systèmes informatiques représentent les données en utilisant uniquement deux valeurs possibles : 0 et 1. Ces deux valeurs sont appelées **bits** (binary digits). Pour représenter des données plus complexes, on utilise des séquences de bits de longueur variable. Par exemple, le nombre entier 13 peut être représenté par la séquence de bits 00001101.
- **Standards des formats de données** : Ce sont des conventions communes qui définissent comment les systèmes informatiques représentent et échangent les données. Il existe différents standards pour différents types de données, comme les nombres entiers, les caractères, les chaînes de caractères, les couleurs, etc. Ces standards permettent aux systèmes informatiques de communiquer et d’interpréter les données de façon cohérente et efficace. Par exemple, le standard ASCII (American Standard Code for Information Interchange) définit comment les caractères sont représentés par des séquences de 8 bits. Ainsi, le caractère “A” est représenté par la séquence 01000001.
- **Représentation de quelques types de données** : Le document PDF donne des exemples de représentation de quatre types de données : les nombres entiers, les caractères, les chaînes de caractères et les couleurs. Voici un résumé de ces exemples :
    - Les nombres entiers sont représentés par des séquences de bits de longueur variable, généralement 8 bits (un octet). Le nombre de représentations distinctes possibles dépend du nombre de bits utilisés. Par exemple, avec 8 bits, on peut représenter 256 nombres différents, de 0 à 255.
    - Les caractères sont représentés par des séquences de 8 bits selon le standard ASCII. Chaque caractère correspond à un code numérique unique. Par exemple, le caractère “B” correspond au code 66, qui est représenté par la séquence 01000010.
    - Les chaînes de caractères sont des concaténations de caractères. Elles sont représentées par des séquences de bits qui suivent l’ordre des caractères. Chaque mot comprend environ 16 à 32 bits. Par exemple, le mot “bonjour” est représenté par la séquence 01100010 01101111 01101110 01101010 01101111 01110101 01110010.
    - Les couleurs sont représentées dans le système numérique hexadécimal, qui utilise 16 symboles (0 à 9 et A à F) pour représenter les valeurs de 0 à 15. Chaque couleur est représentée par 6 valeurs hexadécimales, 2 pour chaque couleur primaire (rouge, vert, bleu). Par exemple, la couleur rouge est représentée par FF0000. Lorsqu’elle est visualisée sur un écran, la valeur est généralement précédée d’un dièse (#FF0000). Un maximum d’environ 16,8 millions de couleurs différentes peut être saisi (16 à la puissance 6 ou 2 à la puissance 24).

- **Le type de données booléen et la logique booléenne** : Le type de données booléen est un type de données qui a deux valeurs, true (vrai) ou false (faux), qui représentent les valeurs de vérité de la logique et de l’algèbre de Boole. La logique booléenne est un système algébrique qui permet de manipuler les valeurs booléennes à l’aide d’opérateurs booléens. Le type de données booléen est utilisé dans les instructions conditionnelles et les circuits logiques des ordinateurs.
- **Les opérateurs booléens / Portes logiques** : Il existe six opérateurs booléens : AND (ET), OR (OU), NOT (NON), NAND (NON-ET), NOR (NON-OU) et XOR (OU-EXCLUSIF). Chaque opérateur booléen a une ou deux entrées et une sortie, qui sont toutes des valeurs booléennes. Chaque opérateur booléen peut être représenté par un symbole, une table de vérité ou un diagramme logique. Une table de vérité montre toutes les combinaisons possibles des entrées et la sortie correspondante. Un diagramme logique montre le fonctionnement du circuit électrique associé à l’opérateur. Une porte logique est un composant électronique qui implémente un opérateur booléen.
- **Les exemples d’applications possibles dans le monde réel** : Les opérateurs booléens peuvent être utilisés pour modéliser des situations réelles qui impliquent des conditions logiques. Par exemple :
    - AND : Alarme incendie : Fumée (1) ET chaleur 
    - OR : Lumière de voiture interne : L’une ou l’autre porte ouverte (1)
    - NOR : Climatisation : La climatisation ne se met en marche (1) que si les DEUX fenêtres A et B sont fermées.
    - XOR : 2 interrupteurs d’éclairage dans un couloir
- **Le passage d’une expression logique à une table de vérité ou à un diagramme logique** : Une expression logique est une combinaison d’opérateurs booléens et de variables booléennes. Pour passer d’une expression logique à une table de vérité, il faut énumérer toutes les valeurs possibles des variables et calculer la valeur de l’expression pour chaque cas. Pour passer d’une expression logique à un diagramme logique, il faut représenter chaque opérateur booléen par sa porte logique correspondante et connecter les entrées et les sorties selon l’ordre des opérations.