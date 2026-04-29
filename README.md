# Commonplace

A personal reading journal. Track your books, collect quotes, take notes, and monitor your reading progress — all in a single file that lives in your browser.

## Deploying to GitHub Pages

### 1. Create the repository

1. Go to [github.com](https://github.com) and sign in
2. Click **+** → **New repository**
3. Name it anything you like — e.g. `commonplace`
4. Set it to **Public** (required for free GitHub Pages)
5. Leave everything else at defaults and click **Create repository**

### 2. Upload the files

In your new repository, click **Add file** → **Upload files** and upload all of these:

```
index.html
manifest.json
icon-192.svg
_config.yml
```

Commit directly to the `main` branch.

### 3. Enable GitHub Pages

1. Go to **Settings** → **Pages** (left sidebar)
2. Under **Source**, select **Deploy from a branch**
3. Choose branch: `main`, folder: `/ (root)`
4. Click **Save**

GitHub will give you a URL like `https://yourusername.github.io/commonplace/` — it may take a minute to go live.

---

## Installing on iPhone

Once your site is live:

1. Open the URL in **Safari** on your iPhone (must be Safari, not Chrome)
2. Tap the **Share** button (the box with an arrow pointing up)
3. Scroll down and tap **Add to Home Screen**
4. Name it **Commonplace** and tap **Add**

The app will appear on your home screen and open full-screen with no browser chrome, exactly like a native app.

**Important notes:**
- All data is stored in Safari's `localStorage` on your device — it stays private and works offline
- **Back up regularly** using the export function (the download icon in the sidebar) — if you clear Safari's website data, your library will be erased
- The export file is a JSON file you can store in iCloud, email to yourself, or keep anywhere safe
- To restore on a new device or after clearing data, use **Import Library** in the same menu

---

## Keeping it updated

When you make changes to the app, upload the new `index.html` to your repository. GitHub Pages will redeploy automatically within a minute or two. Refresh the app on your phone (you may need to close and reopen it) to pick up the changes. Your data is unaffected by updates.
