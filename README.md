# helsens.ch — Site personnel

Site web statique de Clément Helsens, déployé sur GitHub Pages avec le domaine `helsens.ch`.

## Licence

- **Code source (HTML/CSS)** : MIT License — libre de réutilisation, voir [LICENSE](LICENSE)
- **Contenu éditorial (textes, projets, biographie)** : © 2026 Clément Helsens — tous droits réservés

## Structure

```
/
├── index.html        ← Page d'accueil (pitch + expertise + projets vedettes)
├── projects.html     ← Projets (Key4HEP, LiLiTTool, Drug Screen, Sports Platform)
├── about.html        ← CV & parcours
├── contact.html      ← Contact + formulaire d'étude de marché (Tally.so)
├── style.css         ← Styles partagés
├── CNAME             ← Domaine personnalisé (helsens.ch)
└── LICENSE           ← MIT (code) + tous droits réservés (contenu)
```

---

## Déploiement GitHub Pages

### Étape 1 — Créer le dépôt

1. Connectez-vous sur [github.com](https://github.com) avec le compte `clementhelsens`
2. **New repository** → nommez-le exactement `clementhelsens.github.io` (Public)
3. Ne cochez pas "Add README"

### Étape 2 — Pousser les fichiers

Depuis ce dossier :

```bash
git init
git add index.html projects.html about.html contact.html style.css CNAME LICENSE README.md
git commit -m "Initial commit — helsens.ch"
git remote add origin https://github.com/clementhelsens/clementhelsens.github.io.git
git branch -M main
git push -u origin main
```

### Étape 3 — Activer GitHub Pages

Settings → Pages → Source : **Deploy from a branch** → `main` / `/ (root)` → Save

→ Site disponible sur `https://clementhelsens.github.io` dans ~2 min.

---

## Domaine helsens.ch (Infomaniak)

### DNS chez Infomaniak

| Type  | Nom | Valeur                        |
|-------|-----|-------------------------------|
| A     | @   | 185.199.108.153               |
| A     | @   | 185.199.109.153               |
| A     | @   | 185.199.110.153               |
| A     | @   | 185.199.111.153               |
| CNAME | www | clementhelsens.github.io.     |

### GitHub Pages

Settings → Pages → Custom domain : `helsens.ch` → Save → cocher **Enforce HTTPS**

> La propagation DNS peut prendre 24–48h.

---

## Intégrer le formulaire Tally

1. Créez un compte sur [tally.so](https://tally.so) (gratuit)
2. Créez un formulaire avec ces questions :
   - Laboratoire / institution
   - Type de données collectées
   - Besoins principaux
   - Budget disponible
   - Délai souhaité
   - Email (optionnel)
3. **Share → Embed** → copiez l'ID du formulaire (ex : `wMXkbP`)
4. Ouvrez `contact.html`, remplacez `YOUR_FORM_ID`, décommentez le bloc `<iframe>`

---

## Mises à jour

```bash
# Modifiez vos fichiers, puis :
git add -A
git commit -m "Description de la modification"
git push
```

GitHub Pages redéploie automatiquement en ~30 secondes.

---

## À personnaliser

- `about.html` : titre de thèse, dates de formation, stats, lien CV PDF
- `about.html` : URL LinkedIn (vérifier `/in/clementhelsens`)
- `contact.html` : formulaire Tally (voir section ci-dessus)
- Toutes les pages : ajouter un favicon (`<link rel="icon" href="favicon.ico">`)
