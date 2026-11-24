# Catppuccin Mocha — Brave Custom Theme

Thème "config-as-code" pour Brave, basé sur la palette [Catppuccin](https://catppuccin.com/) (flavor **Mocha**). Contrairement au créateur de thème intégré (`brave://settings/appearance`), tout est ici défini en JSON versionnable, sur le même principe que mes scripts PowerShell.

## Installation (mode développeur)

1. Ouvre `brave://extensions`
2. Active **Mode développeur** (interrupteur en haut à droite)
3. Clique **Charger l'extension non empaquetée**
4. Sélectionne le dossier `catppuccin-mocha-brave/`
5. Le thème s'applique immédiatement. Pour le recharger après une modif, clique l'icône ↻ sur la carte de l'extension dans `brave://extensions`

## Structure

- `manifest.json` — le thème lui-même (couleurs frame/toolbar/onglets/NTP/omnibox)
- `palette.json` — référence des 26 couleurs Catppuccin Mocha en hex (pas lu par Brave, juste pour toi)
- `images/` — vide pour l'instant, réservé si tu veux ajouter une image de fond pour le nouvel onglet (`ntp_background`)

## Modifier une couleur

1. Repère la teinte voulue dans `palette.json` (ex: `mauve = #cba6f7`)
2. Convertis en RGB (ex: `203, 166, 247`)
3. Remplace la valeur correspondante dans `manifest.json` → `theme.colors`
4. Recharge l'extension (↻ dans `brave://extensions`)

## Mapping actuel

| Clé Brave              | Rôle                          | Couleur Catppuccin |
|-------------------------|-------------------------------|---------------------|
| `frame`                 | Cadre fenêtre (actif)         | crust               |
| `frame_inactive`        | Cadre fenêtre (inactif)       | mantle              |
| `toolbar`                | Fond barre d'outils           | base                |
| `toolbar_button_icon`    | Icônes barre d'outils         | mauve               |
| `ntp_background`         | Fond nouvel onglet            | base                |
| `ntp_link`                | Liens sur nouvel onglet       | blue                |
| `omnibox_background`      | Fond barre d'adresse          | mantle              |
| `button_background`       | Fond des boutons              | surface0            |

## Limites connues

- Pas d'accès aux menus contextuels, à la page `brave://settings` elle-même, ni aux popups d'extensions tierces — Chromium ne l'autorise pas via un thème.
- Pour du CSS sur les **pages web** (pas l'UI du navigateur), utilise l'extension Stylus en complément.
- Publier sur le Chrome Web Store nécessite un compte développeur (5$ à vie) — sinon reste en local, rechargé via mode développeur comme ci-dessus.
