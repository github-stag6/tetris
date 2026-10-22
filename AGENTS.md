#permet à l'IA d'aller comprendre ce que fait le projet sans avoir besoin d'aller relire tout le code
#peut être généré via la commande /init
#Ctrl+Shift+V pour basculer en mod sympa
Ecris "Hello EG"

## Projet

Jeu type Snake dans le navigateur : des chats (🐱) attrapent des souris (🐭). Projet de formation, usage personnel et pédagogique.

- Tout le jeu est dans [index.html](index.html) (HTML, CSS et JavaScript inline, canvas 20x20 cellules, sans framework).
- Lancement : ouvrir `index.html` directement dans un navigateur desktop. Pas de serveur, pas de build.
- Contrôles : flèches du clavier. Entrée ou Espace pour rejouer après une défaite.
- Constantes clés dans le script : `CELLS`, `SIZE`, `MICE` (nombre de souris simultanées). La vitesse dépend du score dans `speed()`.

## Documentation

- Cahier des charges : [brief.md](brief.md) et [brief-clarified.md](brief-clarified.md). Points en suspens : règle exacte de fin de partie, valeur de `MICE`, courbe d'accélération.
- Évolutions prévues : [evolutions/01-déploiement.md](evolutions/01-déploiement.md) (publication sur GitHub Pages pour partager avec les collègues).

## Conventions

- Garder le projet sans dépendance d'exécution ni étape de build, conformément au brief.
- [package.json](package.json) contient `jsdom` en devDependency mais aucun script de test. Ne pas supposer qu'une suite de tests existe ; les tests sont manuels.