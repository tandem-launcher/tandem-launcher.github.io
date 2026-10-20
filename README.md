# Site Tandem

Site vitrine indépendant, en français, sans compilation ni dépendance JavaScript. Les fichiers servis sont dans `dist/`.

Prévisualisation : `node serve.mjs`, puis ouvrir http://127.0.0.1:4178.

Le téléchargement pointe vers la dernière publication GitHub (`releases/latest`).

Les captures de `dist/assets/shots/` sont de vraies captures de l'interface de Tandem, prises sur l'aperçu de développement (données d'exemple). L'icône `dist/assets/icon.png` est celle de l'application.

Le paysage original est dessiné en Canvas et le bouton « Changer d’horizon » génère une nouvelle composition. Les polices Geist et Jersey 10 sont embarquées ; voir leurs licences dans `dist/assets/`.

## Mise en ligne

GitHub Pages, par l'action `.github/workflows/pages.yml` (publie `dist/` à chaque push sur `main`). Rien n'est publié tant que la variable du dépôt `SITE_LIVE` ne vaut pas `true` :

```bash
gh variable set SITE_LIVE --body true --repo RandomZeleff/RandomZeleff.github.io
gh workflow run pages.yml --repo RandomZeleff/RandomZeleff.github.io
```
