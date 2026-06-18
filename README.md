# Mohamed Ben Rabah — Portfolio

> Full-stack developer portfolio · bilingual (EN / FR) · light & dark themes
> Portfolio de développeur full-stack · bilingue (EN / FR) · thèmes clair & sombre

🇬🇧 [English](#-english) · 🇫🇷 [Français](#-français)

---

## 🇬🇧 English

A single-page, responsive portfolio website built as a self-contained HTML component.
Content is fully separated into JSON files, with a built-in language switch (EN / FR)
and a light / dark theme toggle.

### ✨ Features

- **One-page site** — hero, about, work experience, tech stack, contact.
- **Bilingual** — English & French, toggled live from the navbar (`EN / FR`).
- **Light & dark themes** — toggled with the ☀ / ☾ button; preference is remembered.
- **Responsive** — adapts to mobile, tablet and desktop.
- **Content in JSON** — all text lives in `content.en.json` / `content.fr.json`, no need to touch the HTML.
- **Animated reveals & hover effects** — subtle, terminal-inspired visual style.

### 📁 Project structure

```
.
├── Portfolio.dc.html     # The website (markup + logic)
├── content.en.json       # All English content (text, experience, skills)
├── content.fr.json       # All French content
├── support.js            # Runtime required by the .dc.html file
└── assets/
    ├── mohamed.jpg                 # Profile photo
    └── Mohamed-Ben-Rabah-CV.pdf    # Downloadable résumé
```

> Keep every file in the same folder with this structure — the page loads the JSON
> files at runtime, so moving them will break the content.

### ▶️ Running the site

Because the page loads JSON files, it **cannot** be opened by double-clicking
(browsers block `file://` requests). Serve it through a local web server:

**Option 1 — VS Code Live Server (easiest)**
1. Open the folder in VS Code.
2. Install the **Live Server** extension.
3. Right-click `Portfolio.dc.html` → **Open with Live Server**.

**Option 2 — Python** (pre-installed on macOS / Linux)
```bash
python3 -m http.server 8000
# then open http://localhost:8000/Portfolio.dc.html
```

**Option 3 — Node.js**
```bash
npx serve
# then open the printed URL
```

### ✏️ Editing the content

All text is in **`content.en.json`** and **`content.fr.json`**. Both files share the
same structure, so edit them in pairs to keep the two languages in sync:

- `t` — labels, headings, bio paragraphs, buttons.
- `experiences` — your work history (one object per role): `company`, `tag`,
  `period`, `role`, `project`, `bullets`, `tech`.
- `skills` — skill groups: `label` + `items`.

To **add a project**, copy one object inside `experiences`, paste it at the top of
the array (most recent first) and edit its fields — in both JSON files.

### ⚙️ Defaults

In `Portfolio.dc.html`, the first line of the logic sets the defaults:

```js
state = { lang: 'en', theme: 'light', ready: false };
```

- `lang` → `'en'` or `'fr'` (default language)
- `theme` → `'light'` or `'dark'` (default theme)

### 🚀 Deploying

Drag the whole folder onto [Netlify Drop](https://app.netlify.com/drop) or deploy
with [Vercel](https://vercel.com). Renaming `Portfolio.dc.html` to `index.html`
makes the site load at the root URL.

---

## 🇫🇷 Français

Un portfolio responsive en une seule page, construit comme un composant HTML
autonome. Le contenu est entièrement séparé dans des fichiers JSON, avec un
sélecteur de langue intégré (EN / FR) et un basculement de thème clair / sombre.

### ✨ Fonctionnalités

- **Site une page** — hero, à propos, expériences, stack technique, contact.
- **Bilingue** — anglais & français, basculés en direct depuis la barre de navigation (`EN / FR`).
- **Thèmes clair & sombre** — bouton ☀ / ☾ ; la préférence est mémorisée.
- **Responsive** — s'adapte au mobile, à la tablette et au bureau.
- **Contenu en JSON** — tout le texte est dans `content.en.json` / `content.fr.json`, sans toucher au HTML.
- **Animations au défilement & effets au survol** — style visuel sobre inspiré du terminal.

### 📁 Structure du projet

```
.
├── Portfolio.dc.html     # Le site (balisage + logique)
├── content.en.json       # Tout le contenu anglais (textes, expériences, compétences)
├── content.fr.json       # Tout le contenu français
├── support.js            # Runtime nécessaire au fichier .dc.html
└── assets/
    ├── mohamed.jpg                 # Photo de profil
    └── Mohamed-Ben-Rabah-CV.pdf    # CV téléchargeable
```

> Garde tous les fichiers dans le même dossier avec cette structure — la page
> charge les fichiers JSON à l'exécution, les déplacer casserait le contenu.

### ▶️ Lancer le site

Comme la page charge des fichiers JSON, elle **ne peut pas** être ouverte par un
simple double-clic (les navigateurs bloquent les requêtes `file://`). Il faut la
servir via un serveur web local :

**Option 1 — Live Server de VS Code (le plus simple)**
1. Ouvre le dossier dans VS Code.
2. Installe l'extension **Live Server**.
3. Clic droit sur `Portfolio.dc.html` → **Open with Live Server**.

**Option 2 — Python** (préinstallé sur macOS / Linux)
```bash
python3 -m http.server 8000
# puis ouvre http://localhost:8000/Portfolio.dc.html
```

**Option 3 — Node.js**
```bash
npx serve
# puis ouvre l'URL affichée
```

### ✏️ Modifier le contenu

Tout le texte est dans **`content.en.json`** et **`content.fr.json`**. Les deux
fichiers ont la même structure : modifie-les par paire pour garder les deux langues
synchronisées :

- `t` — libellés, titres, paragraphes de bio, boutons.
- `experiences` — ton parcours (un objet par poste) : `company`, `tag`, `period`,
  `role`, `project`, `bullets`, `tech`.
- `skills` — groupes de compétences : `label` + `items`.

Pour **ajouter un projet**, copie un objet dans `experiences`, colle-le en haut du
tableau (le plus récent en premier) et modifie ses champs — dans les deux fichiers JSON.

### ⚙️ Valeurs par défaut

Dans `Portfolio.dc.html`, la première ligne de la logique définit les valeurs par défaut :

```js
state = { lang: 'en', theme: 'light', ready: false };
```

- `lang` → `'en'` ou `'fr'` (langue par défaut)
- `theme` → `'light'` ou `'dark'` (thème par défaut)

### 🚀 Déploiement

Glisse tout le dossier sur [Netlify Drop](https://app.netlify.com/drop) ou déploie
avec [Vercel](https://vercel.com). Renommer `Portfolio.dc.html` en `index.html`
permet d'afficher le site à la racine de l'URL.

---

© 2026 Mohamed Ben Rabah
