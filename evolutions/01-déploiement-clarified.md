# Déploiement du jeu sur GitHub Pages

## Contexte

Le jeu (des chats qui mangent des souris, voir [brief-clarified.md](../brief-clarified.md)) existe déjà sous forme d'une page unique [index.html](../index.html), sans build ni dépendance d'exécution. L'objectif est de le partager avec des collègues, sans installation.

## Objectif

Publier le jeu sur GitHub Pages, accessible publiquement via l'URL GitHub Pages par défaut, afin qu'une petite équipe identifiée puisse y jouer depuis un navigateur.

## Périmètre fonctionnel

- Publication de la page `index.html` à la racine du dépôt comme source GitHub Pages.
- Accès public, sans authentification.
- Publication manuelle : pas de déploiement automatique à chaque modification.
- Pas de suivi d'usage autre que le compteur de visites GitHub.

## Hors périmètre

- Nom de domaine personnalisé.
- Déploiement automatique (CI/CD) à chaque push.
- Validation préalable par des collègues pilotes.
- Support mobile ou tactile : le jeu est destiné au desktop, contrôlé au clavier.
- Outil d'analyse externe (type Google Analytics).

## Utilisateurs cibles

Une petite équipe de collègues identifiée, qui joue au jeu depuis un navigateur desktop avec le clavier.

## Contraintes techniques

- Aucune étape de build ni dépendance d'exécution (contrainte du brief).
- Dépôt Git existant ; `node_modules/` déjà exclu du suivi.
- Exclusion de fichiers de la publication : à confirmer (voir points en suspens).

## Critères de succès

- Le lien GitHub Pages s'ouvre et le jeu démarre sans erreur dans le navigateur.

## Points en suspens

- Nettoyage du dépôt : la réponse « Git, node_modules exclu » doit être précisée (le dossier `.git` est-il exclu de la publication, ou seulement `node_modules/` ?). Pour GitHub Pages, `.git` n'est pas publié, mais le sens de la réponse reste à confirmer.
