# CLAUDE.md — Gîte La Bataillère

## Règles absolues

- **Single-file** : tout le code vit dans `index.html`. Ne pas créer de fichiers JS/CSS séparés.
- **Pas de framework** : vanilla HTML/CSS/JS uniquement, pas de build step.
- **Langue** : toujours répondre en français.
- Après chaque modification d'`index.html`, synchroniser `gite-la-bataillere_2.html` (ou l'inverse).

## Propriétaire

Marie-Alix Lecerf · malixdlb@gmail.com · 06 58 41 76 65  
Adresse : 90 La Bataillère, 85440 Poiroux (Vendée)  
Label : Gîtes de France 3 épis · 5 personnes max

## Repères dans le code

- **Formspree** : chercher `FORMSPREE_ENDPOINT` dans le `<script>`
- **Détection saison** : fonctions `detectSaison()` et `afficherSaison()` dans le `<script>`
- **SVG épis de blé** : `<defs>` juste après `<body>`, réutilisés via `<use href="#epi">`
- **Checkbox ménage** : wrapper `<div class="form-checkbox">` (pas `form-group`) — évite le bleeding du sélecteur `.form-group input`
- **Saison cachée Formspree** : `<input type="hidden" name="saison" id="saisonHidden">`
- **Fallback local** : `if (location.protocol === 'file:')` → `mailto:` au lieu de fetch

## Conventions CSS

- Variables : `--sage-dark #3d5e40`, `--sage-pale #e8f0e9`, `--sage-light`, `--gold #c9a96e`, `--text`
- Typos : Playfair Display (titres) + Jost (corps)
- Breakpoint mobile : 900px
- Icônes SVG : viewBox 24×24, `stroke-width: 1.5`, `stroke-linecap: round`, pas de fill

## Saisons et tarifs

| Saison | Période | Tarif |
|---|---|---|
| Haute saison | 27 juin → 28 août | 700 €/sem. |
| Moyenne saison | 9 juin → 26 juin + 29 août → 15 nov. | 450 €/sem. |

Réservations samedi → samedi uniquement.

## Déploiement

GitHub Pages : `main` → `index.html` à la racine.  
URL : https://jean-chevillardd.github.io/gite-la-bataillere/
