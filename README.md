# Commonplace

A personal reading journal. Track your books, collect quotes and notes, monitor your progress, run your book club, and vote on what to read next — all in a single file that lives in your browser, works offline, and stores everything privately on your own device.

---

## Table of Contents

1. [Getting the App](#getting-the-app)
2. [Installing on iPhone (iOS)](#installing-on-iphone-ios)
3. [Installing on Android](#installing-on-android)
4. [Keeping It Updated](#keeping-it-updated)
5. [Your Library — Adding Books](#your-library--adding-books)
6. [Tracking Reading Progress](#tracking-reading-progress)
7. [Quotes & Notes (Notebook)](#quotes--notes-notebook)
8. [The Bookshelf Tab](#the-bookshelf-tab)
9. [To-Read List](#to-read-list)
10. [Stats](#stats)
11. [Book Club](#book-club)
12. [AI Insights](#ai-insights)
13. [Backup, Export & Import](#backup-export--import)
14. [Data & Privacy](#data--privacy)

---

## Getting the App

Commonplace is a web app hosted on GitHub Pages. There is nothing to install from an app store. You access it at:

**[danpmeyer.github.io/commonplace](https://danpmeyer.github.io/commonplace)**

You can also fork or clone the source from the GitHub repository:

**[github.com/danpmeyer/commonplace](https://github.com/danpmeyer/commonplace)**

The entire app ships as a single `index.html` file. If you want your own private copy under your own GitHub account, see the [self-hosting instructions](#self-hosting-on-github-pages) at the end of this document.

---

## Installing on iPhone (iOS)

Commonplace is a Progressive Web App (PWA). On iOS, the only browser that can install PWAs to your home screen is **Safari**. Chrome, Firefox, and other iOS browsers cannot do this.

1. Open **[danpmeyer.github.io/commonplace](https://danpmeyer.github.io/commonplace)** in **Safari**
2. Tap the **Share** button — the square icon with an arrow pointing upward, in the toolbar at the bottom of Safari
3. Scroll down in the share sheet and tap **Add to Home Screen**
4. The name will be filled in as "Commonplace" — leave it as is and tap **Add** in the top-right corner

The app will appear on your home screen. Tap it to open — it runs full-screen with no browser chrome, exactly like a native app. It works completely offline once installed.

**Notes for iOS users:**
- All data is stored in Safari's local storage on your device. It is never sent to any server.
- iOS Safari can aggressively clear local storage if your device is low on space or if you haven't opened the app in more than seven days. The app uses a secondary storage layer (IndexedDB) that is harder to evict, and will attempt to restore your data automatically if local storage is cleared. However, you should still **export a backup regularly** — see [Backup, Export & Import](#backup-export--import).
- Clearing Safari's website data in iOS Settings will erase all your Commonplace data. Export first.
- If the app appears broken or white after an update, close it fully (swipe up from the app switcher) and reopen it.

---

## Installing on Android

Android supports PWA installation from any Chromium-based browser, including Chrome, Edge, and Brave.

### Chrome (recommended)

1. Open **[danpmeyer.github.io/commonplace](https://danpmeyer.github.io/commonplace)** in **Chrome**
2. Tap the **three-dot menu** (⋮) in the top-right corner
3. Tap **Add to Home screen** (or **Install app** — the label varies by Android version)
4. Tap **Add** in the dialog that appears

The app icon will appear on your home screen and in your app drawer. It opens full-screen with no browser interface.

### Alternative: Samsung Internet

1. Open the app URL in **Samsung Internet**
2. Tap the **menu icon** (three horizontal lines) at the bottom
3. Tap **Add page to** → **Home screen**

**Notes for Android users:**
- Android's local storage for PWAs is generally more stable than iOS and is less likely to be cleared without warning.
- Chrome will occasionally prompt you to install the app automatically via a banner at the bottom of the screen — you can use that prompt instead of the menu steps above.
- To uninstall, long-press the icon on your home screen and choose **Remove** or **Uninstall**, as you would any app.

---

## Keeping It Updated

When a new version of Commonplace is published at `danpmeyer.github.io/commonplace`:

1. Open the app
2. Close it fully (on iOS: swipe it up in the app switcher; on Android: clear it from recents)
3. Reopen it

Your data is stored on your device and is not affected by app updates. If you notice the app looks wrong after an update, a full close and reopen almost always fixes it.

---

## Your Library — Adding Books

Tap **+ Add Book** (sidebar on desktop, the **+** icon at the top-right on mobile) to open the book form.

### Auto-fill from ISBN

Enter an ISBN-10 or ISBN-13 at the top of the form and tap **Look up**. The app queries the Open Library API and fills in the title, author, publisher, publication year, page count, cover image, and language automatically. You can still edit any of the auto-filled fields.

### Manual fields

| Field | Notes |
|---|---|
| **Title** | Required |
| **Author(s)** | Required. For multiple authors, separate with commas |
| **Translator / Editor** | Optional. Used for translated works or edited collections |
| **Original Published** | The first publication year of the work |
| **Edition Year** | The year of the specific edition you own |
| **Publisher** | |
| **Pages** | Total pages in the volume |
| **ISBN** | Used for cover lookup |
| **Genre / Category** | Free text |
| **Language** | |
| **Status** | To-Read, Currently Reading, or Read |
| **Ownership** | Owned or Wishlist. Owned reveals purchase source and date fields |
| **Cover Image** | Upload a photo. If left blank, a generated colour spine is used |
| **Notes** | Private notes about the book itself (not the same as reading notes) |

### Anthologies

If you are reading a work that appears within a larger collection — a poem in an anthology, an essay in a collected works, a novella in an omnibus — tick **This is an anthology / collected work**. This reveals:

- **Anthology / Collection Title** — the title of the containing volume
- **Editor(s)** — the anthology's editor
- **Start Page in Volume** — the first page of the work you are reading
- **End Page in Volume** — the last page of the work you are reading

When these fields are set, progress is calculated within that range. Entering page 180 in a 142–289 range shows 33% complete, not 33% of the full volume. The "mark as finished" trigger fires when you reach the end page of the work, not the last page of the whole book.

---

## Tracking Reading Progress

### Updating progress

On the **Home** tab, each currently-reading book shows an **Update Progress** button. Tap it to enter:

- **Current page** — your current page number. For anthologies, enter the page number within the full volume (the range is shown as a reminder).
- **Date Started** — pre-filled from when you first started tracking. Edit if needed.
- **Date Finished** — appears automatically when you enter the last page (or end page for anthologies). Marking the book as finished records a completed reading session.

The progress bar updates in real time as you type the page number.

### Stale books

If a currently-reading book hasn't had its progress updated in **14 days**, it shrinks to a compact row on the Home tab — a subtle reminder that it has gone quiet. An **Update** button appears on the right of the row.

### Reading history

Every progress update is logged. You can see the full page-by-page history for any book by opening its detail view (tap anywhere on the book card) and scrolling to the collapsible **Reading History** section at the bottom. This section shows every update with its date and how many pages were read in that session.

### Reading Dates tab

For books marked as **Read**, the **Dates** tab in the detail view lets you edit start and finish dates for each reading session. You can also add a new reading session (if you read a book a second time) or tap **+ Read again** to reset the book to currently-reading with a fresh start date.

---

## Quotes & Notes (Notebook)

Access your notebook via the **Notebook** tab (desktop sidebar) or the **Notebook** tab in the mobile tab bar.

### Adding a quote

Tap **+ Quote** and fill in:
- **Book** — search by title or author, or pick from the three most recently updated books
- **Quote text** — supports Markdown formatting (**bold**, *italic*, lists, headings)
- **Page number** — optional
- **Chapter / Section** — optional
- **Commentary** — your own note on the quote

### Adding a note

Tap **+ Note** and fill in:
- **Book** — same search widget as quotes
- **Note type** — General, Chapter Summary, Thematic, Reflection, or Question
- **Reference** — chapter title, section, or page range this note refers to
- **Note text** — supports Markdown formatting

### Viewing the Notebook

Entries are grouped by book, with the book title and author shown as a section header. Within each book, quotes and notes are listed in reverse chronological order. Use the **filter bar** to show All, Quotes only, or Notes only. The **search bar** filters across text, book titles, and authors.

Edit or delete any entry using the buttons at the bottom-right of each card.

### Quote of the Day

The **Home** tab shows a randomly selected quote at the very top, seeded from today's date — so it changes every day automatically. Tap **↻ Shuffle** to see a different quote immediately.

---

## The Bookshelf Tab

The **Shelf** tab shows your full library with filtering, sorting, and two display modes.

### Display modes

Toggle between **List** (rows with full metadata) and **Grid** (cover tiles) using the icons at the top-right of the shelf.

### Filtering

The **Show** dropdown filters by:
- All
- Reading
- Read
- To-Read
- Owned (all books you own, regardless of status)
- Wishlist
- Has Notes

### Sorting

The **Sort by** dropdown offers:
- **Last updated** (default) — currently-reading books appear first, sorted by most recent progress update; everything else follows by when it was last touched
- **Status** — groups books by reading status
- **Title A–Z**
- **Author surname**
- **Year published**
- **Year read** — finished books newest first, currently-reading at top
- **Date added**

### Tapping a book

Tap any book to open its detail view, which has four tabs:

| Tab | Contents |
|---|---|
| **Info** | Full metadata, reading dates summary, anthology details if applicable |
| **Quotes** | All quotes for this book, with add/edit/delete |
| **Notes** | All notes for this book, with add/edit/delete |
| **Dates** | Editable start/finish dates for each reading session (read books only) |

A collapsible **Reading History** section at the bottom shows the full page-log for currently-reading or finished books.

---

## To-Read List

The **To-Read** tab lists all books with status "To-Read" or "Wishlist". Tap any book to view its details, or use the status field in the Edit view to move it to Currently Reading when you're ready to start.

---

## Stats

The **Stats** view (sidebar on desktop, More → Stats on mobile) shows:

- **Yearly reading goal** — set a target number of books. A progress bar shows how many you have read this year and your pace relative to finishing on time.
- **Reading statistics** — total books, total read, total quotes, total notes.

---

## Book Club

Access the **Book Club** section from the sidebar (desktop) or **More** drawer (mobile).

### First-time setup

On first opening, you will see a setup form:
- **Book Club Name**
- **Meeting Frequency** — weekly, bi-weekly, monthly, every two months, or quarterly
- **Members** — add each member with a name and optional photo (tap the circle to upload a square-cropped image)

You need at least two members to create the club.

### Current Read

The top of the Book Club page shows the current read — book title, author, and a countdown to the meeting date ("12 days until meeting"). Tap **+ Set Current Read** (if no book is set) or the **Edit** button (if one is) to choose:
- The book (from your library)
- The meeting date
- A **Meeting Poster** — upload a custom image you have designed for the meeting. It replaces the book cover in the hero card.

When the meeting is over, tap **Mark as Finished** to move the book into Past Reads.

### Past Reads

A chronological list of books the club has read, sorted by when they were read (newest first). Tap any book to open its ratings panel:

- Each member has a **0–10 rating field** supporting decimals (e.g. 7.5, 8.3). Leave a member's field blank if they did not read the book.
- The **average score** is calculated from members who have rated.
- Add freeform **club notes** for this book.
- Tap **+ Add** in the Past Reads section header to add a book manually with a month/year (e.g. "March 2025").

### Book Voting

The voting system uses **Borda count** — a ranked-choice method where each voter ranks all candidates. First place gets the most points, last place the fewest. The book with the most total points wins.

**Starting a vote:**

1. Tap **New Vote**
2. Select which books are candidates for the vote
3. Select which members are participating (useful if someone is absent)
4. Tap **Start Voting**

**Voting:**

Each member votes one at a time. Their name and photo appear at the top of the ballot. They rank the books by dragging them up and down, or using the ▲/▼ arrow buttons. When satisfied, they tap **Submit Ranking →** and the next member's ballot appears automatically.

**Results:**

When all members have voted, a "Calculate Results" button appears. Tap it to run the tally. The results screen shows a bar chart of scores with the winner highlighted. Past vote results are saved and accessible from the Voting section.

**Editing votes after the fact:**

Tap **View results** on any completed vote. The results screen shows the full tally at the top, then each member's ballot below it. You can:
- **Edit a ranking** — drag the books in any member's ballot to a new order, or use the arrows
- **Add a voter** — if a member didn't vote originally, a dropdown lets you add them; tapping it opens their ballot immediately
- Tap **Save & Recalculate** to commit all changes and rerun the Borda count

### Club Settings

At the bottom of the Book Club page, tap **Club Settings** to edit the club name, meeting frequency, member names, member photos, and add or remove members.

---

## AI Insights

Commonplace can generate literary analysis and summaries using the Claude API. This requires a **Claude API key** from Anthropic — the API is separate from a Claude.ai subscription and is billed per use (a typical book summary costs a fraction of a cent).

**Getting an API key:**
1. Go to [console.anthropic.com](https://console.anthropic.com)
2. Sign in or create an account
3. Go to **API Keys** → **Create Key**
4. Copy the key (it begins with `sk-ant-api03-…`)

**Using AI Insights:**

Tap **✦ AI Insights** on any book's detail view. The first time you use it, a prompt appears to enter your API key — it is stored only on your device and never transmitted anywhere except directly to Anthropic's API.

Available insight types:
- **Overall Book Summary** — themes, narrative arc, and significance
- **Chapter Summary** — enter a specific chapter or page range
- **Thematic Analysis** — deep analysis of major themes and literary context
- **Historical / Literary Context** — background a reader should know
- **Synthesize My Notes & Quotes** — patterns and threads from your own annotations
- **Custom Prompt** — ask anything

Responses render with full Markdown formatting. Tap **Change API key** at the bottom of the modal to update or remove your key.

---

## Backup, Export & Import

Your data lives entirely on your device. Commonplace has no server or cloud sync. **Regular exports are the only way to ensure your data is safe.**

### Exporting

On desktop: click the download icon at the bottom of the sidebar.
On mobile: open **More** → **Backup & Import**.

Tap **Export Library**. A JSON file named `commonplace-backup-YYYY-MM-DD.json` will be downloaded. Store it somewhere safe — iCloud Drive, Google Drive, email to yourself, a computer — anywhere outside your phone.

The export includes your complete library: all books, quotes, notes, reading log, reading dates, yearly goal, and book club data (members, past reads, votes, ratings, meeting poster).

### Importing

Open **Backup & Import** and tap **Import / Restore**. Select your JSON backup file. The import merges the backup with your current data — books, quotes, and notes are merged by ID so duplicates are avoided. Book club data is fully restored from the backup.

### Automatic reminder

If you haven't exported in 14 days, a quiet banner appears at the bottom of the screen reminding you to back up. Tap **Export now** to dismiss it and download a backup, or **Dismiss** to close the banner temporarily.

### Restoring from the automatic backup

The app writes your data to two separate browser storage locations simultaneously — localStorage and IndexedDB. If iOS Safari clears localStorage (which it can do silently when storage is low), the app will automatically detect this on next launch and restore your data from IndexedDB. A banner will inform you that a restore happened and recommend exporting a manual backup.

---

## Data & Privacy

- **All data is stored locally on your device.** Nothing is sent to any server except when you use AI Insights (which sends only the book title and your notes to Anthropic's API) or the ISBN lookup (which sends only the ISBN to the Open Library API).
- **The app works fully offline** once installed as a PWA.
- **There are no accounts, no sign-in, and no analytics.**
- Clearing browser or Safari website data will erase your Commonplace library. Always maintain a backup export.

---

## Self-Hosting on GitHub Pages

If you want your own copy under your own GitHub account:

### 1. Fork or create the repository

**Option A — Fork:** Go to [github.com/danpmeyer/commonplace](https://github.com/danpmeyer/commonplace) and click **Fork**. Your fork will be at `github.com/yourusername/commonplace`.

**Option B — New repository:**
1. Go to [github.com](https://github.com) → **+** → **New repository**
2. Name it `commonplace` (or anything you like)
3. Set it to **Public** — required for free GitHub Pages
4. Click **Create repository**
5. Click **Add file** → **Upload files** and upload: `index.html`, `manifest.json`, `icon-192.svg`, `_config.yml`

### 2. Enable GitHub Pages

1. Go to your repository's **Settings** → **Pages** (left sidebar)
2. Under **Source**, choose **Deploy from a branch**
3. Set branch to **main**, folder to **/ (root)**
4. Click **Save**

Your app will be live at `https://yourusername.github.io/commonplace/` within a minute or two.

### 3. Updating your copy

When you want to update to a newer version, download the latest `index.html` from the source repository and upload it to your own repository via **Add file** → **Upload files**, choosing to overwrite the existing file. GitHub Pages redeploys automatically.

**Before uploading any update, export a backup from the app** — just in case.
