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
Les dossiers relatifs à python ainsi que les fichiers du dossier 'test/data' ne doivent pas être modifiés ou supprimés, auquel cas le programme ne sera plus en mesure d'accéder aux données.

## Pour les developpeurs
Le programme est accompagné de fichier de tests simples. Ces tests sont suffisants pour vérifier les scénarios basiques mais peuvent largement être améliorés.

Un système de journalisation a été mis en place pour garder une trace des évènements, et des potentielels erreurs.
Les Logs (journaux) indiquent les différentes étapes du programmes, et précise lorsqu'un fichier est créé, ou à l'inverse, si la création a échoué.
La journalisation est facile à distinguer: à chaque lancement du programme, une séparation se fait.

Les logs sont par défaut réglés pour n'afficher que les messages d'importance moindre (.info) mais permettent d'afficher également les erreurs s'il y en a.
Il est possible de changer le mode d'affichage en déboggage (.debug) depuis le fichier cfu_import.py pour disposer d'une plus grande précision dans les messages
et obtenir des information relatives au code directement.

Le fichier test/data/cfu_index.py contient la liste des fichiers excel à traiter. La modification n'est conseillée que lors d'une mise à jour des données importante.
La modification des fichiers eux-même est prise en compte au lancement du programme. 

## Resultats

Une fois le programme complété, un message de ce type: 'start_all_cfu_extraction completed successfully' doit apparaître dans les logs.
Si un message indique le contraire, une erreur gênante est probablement survenue et cela signifie que le programme s'est terminé de manière inattendue.


Parmis les fichiers générés à l'issue du programme, on trouve:
- Un fichier de diagnostic qui liste l'ensemble des fichiers traités, s'ils ont pu être trouvé, analysé, et sinon pour quelle raison. Les erreurs précises sont inscrites dans la colonne adaptée, accompagnées d'un texte explicatif. Les erreurs ne concerne pas toujours le code en lui-même, mais souvent une erreur ou un oubli dans le fichier traité. Si cela est possible, modifier le fichier en conséquence permettra (sans doute) de corriger l'erreur.
- Un fichier de données globales dans lequel on trouve l'intégralité des données des fichiers qui ont pu être traités. Les données ne sont pas brutes, mais on y retrouve les colonnes les plus importantes. Les données ne sont pas spécialement triées de base.
- Deux fichiers de statistiques: le premier donne des informations rapides sur le traitement des fichiers (nombre de projets à analyser, combien ont été traités, valeurs en pourcentage, colonne manquantes, errreurs communes...); Le second restitue les données de manière organisée, et affiche les totaux de quantité, de revenus, par mois notamment. 
