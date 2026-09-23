# 🔥 Flo Tracker

Application personnelle de suivi fitness — HTML standalone, 100% offline.

## Lien direct

https://flodus.github.io/tracker/flo-tracker.html

## C'est quoi

Un tracker de remise en forme personnel. Une seule page HTML, aucune dépendance serveur, tout est stocké en localStorage.

## Fonctionnalités

- **Écran de démarrage** — configuration du programme : date de début, pesée du jour, objectif poids/MG avec date cible
- **Onglet Aujourd'hui** — module HIIT (YouTube ou timer) + module pompes avec timer de repos, compteur série par série, S5 MAX libre ; messages de motivation selon l'avancement
- **Onglet Pesées** — graphique double (poids + % MG) avec zones cibles, courbe de tendance, projection vers l'objectif, historique
- **Onglet Séances** — historique détaillé + tableaux de référence des programmes
- **Onglet Recap** — stats, calendrier mensuel (jours avant le début grisés), objectifs, journal, compteur jours sans alcool, export/import CSV

## Programme par défaut

| Jour | Séance |
|------|--------|
| Lundi | HIIT 15-20 min |
| Mardi | Challenge 100 pompes |
| Mercredi | Repos |
| Jeudi | Challenge 100 pompes |
| Vendredi | HIIT 15-20 min |
| Samedi | Challenge 100 pompes |
| Dimanche | Repos |

## Challenge 100 pompes

3 niveaux (11-20 / 21-25 / 26-30 pompes), 2 semaines par niveau, 3 jours par semaine.  
Si le total minimum n'est pas atteint, la séance est à refaire.  
S5 = MAX : la cible est un minimum, on note le vrai chiffre réalisé.

## Objectifs

Configurables au démarrage ou depuis l'onglet Recap → Objectifs.  
Poids cible + % MG cible + date cible → courbe de projection visible dans l'onglet Pesées.

## Synchronisation PC ↔ téléphone

Les données sont locales à chaque appareil (localStorage). Pour synchroniser :

1. **Recap → Stats → Exporter CSV** sur l'appareil source
2. **Recap → Stats → Importer CSV** sur l'appareil destination

Les doublons sont ignorés automatiquement.

## Installation comme appli Android (PWA)

1. Ouvrir l'URL dans Chrome : `https://flodus.github.io/tracker/flo-tracker.html`
2. Menu ⋮ → **Ajouter à l'écran d'accueil**
3. L'appli s'installe et fonctionne offline

## Technique

- Fichier unique `flo-tracker.html` — HTML + CSS + JS inline
- `localStorage` key : `flo_tracker` (jamais versionnée)
- Données de référence hardcodées (`HC_SESSIONS` / `HC_WEIGHINGS`) — priorité absolue sur localStorage pour les dates concernées
- PWA : manifest inline + service worker blob — pas de fichiers séparés nécessaires
- Aucune dépendance externe sauf Google Fonts (Inter + Bebas Neue)
