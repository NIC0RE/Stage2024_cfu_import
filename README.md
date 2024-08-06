# Stage2024_cfu_import
Le travail que j'ai effectué dans le cadre de mon stage de fin d'année de licence au sein de l'entreprise Median Technologies.

# CFU IMPORT

Cet ensemble de programmes python a pour objectif final de remplacer ou d'accompagner l'utilisation du process 'Synthesis'

## Pour les utilisateurs
Le programme peut être lancé automatiquement à partir du fichier cfu_import_all. 

Un système de journalisation a été mis en place pour garder une trace des évènements, et des potentielles erreurs.
Les Logs (journaux) indiquent les différentes étapes du programmes, et précise lorsqu'un fichier est créé, ou à l'inverse, si la création a échoué.
La journalisation est facile à distinguer: à chaque lancement du programme, une séparation se fait.

Les erreurs sont apparentes (en rouge) et assez claires pour être cernée facilement. 
Dans la majorité des cas, une erreur ne cause pas l'arrêt du programme, mais plutôt indique une défaillance liée à un fichier ou une donnée traitée.
Si l'erreur semble venir directement du programme, alors mieux vaut contacter une personne en mesure d'y accéder sans pertuber le déroulement de l'execution.

L'emplacement des documents générés par le programme est indiqué dans les logs. En général, les fichiers pertinents se trouvent dans le répertoire 'test/working'
Les dossiers relatifs à python ainsi que les fichiers du dossier 'test/data' ne doivent pas être modifiés ou supprimer, auquel cas le programme ne sera plus en mesure d'accéder aux données.

## Pour les developpeurs
Le programme est accompagné de fichier de tests simples. Ces tests sont suffisant pour vérifier les scénarios basiques mais peuvent largement être améliorer.

Un système de journalisation a été mis en place pour garder une trace des évènements, et des potentielels erreurs.
Les Logs (journaux) indiquent les différentes étapes du programmes, et précise lorsqu'un fichier est créé, ou à l'inverse, si la création a échoué.
La journalisation est facile à distinguer: à chaque lancement du programme, une séparation se fait.

Les logs sont par défaut réglés pour n'afficher que les messages d'importance moindre (.info) mais permettent d'afficher également les erreurs s'il y en a.
Il est possible de changer le mode d'affichage en déboggage (.debug) depuis le fichier cfu_import.py pour disposer d'une plus grande précision dans les messages
et obtenir des information relatives au code directement.

Le fichier test/data/cfu_index.py contient la liste des fichiers excel à traiter. La modification n'est conseillée que lors d'une mise à jour des données importante.
La modification des fichiers eux-même est prise en compte au lancement du programme. 
