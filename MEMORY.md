# MEMORY.md — Notes et décisions projet

## Décisions techniques prises

### Formulaire
- Formspree pour l'envoi réel (nécessite hébergement HTTP)
- Fallback `mailto:` automatique quand ouvert en `file://` (test local)
- Validation JS : dates samedi uniquement (`getDay() === 6`) avec trick UTC `'T12:00:00'`
- Saison auto-détectée depuis la date d'arrivée, transmise à Formspree via champ caché

### Icônes
- Tous les emoji remplacés par des SVG inline (stroke-width 1.5, stroke-linecap round, 24×24)
- Épis de blé : définis une fois dans `<defs id="epi">`, réutilisés via `<use href="#epi">`

### Checkbox ménage
- Wrapper retiré de la classe `form-group` pour éviter que `.form-group input { appearance:none; width:100% }` ne s'applique à la checkbox
- Styles checkbox avec `!important` + `appearance: auto; -webkit-appearance: checkbox`

### Carte
- Google Maps embed via `maps.google.com/maps?q=...&output=embed` (pas d'API key requise)

## À faire

- [ ] Intégrer les vraies photos de Marie-Alix (galerie + sections équipements)
- [ ] Vérifier les URLs des photos d'activités (certaines peuvent être en 404)
- [ ] Optionnel : calendrier de disponibilités (iCal ou tableau visuel)
- [ ] Optionnel : domaine personnalisé (ex: gite-la-bataillere.fr) via GitHub Pages

## Historique des modifications notables

- Validation samedi→samedi (suppression de la vérification 14 nuits)
- Remplacement OSM → Google Maps embed
- Remplacement dropdown saison → bannière auto-détection
- Déploiement GitHub Pages : https://jean-chevillardd.github.io/gite-la-bataillere/
