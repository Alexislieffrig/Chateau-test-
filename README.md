# Info-F-101 : Projet d’Informatique castle_quest
![Tuf, the Linux mascot](https://fundit.fr/sites/default/files/actors/1456-universite-libre-bruxelles-ulb.jpg)

## Présentation générale:


![plateau de jeu](../../../../PRO_PR~1/AppData/Local/Temp/video_jeu.gif)

Ce projet, si vous le menez jusqu’au bout, va vous faire programmer un petit jeu du type jeu d’évasion (escape game) dans lequel le joueur commande au clavier les déplacements d’un personnage au sein d’un « château » représenté en plan. Le château est constitué de cases vides (pièces, couloirs), de murs, de portes, que le personnage ne pourra franchir qu’en répondant à des questions, d’objets à ramasser, qui l’aideront à trouver les réponses à ces questions et de la case de sortie / quête du château. Le but du jeu est d’atteindre cette dernière.

Le programme utilisera le module turtle comme interface graphique et comportera deux parties principales :

le tracé du plan du château,

la gestion du jeu sur le plan tracé (gestion des déplacements du personnage au sein du château, affichage des objets recueillis, gestion de l’ouverture des portes).

Les données nécessaires (plan du château, objets, portes) sont encodées dans 3 fichiers texte. Vous disposerez d’un jeu de fichiers de données que nous vous proposons et devrez réaliser un programme de jeu qui met en œuvre ces données. Vous pourrez ensuite si vous le souhaitez encoder votre propre château en préparant d’autres fichiers de données, qui tourneront avec le même programme. Votre château pourra aussi bien être du type labyrinthe (entièrement fait de couloirs étroits, sans portes) que du type escape game (un ensemble de pièces, entre lesquelles un personnage circule pour rassembler des objets lui permettant de répondre à des questions ou résoudre des énigmes).

Ce projet vous permettra d’écrire un code plus substantiel que ce que nous vous demandons ailleurs dans le cours, et va vous demander de manipuler de nombreux concepts vus tout au long du cours.

##NIVEAUX DE PROJET
Dans le cadre de ce projet, 4 niveaux de jeux peuvent être réalisés correspondant à des difficultés croissantes :

- Niveau 1 : 

construction et affichage du plan du château. Ce niveau consiste à tracer correctement le plan du château à partir du fichier de données. La gestion du jeu après affichage du plan ne fait pas partie de ce niveau.

- Niveau 2 : 

en plus du niveau 1, la gestion des déplacements au clavier, sans portes ni objets à ramasser. Ce niveau consiste à gérer les déplacements d’un personnage dans le plan construit au niveau 1. Ici on suppose qu’aucun objet ni porte n’est présent dans le plan : leur gestion n’est pas prise en compte.

On déplace le personnage de case en case à l’aide des 4 flèches du clavier.

Le personnage ne doit pas pouvoir traverser les murs ni sortir du plan.

Si le personnage arrive sur la case quête / sortie du château, un message lui annonce qu’il a gagné.

Option non demandée, si vous voulez aller plus loin : les cases déjà parcourues par le personnage peuvent être affichées dans une couleur spécifique, de façon à ce que la trace de son parcours soit conservée.

- Niveau 3 : 

niveaux 1 + 2 + gestion des objets à ramasser. Dans ce niveau, il y a dans le labyrinthe des objets que le joueur doit collecter. Outre le fichier contenant le plan, un second fichier de données contient la liste des objets et la case où chaque objet se trouve.

Les cases où se trouve un objet doivent apparaître dans une couleur spécifique.

Lorsque le joueur se déplace sur une case contenant un objet, un message lui signale qu’il a trouvé un objet, et ce dernier s’ajoute à l’inventaire affiché en permanence à côté du plan. La case où était l’objet devient vide, puisque l’objet a été ramassé.

Option non demandée, si vous voulez aller plus loin : on peut prévoir que la sortie du labyrinthe ne sera accessible qu’une fois tous les objets rassemblés.

- Niveau 4 (escape game complet) : 

niveaux 1 + 2 + 3 + gestion des portes. Ce niveau consiste à ajouter dans la labyrinthe des portes que le joueur doit ouvrir en répondant à des questions. Le troisième fichier de données contient la liste des portes avec les questions et réponses associées.

Les cases où se trouve une porte doivent apparaître dans une couleur spécifique.

Lorsque le joueur tente d’accéder à une porte, la question associée lui est posée.

S’il répond correctement, la porte s’ouvre et il peut alors la franchir. La case de la porte apparaît alors comme une case vide.

S’il ne répond pas ou s’il donne une mauvaise réponse, la porte reste fermée et infranchissable.