# Les chats attrapent les souris

Jeu type Snake dans le navigateur : un chat (🐱) doit attraper des souris (🐭). Projet de formation, à usage personnel et pédagogique.

## Lancer le jeu

Ouvrir le fichier [index.html](index.html) directement dans un navigateur desktop. Il n'y a ni serveur, ni build, ni dépendance à installer.

## Comment jouer

- Les flèches du clavier déplacent le chat. Le premier appui lance la partie.
- Chaque souris attrapée fait grandir le chat et ajoute 1 au score.
- Une nouvelle souris apparaît aussitôt, pour garder un nombre constant de souris sur le terrain.
- La vitesse augmente à mesure que le score progresse.
- La partie se termine si le chat touche un bord du terrain ou son propre corps. Le score final s'affiche.
- Appuyer sur Entrée ou Espace pour rejouer après une défaite.

## Configuration

Les constantes sont en haut du script, dans [index.html](index.html) :

- `CELLS` : taille de la grille (20 cases par côté).
- `SIZE` : taille d'une case en pixels.
- `MICE` : nombre de souris présentes simultanément (3).

La vitesse est calculée par la fonction `speed()` : plus le score est élevé, plus le délai entre deux déplacements diminue, avec une limite basse.

## Structure du dépôt

- [index.html](index.html) : le jeu complet (HTML, CSS et JavaScript inline, sans framework).
- [brief.md](brief.md) et [brief-clarified.md](brief-clarified.md) : cahier des charges et précisions.
- [evolutions/](evolutions/) : demandes d'évolution, dont la publication sur GitHub Pages.
- [AGENTS.md](AGENTS.md) : guide de projet pour l'assistant de code.

## Tests

Il n'existe pas de suite de tests automatisés. Les vérifications sont manuelles : lancer le jeu dans le navigateur, vérifier les déplacements, la capture des souris, la fin de partie et le redémarrage.

## Publication

Le dépôt est publié sur GitHub : [github-stag6/tetris](https://github.com/github-stag6/tetris). La publication du jeu sur GitHub Pages est prévue dans [evolutions/01-déploiement.md](evolutions/01-déploiement.md) et n'est pas encore activée.
