# 🍼 Tiny Bites — AI-Powered Baby & Toddler Meal Planner

A fully self-contained Progressive Web App (PWA) for planning meals for babies (6–12 months) and toddlers (1–3 years), powered by Claude AI.

**No app store. No server. No login required.** Just open the file in a browser and install it to your home screen.

---

## ✨ Features

- **55+ recipes** covering purees, finger foods, soups, pasta, meat, fish, vegetarian, and snacks
- **Claude AI integration** — connect your own Anthropic API key for personalised meal plans, recipe suggestions, and conversational nutrition help
- **Smart search & filters** — search by ingredient, filter by allergen and meal type in real time
- **AI recipe highlighting** — Claude's suggestions get highlighted with a ✨ badge in the recipe grid
- **Weekly meal planner** — auto-generated 7-day grid with one-click "Add all to shopping list"
- **Shopping list** — auto-populated from selected recipes, categorised by store section (Produce, Protein, Dairy, Grains, Pantry)
- **Export options** — Google Keep, iOS Reminders, plain text copy
- **Nutrition tracker** — calorie, carb, protein and fat averages vs age-appropriate targets
- **Preferences system** — favourite foods, disliked foods, meal type preferences and notes all feed into Claude's context
- **Dark mode** — follows system preference automatically
- **Works offline** — service worker caches the app after first load
- **Installable** — full PWA with manifest, icons, and install prompts for iOS and Android

---

## 🚀 Getting Started

### Option 1 — Open directly in browser
Download `index.html` and open it in any modern browser. That's it.

### Option 2 — Host on GitHub Pages (recommended)
1. Fork this repo
2. Go to **Settings → Pages**
3. Set source to **main branch / root**
4. Your app is live at `https://YOUR-USERNAME.github.io/tiny-bites`

### Option 3 — Host on Netlify (30 seconds)
1. Go to [netlify.com/drop](https://netlify.com/drop)
2. Drag and drop `index.html`
3. Get a live URL instantly — share it with anyone

---

## 🤖 Connecting Claude AI

1. Get a free API key at [console.anthropic.com](https://console.anthropic.com/settings/keys)
2. Open the app and tap **API key** in the sidebar
3. Paste your key and tap **Connect Claude**

Your key is stored only in your browser's local storage and sent directly to Anthropic's servers. It is never stored or transmitted anywhere else.

Once connected:
- The **Claude AI** page opens a full chat interface
- Quick-action prompts appear throughout the app (Weekly plan, Nutrition, recipe modals)
- All messages include your saved preferences as context automatically

---

## 📱 Installing on iOS (iPhone / iPad)

1. Open the app URL in **Safari** (must be Safari, not Chrome)
2. Tap the **Share button** ⬆️ at the bottom
3. Scroll down and tap **"Add to Home Screen"**
4. Tap **Add**

The app will appear on your home screen and launch full-screen, just like a native app. A one-time tip sheet guides you through this on first visit.

## 📱 Installing on Android

1. Open the app URL in **Chrome**
2. A green **"Install Tiny Bites"** banner appears at the bottom — tap **Install**
3. Or tap the **three-dot menu ⋮ → Add to Home screen**

---

## 🗂 Project Structure

```
tiny-bites/
├── index.html          # Complete self-contained PWA (all CSS, JS, data inline)
├── README.md           # This file
└── 404.html            # Redirect for GitHub Pages
```

This is intentionally a single-file app. Everything — styles, scripts, recipe data, service worker, and manifest — is embedded in `index.html` so it works when opened as a local file, shared via AirDrop/WhatsApp, or hosted on any static server.

---

## 🔧 Development

To split into a proper multi-file project:

```bash
git clone https://github.com/YOUR-USERNAME/tiny-bites
cd tiny-bites
claude  # Open in Claude Code
```

Then ask Claude Code to scaffold into separate `styles.css`, `app.js`, `recipes.js`, `sw.js` etc.

### Local development server

```bash
npx serve .
# or
python3 -m http.server 8080
```

> **Note:** The service worker requires either `localhost` or `https://` — it won't register over plain `http://` on a remote host.

---

## 🧑‍🍳 Recipe Coverage

| Category | Baby (6–12m) | Toddler (1–3y) |
|----------|-------------|----------------|
| Purees & firsts | ✓ 15 recipes | — |
| Finger foods | ✓ 5 recipes | — |
| Breakfast | ✓ 3 recipes | ✓ 7 recipes |
| Soups | ✓ 1 recipe | ✓ 3 recipes |
| Pasta | — | ✓ 3 recipes |
| Meat & poultry | — | ✓ 5 recipes |
| Fish | — | ✓ 4 recipes |
| Vegetarian | — | ✓ 4 recipes |
| Quick & easy | — | ✓ 4 recipes |
| Snacks | — | ✓ 5 recipes |

---

## 🔒 Privacy

- **No account required** — the app has no backend
- **API key** — stored in `localStorage` on your device only, never sent anywhere except directly to `api.anthropic.com`
- **No analytics** — zero tracking, no cookies, no third-party scripts
- **No ads** — ever

---

## 🛠 Tech Stack

- Vanilla HTML, CSS, JavaScript — no frameworks, no build step
- [Anthropic Messages API](https://docs.anthropic.com/en/api/messages) with streaming
- PWA: Web App Manifest + Service Worker (both inline as Blob URLs)
- LocalStorage for state persistence

---

## ⚠️ Disclaimer

Tiny Bites provides general meal ideas and nutritional information for reference only. It is not a substitute for advice from a paediatrician, dietitian, or other qualified health professional. Always consult your child's doctor before introducing new foods, especially if your child has allergies or medical conditions.

---

## 📄 License

MIT — free to use, modify, and share.

---

*Built with Claude · Powered by Anthropic*
