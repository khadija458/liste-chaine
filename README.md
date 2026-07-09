# Listes Chaînées — Site Éducatif Java

Site web vitrine éducatif complet sur les listes chaînées en Java (simples et doublement chaînées), construit avec React, Vite et Tailwind CSS.

## 🚀 Stack Technique

- **Frontend** : React 18 + Vite
- **Styling** : Tailwind CSS
- **Routing** : React Router v6
- **Coloration syntaxique** : react-syntax-highlighter (Prism)
- **Déploiement** : Build statique (compatible Vercel/Netlify)

## 📋 Prérequis

- Node.js (v18 ou supérieur)
- npm ou yarn

## 🛠️ Installation

1. Installer les dépendances :
```bash
npm install
```

2. Lancer le serveur de développement :
```bash
npm run dev
```

Le site sera accessible à l'adresse `http://localhost:5173`

## 🏗️ Build pour la production

Pour créer une version optimisée du site :

```bash
npm run build
```

Les fichiers compilés seront dans le dossier `dist`.

Pour prévisualiser le build de production :

```bash
npm run preview
```

## 📁 Structure du projet

```
linked-list-course/
├── src/
│   ├── components/          # Composants réutilisables
│   │   ├── Navbar.jsx       # Barre de navigation
│   │   ├── ChapterLayout.jsx # Layout des chapitres
│   │   ├── VideoPlayer.jsx  # Lecteur vidéo
│   │   ├── CodeBlock.jsx    # Bloc de code avec coloration
│   │   ├── TipBox.jsx       # Encadré d'astuce
│   │   └── ComparisonTable.jsx # Tableau comparatif
│   ├── pages/               # Pages du site
│   │   ├── Home.jsx         # Page d'accueil
│   │   ├── Chapter1.jsx     # Chapitre 01
│   │   ├── Chapter2.jsx     # Chapitre 02
│   │   ├── Chapter3.jsx     # Chapitre 03
│   │   ├── Chapter4.jsx     # Chapitre 04
│   │   ├── Chapter5.jsx     # Chapitre 05
│   │   └── Conclusion.jsx   # Page conclusion
│   ├── data/
│   │   └── chapters.js      # Contenu des chapitres
│   ├── App.jsx              # Composant principal avec routing
│   ├── main.jsx             # Point d'entrée
│   └── index.css            # Styles globaux + Tailwind
├── index.html               # Template HTML
├── package.json             # Dépendances
├── vite.config.js           # Configuration Vite
├── tailwind.config.js       # Configuration Tailwind
└── postcss.config.js        # Configuration PostCSS
```

## 📚 Contenu du cours

Le site comprend 5 chapitres sur les listes chaînées en Java :

1. **Définition & Structure Mémoire** — Introduction aux listes chaînées
2. **Implémentation Java** — Code des classes Node et DNode
3. **Opérations Principales** — Insertion, suppression, recherche
4. **Comparaison avec ArrayList** — Quand choisir l'une ou l'autre
5. **Cas concret : Undo/Redo** — Application pratique avec Deque

## 🎨 Personnalisation

### Ajouter des vidéos

Pour ajouter des vidéos, modifiez le fichier `src/data/chapters.js` et remplacez les chaînes vides `videoUrl` par les URLs de vos vidéos :

```javascript
videoUrl: "https://votre-url-video.mp4" // ou YouTube embed
```

### Modifier les couleurs

Les couleurs sont configurées dans `tailwind.config.js`. Vous pouvez modifier la palette `primary` et `accent` selon vos préférences.

### Ajouter du contenu

Le contenu des chapitres est centralisé dans `src/data/chapters.js`. Vous pouvez modifier :
- Le texte HTML dans la propriété `content`
- Les blocs de code dans `codeBlocks`
- Les encadrés d'astuce dans `tip`
- Les tableaux comparatifs dans `comparisonTable`

## 🚢 Déploiement

Le site est prêt pour l'hébergement. Le dossier `dist` contient tous les fichiers nécessaires.

### Option 1 : Vercel (Recommandé)

**Via le site web :**
1. Créez un compte sur [vercel.com](https://vercel.com)
2. Cliquez sur "Add New Project"
3. Importez votre dépôt Git (GitHub, GitLab, Bitbucket)
4. Vercel détectera automatiquement la configuration (fichier `vercel.json`)
5. Cliquez sur "Deploy"

**Via CLI :**
```bash
npm i -g vercel
vercel
```

### Option 2 : Netlify

**Via le site web :**
1. Créez un compte sur [netlify.com](https://netlify.com)
2. Cliquez sur "Add new site" → "Deploy manually"
3. Glissez-déposez le dossier `dist` ou connectez votre dépôt Git
4. Netlify détectera automatiquement la configuration (fichier `netlify.toml`)

**Via CLI :**
```bash
npm i -g netlify-cli
netlify deploy --prod --dir=dist
```

### Option 3 : GitHub Pages

1. Créez un dépôt GitHub avec votre code
2. Allez dans Settings → Pages
3. Source : Deploy from a branch
4. Branch : main / master
5. Folder : dist
6. Ajoutez un workflow `.github/workflows/deploy.yml` si nécessaire

### Option 4 : Hébergement manuel

1. Lancez le build : `npm run build`
2. Uploadez le contenu du dossier `dist` sur votre hébergeur
3. Assurez-vous que le serveur redirige toutes les requêtes vers `index.html` (pour React Router)

### Vérification avant déploiement

Le dossier `dist` doit contenir :
- `index.html`
- `assets/` (CSS, JS, et vidéos)
- `assets/video/` (7 fichiers vidéo)

Vérifiez avec :
```bash
npm run build
npm run preview
```

## 📝 Notes

- Le site est 100% statique, aucun backend n'est requis
- Les vidéos utilisent un placeholder par défaut si l'URL n'est pas fournie
- Le design est responsive (mobile, tablette, desktop)
- La navigation inclut une barre de progression par chapitre

## 🤝 Contribution

Ce projet est un site éducatif. N'hésitez pas à adapter le contenu selon vos besoins pédagogiques.
