# 🔥 Flo Tracker

Application personnelle de suivi fitness — HTML standalone, 100% offline.

# Lien Direct
https://flodus.github.io/tracker/flo-tracker.html

## C'est quoi

Tracker de remise en forme démarré le 1er juin 2026. Programme HIIT + Challenge 100 pompes.  
Une seule page HTML, aucune dépendance serveur, tout est stocké en localStorage.

## Programme

| Jour | Séance |
|------|--------|
| Lundi | HIIT 15-20 min |
| Mardi | Challenge 100 pompes |
| Mercredi | Repos |
| Jeudi | Challenge 100 pompes |
| Vendredi | HIIT 15-20 min |
| Samedi | Challenge 100 pompes |
| Dimanche | Repos |

## Fonctionnalités

- **Onglet Aujourd'hui** — module HIIT (YouTube ou timer) + module pompes avec timer de repos, compteur série par série, S5 MAX libre
- **Onglet Pesées** — graphique double (poids + % MG) avec zones cibles, historique
- **Onglet Séances** — historique détaillé + tableaux de référence des programmes
- **Onglet Recap** — streak, calendrier mensuel, objectifs, journal

## Challenge 100 pompes

3 niveaux (11-20 / 21-25 / 26-30 pompes), 2 semaines par niveau, 3 jours par semaine.  
Si le total minimum n'est pas atteint, la séance est à refaire.  
S5 = MAX : la cible est un minimum, on note le vrai chiffre réalisé.

## Objectifs

- 🎪 Festival avec Louise — 17 juillet 2026
- 💛 Rencontre Aurélie — 4 août 2026

## Utilisation

### En local
Ouvrir `flo-tracker.html` directement dans le navigateur.

### Comme appli Android (PWA)
1. Ouvrir l'URL GitHub Pages dans Chrome : `https://[username].github.io/[repo]/flo-tracker.html`
2. Menu ⋮ → **Ajouter à l'écran d'accueil**
3. L'appli s'installe et fonctionne offline

## Technique

- Fichier unique `flo-tracker.html` — HTML + CSS + JS inline
- `localStorage` key : `flo_tracker` (jamais versionnée)
- Données de référence hardcodées (HC_SESSIONS / HC_WEIGHINGS) — priorité absolue sur localStorage pour les dates concernées
- PWA : manifest inline + service worker blob — pas de fichiers séparés nécessaires
- Aucune dépendance externe sauf Google Fonts (Inter + Bebas Neue)
