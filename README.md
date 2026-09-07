# WinterHaven — site vitrine

Personnalisation du site vitrine de **WinterHaven, Superyacht Marine Centre**,
un projet de centre de maintenance et de mise à sec pour superyachts situé en
Comunitat Valenciana (Méditerranée occidentale). Le dépôt contient la feuille de
style d'habillage injectée dans le site Squarespace et les visuels éditoriaux
(rendus 3D, schémas, logos partenaires) utilisés dans les pages.

**Année de réalisation / livraison : 2018–2019.** D'après les identifiants
Squarespace des pages (`#collection-5c24…`) et des images
(`static/5c2386a24cde7a0c1a74561a/…/15459…`), datés de fin décembre 2018 ; la
feuille de route présentée sur le site court de 2019 à 2022–2025.

## Contenu

- `styles.less` — feuille de style d'habillage, à coller dans le panneau *Custom
  CSS* de Squarespace. Règles globales (typographie, titres, listes, boutons,
  formulaires) puis ajustements par page, ciblés par identifiant de collection et
  de bloc.
- `images/` — visuels éditoriaux du site :
  - `logo.png` — logo WinterHaven.
  - `home-banner.jpg`, `home-winterhaven.jpg`, `home-port.jpg`, `intro-banner.png`,
    `intro-banner-2.jpg`, `facilities-port.png` — rendus 3D du site (bannières et
    illustrations pleine largeur).
  - `home-concept.png`, `home-build.png`, `home-deliver.png`, `home-schema.png` —
    pictogrammes et schéma « new concept » de la page d'accueil.
  - `crew-academy.png`, `crew-gym.png`, `crew-lounge.png`, `crew-playground.png` —
    pictogrammes des services équipage.
  - `roadmap-2019.png`, `roadmap-2020.png`, `roadmap-2021.png`,
    `roadmap-2022-2025.png`, `roadmap-phases.png` — jalons et phases de la feuille
    de route.
  - `location-map.png`, `location-background.png`, `location-comunitat-valenciana.png`,
    `location-lonely-planet.png`, `location-viator.png`, `location-visitacity.png`,
    `location-more-info.png` — carte de situation et logos de la page *Location*.
  - `after-title.png`, `before-list.png`, `before-list-2.png` — ornements
    typographiques appelés en `background-image` depuis `styles.less`.
- `_Documents/Maquette_Website_WH_V5.afphoto` — maquette du site sous Affinity
  Photo (non suivie par git, voir `.gitignore`).

## Stack technique

- Site hébergé et édité sur **Squarespace** (template de la famille Brine :
  classes `tweak-…`, `Header--bottom`, `Index-page`, `sqs-block-…`).
- Habillage écrit en **LESS** (imbrication, échappement `~'calc(…)'`), collé dans
  l'éditeur *Custom CSS* de Squarespace qui le compile ; aucun outil de build
  dans le dépôt.
- Ciblage par identifiants Squarespace : `#collection-<id>` pour les pages
  (accueil, *WinterHaven at a glance*, *Location*, *Roadmap*), `#block-<id>` pour
  les blocs.
- Police **Brandon Grotesque** (`font-family: brandon-grotesque`), fournie par le
  service de polices de Squarespace / Adobe Fonts.
- Ornements servis depuis le CDN Squarespace du site
  (`static1.squarespace.com/static/5c2386a24cde7a0c1a74561a/…`).

## Développement

Prérequis : un accès éditeur au site Squarespace WinterHaven. Aucune chaîne
d'outils locale n'est nécessaire.

```sh
# Il n'y a pas d'installation ni de build.
# 1. Ouvrir Squarespace : Design → Custom CSS (ou Website → Website Tools → Custom CSS).
# 2. Coller le contenu de styles.less dans l'éditeur ; Squarespace le compile.
# 3. Téléverser les fichiers de images/ via les blocs correspondants des pages.
```

Notes de configuration :

- Les identifiants `#collection-…` et `#block-…` de `styles.less` sont propres à
  cette instance Squarespace ; ils changent si les pages ou les blocs sont
  recréés.
- Les URL d'ornements (`after-title.png`, `before-list.png`) pointent vers le CDN
  du site (`static/5c2386a24cde7a0c1a74561a/…`) : à re-téléverser et à mettre à
  jour dans `styles.less` en cas de migration.
- `html { font-size: 15px }` fixe la base des unités `rem` utilisées partout dans
  la feuille.

## Crédits

- **Commanditaire** — WinterHaven, Superyacht Marine Centre
- **Développement** — Olivier Charvoz
- **Identité visuelle** — Big Company

Copyright © 2018–2019 WinterHaven. Tous droits réservés.
