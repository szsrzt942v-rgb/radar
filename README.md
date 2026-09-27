# Radar — ta veille mondiale sur téléphone

## Mettre l'appli en ligne (gratuit, environ 5 minutes)

1. Crée un compte sur https://github.com si tu n'en as pas.
2. Clique sur « New repository », nomme-le `radar`, coche « Public », puis « Create repository ».
3. Clique sur « uploading an existing file » et glisse **tous** les fichiers de ce dossier (index.html, sw.js, manifest.json et les trois icônes). Valide avec « Commit changes ».
4. Va dans **Settings > Pages**. Sous « Branch », choisis `main` puis `/ (root)` et clique sur « Save ».
5. Après une ou deux minutes, ton appli est disponible sur `https://TON-PSEUDO.github.io/radar/`.

## L'installer sur ton téléphone

- **iPhone (Safari)** : ouvre l'adresse, touche le bouton Partager, puis « Sur l'écran d'accueil ».
- **Android (Chrome)** : ouvre l'adresse, touche le menu ⋮, puis « Installer l'application » ou « Ajouter à l'écran d'accueil ».

L'appli s'ouvre alors en plein écran, comme une appli normale.

## Sources de données (toutes gratuites, sans clé)

| Module | Source | Actualisation |
|---|---|---|
| Séismes | USGS | 5 min |
| Catastrophes naturelles | NASA EONET | 15 min |
| Actualités | France 24, Le Monde, BBC, Al Jazeera (RSS) | 10 min |
| Conflits | GDELT + titres d'actualité | 15 min |
| Pétrole, gaz, or | TradingView | en continu |
| Cryptos | CoinGecko | 2 min |
| Devises et dinar | ExchangeRate-API | 1 h |
| Algérie | TSA Algérie, GDELT, USGS | 15 min |

Les flux RSS passent par un proxy public de secours (allorigins, corsproxy) quand le site d'origine bloque l'accès direct. Si un de ces proxys ferme, remplace-le dans `CONFIG.proxies` en haut du script d'`index.html`.

## Personnaliser

Tout se règle dans le bloc `CONFIG` en haut du script d'`index.html` : ajouter un flux RSS (par exemple El Watan ou l'APS), changer les cryptos suivies, les fréquences d'actualisation ou la zone des séismes. La liste `HOTSPOTS` définit les pays suivis pour l'indice de tension.

Après une modification, change `radar-v1` en `radar-v2` dans `sw.js` pour que les téléphones récupèrent la nouvelle version.
