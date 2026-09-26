# Révis GEII

Application web de révision pour le BUT GEII : matières organisées par semestre et onglets personnalisables (onglet « Gérer »), cours, fiches avec formules (LaTeX), cartes de révision, QCM, exercices extraits ou générés, et estimation du temps de travail restant.

Tout tourne dans le navigateur (un seul fichier `index.html`, aucun serveur). L'IA passe par ta propre clé API [Groq](https://console.groq.com/keys) (gratuite).

## Utiliser

**En local** : ouvre `index.html` dans Chrome, Firefox ou Edge.

**En ligne avec GitHub Pages** :
1. Crée un dépôt GitHub et envoie-y ces fichiers.
2. Va dans *Settings → Pages*.
3. Sous *Build and deployment*, choisis *Deploy from a branch*, la branche `main` et le dossier `/ (root)`, puis *Save*.
4. Au bout d'une minute, le site est disponible sur `https://TON-PSEUDO.github.io/NOM-DU-DEPOT/`.

## Première utilisation

1. Ouvre l'onglet **Réglages** et colle ta clé Groq.
2. Ouvre une matière, colle ton cours dans **Cours**.
3. Génère fiches, cartes, QCM et exercices.

## Sur mobile

Depuis Safari (iPhone/iPad) ou Chrome (Android), utilise « Ajouter à l'écran d'accueil » : une icône Révis GEII apparaît comme une vraie application. Ça fonctionne aussi bien en ouvrant `index.html` en local qu'en passant par GitHub Pages ; l'icône est déjà intégrée, rien à configurer.

## Plusieurs clés API

Dans Réglages, ajoute autant de clés Groq que tu veux (les tiennes, ou prêtées par des camarades). L'appli affiche, pour chaque clé, une estimation des tokens qu'il lui reste (donnée renvoyée par Groq après chaque utilisation) et choisit automatiquement celle qui en a le plus, avant même de tomber en erreur. Si une clé est épuisée ou invalide, elle passe à la suivante toute seule.

## Importer des documents scannés ou manuscrits

Dans l'onglet Cours, « Importer » accepte aussi des photos (.png, .jpg, .webp) et des PDF scannés, en plus du texte. Un document sans texte numérique (photo de notes, PDF scanné) est automatiquement lu par un modèle d'IA capable de déchiffrer de l'écriture manuscrite. Le menu à côté du bouton Importer permet de choisir : tout garder, retirer l'écriture manuscrite (ne garder que l'imprimé), ou l'inverse. C'est un modèle « aperçu » chez Groq : la lecture est utile mais pas parfaite sur une écriture peu lisible — relis toujours le résultat. Nécessite une clé API.

## Vie privée

- Tes cours et résultats sont enregistrés dans le navigateur (`localStorage`), jamais dans le dépôt.
- La clé API reste dans ton navigateur et n'est envoyée qu'à Groq. Ne l'écris jamais dans le code.
- Utilise *Réglages → Exporter une sauvegarde* pour ne rien perdre (la sauvegarde ne contient pas la clé).
