# Mouvement des souris

## Contexte

Le jeu [index.html](../index.html) est un Snake dans le navigateur où des chats attrapent des souris. Aujourd'hui les souris sont fixes sur le plateau. Cette évolution les rend mobiles pour que la partie devienne une chasse active.

## Objectif

Les souris se déplacent sur le plateau et fuient le chat. Le chat doit les poursuivre pour marquer des points.

## Périmètre fonctionnel

- Les souris se déplacent d'une case à la fois, dans les quatre directions (haut, bas, gauche, droite).
- Le déplacement a lieu une fois sur deux environ (à chaque tick de jeu sur deux).
- Le déplacement vise à fuir le chat.
- Les souris restent dans le plateau : les murs bloquent leur déplacement.
- Deux souris ne peuvent pas occuper la même case.
- Une souris ne peut pas traverser le chat.
- Une souris coincée par le chat est capturée par le chat.
- Une souris capturée est remplacée par une nouvelle souris, comme aujourd'hui.
- Le nombre de souris simultanées reste à `MICE` (3).
- Les règles de score ne changent pas : le score augmente uniquement avec les souris capturées.

## Hors périmètre

- Changement des règles de fin de partie.
- Changement de la logique de déplacement du chat.
- Multijoueur, sauvegarde ou nouvelles fonctionnalités de score.
- Tests automatisés : la validation reste manuelle dans le navigateur.

## Utilisateurs cibles

Joueurs du jeu sur navigateur desktop.

## Contraintes techniques

- Pas de dépendance d'exécution ni d'étape de build, conformément à [AGENTS.md](../AGENTS.md).
- Tout le code reste dans [index.html](../index.html).
- Les souris doivent être plus rapides que le chat. La vitesse du chat est actuellement fixée dans `speed()` ; le déplacement des souris doit être réglé séparément.

## Critères de succès

- Les souris se déplacent visiblement pendant la partie, une fois sur deux environ.
- Les souris fuient le chat.
- Les souris ne sortent jamais du plateau, ne se superposent pas et ne traversent pas le chat.
- Le score n'augmente que lorsqu'une souris est capturée.
- Une souris capturée est remplacée et le nombre de souris reste à 3.

## Points en suspens

- Valeur exacte de la vitesse des souris par rapport au chat (plus rapide, valeur à définir).
- Le comportement de fuite (choix de la case qui éloigne le plus du chat) est à préciser si le résultat ne convient pas.
