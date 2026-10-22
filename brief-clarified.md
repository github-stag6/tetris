# Jeu type Snake : les chats attrapent les souris

## Contexte

Projet de formation (usage personnel et pédagogique). L'idée reprend le principe du jeu Snake classique, avec un changement de thème : ce sont des chats qui doivent attraper des souris.

## Objectif

Livrer un jeu jouable dans un navigateur, en une seule page, qui reproduit la mécanique du Snake : un serpent contrôlé au clavier, qui grandit en consommant de la nourriture, et qui meurt en cas de collision.

## Périmètre fonctionnel

- Un chat (emoji 🐱) contrôlé par le joueur, qui se déplace sur une grille.
- Plusieurs souris (emoji 🐭) présentes simultanément sur le terrain, en nombre fixe.
- Capture : quand le chat atteint une souris, la souris est mangée et le chat grandit.
- Score : égal au nombre de souris attrapées.
- Accélération : la vitesse augmente au fur et à mesure que le score progresse.
- Fin de partie : condition à préciser (voir Points en suspens).
- Contrôles : flèches du clavier uniquement.

## Hors périmètre

- Version mobile et contrôles tactiles.
- Mode multijoueur.
- Sauvegarde des scores et classement.
- Tests automatisés (vérification manuelle uniquement).
- Hébergement en ligne (le jeu s'ouvre localement).

## Utilisateurs cibles

Le développeur lui-même, dans un cadre personnel ou pédagogique. Pas de public externe identifié.

## Contraintes techniques

- Stack : HTML, CSS et JavaScript pur, sans framework.
- Rendu : navigateur web sur desktop.
- Graphismes : emojis 🐱 et 🐭, pas de sprites ni d'images externes.
- Lancement : ouverture directe du fichier `index.html` dans le navigateur, sans serveur ni build.

## Critères de succès

- Le jeu se lance en ouvrant `index.html` dans un navigateur desktop, sans erreur console.
- Le chat se déplace avec les flèches du clavier.
- Le chat grandit à chaque souris attrapée, et le score s'incrémente de 1.
- Le nombre de souris présentes sur le terrain reste constant pendant la partie.
- La vitesse augmente à mesure que le score progresse.
- La partie se termine selon la condition retenue, et le score final est affiché.

## Points en suspens

- Condition de fin de partie : la réponse « Autre règle » a été choisie sans précision. Il faut définir la règle exacte (collisions avec les bords, avec le corps du chat, autre).
- Nombre exact de souris simultanées : « nombre fixe » retenu, mais la valeur reste à fixer.
- Courbe d'accélération : la vitesse croît avec le score, mais le rythme (linéaire, par paliers) reste à définir.
