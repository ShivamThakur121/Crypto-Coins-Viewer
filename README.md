# Crypto Coins Viewer (React + Redux Toolkit)

A tiny React app that fetches cryptocurrency data and displays it as neat cards. It uses Redux Toolkit + React-Redux under the hood with an async thunk to load the list.

> This repository contains the **production build** artifacts (`index.html` and a compiled JS bundle). You can host it anywhere that serves static files, including **GitHub Pages**.

## ✨ Features

- React UI that renders a grid of coin cards
- Global state with **Redux Toolkit** + **React-Redux**
- Async fetching via a thunk (e.g., `FetchData(99)`)
- Simple, responsive flex layout

## 🗂 Project structure

```
.
├── index.html               # App entry (mounts <div id="root">)
├── day16.43440575.js        # Compiled JS bundle (not in this repo example)
├── day16.43440575.js.map    # Source map (optional, for debugging)
├── README.md
├── LICENSE
└── .gitignore
```

> Note: Your compiled JS bundle name may differ (e.g., `day16.xxxxxxxx.js`). Make sure the `<script type="module" src="/day16.43440575.js">` path in `index.html` matches your actual file name.

## 🚀 Quick start (serve locally)

You can serve the static files with any HTTP server. Two easy options:

### Option A: Python
```bash
# From the repo root
python3 -m http.server 5173
# Open http://localhost:5173
```

### Option B: Node (serve)
```bash
# From the repo root
npx serve . -p 5173
# Open http://localhost:5173
```

## 🌐 Deploy to GitHub Pages

1. Create a new GitHub repository and push these files.
2. In GitHub: **Settings → Pages → Build and deployment**  
   - **Source:** Deploy from a branch  
   - **Branch:** `main` (or `master`) → `/ (root)` → **Save**
3. After it builds, your site will be live at the URL shown in the Pages panel.

### Important for GitHub Pages

- If your repo name is **not** your username.github.io, your site will be at:  
  `https://<username>.github.io/<repo>/`
- If your app makes API calls, ensure CORS is allowed and use **absolute URLs** (not relative to domain path).

## 🔧 Development notes

- The app renders a `<CoinCreate />` component that dispatches an async thunk on mount and maps the resulting `data` array into `<CoinCard />` components.
- Loading and error UI states are handled conditionally.
- Styling uses simple inline styles for a clean card grid.

## 📝 License

MIT — see [LICENSE](./LICENSE) for details.
