# Training Log — Personal PWA

A workout tracker that lives entirely on your phone. No accounts, no subscriptions, no cloud.

## What's in this folder

- `index.html` — the entire app (HTML + CSS + JavaScript in one file)
- `sw.js` — service worker for offline support
- `README.md` — this file

That's it. No build step, no dependencies.

---

## Setup: get it onto your iPhone (one-time, ~10 min)

### Step 1: Create a GitHub account (if you don't have one)

1. Go to **https://github.com**
2. Click **Sign up** in the top right
3. Pick a username, email, and password. Free tier is fine.
4. Verify your email when GitHub sends the verification link

### Step 2: Create a new repository

1. Once logged in, click the **+** icon top-right → **New repository**
2. Repository name: `training-log` (or anything you like — lowercase, no spaces)
3. Set it to **Public** (required for free GitHub Pages hosting; the URL is shareable but nobody will find it unless you tell them)
4. Check **Add a README file**
5. Click **Create repository**

### Step 3: Upload the files

1. On the new repo page, click **Add file** → **Upload files**
2. Drag `index.html` and `sw.js` into the upload area (skip this README — it's just for you)
3. Scroll down, click **Commit changes**

### Step 4: Enable GitHub Pages

1. In your repo, click **Settings** (top tab)
2. Left sidebar: click **Pages**
3. Under **Source**, choose **Deploy from a branch**
4. Branch: select **main** and folder: **/ (root)**, then click **Save**
5. Wait ~1 minute. The page will refresh and show: **"Your site is live at https://YOUR-USERNAME.github.io/training-log/"**
6. Copy that URL

### Step 5: Add to iPhone home screen

1. On your iPhone, open **Safari** (must be Safari, not Chrome)
2. Paste the URL from Step 4 and load the page
3. Tap the **Share** button (square with up arrow at the bottom)
4. Scroll down and tap **Add to Home Screen**
5. Name it "Training" (or whatever you want), tap **Add**
6. Close Safari. The app icon is now on your home screen. Tapping it opens the app full-screen — no browser bar.

That's it. The app now works offline. Your data stays on your phone.

---

## Using the app

**First time:** tap the icon. The home screen tells you there's no block yet. Tap **Quick-start with my plan** to load the full 21-exercise plan (Block 1, Weeks 1–8). Or tap **Create blank block** to build from scratch.

**Daily use:** open the app → tap the suggested day → tap an exercise → see last session's numbers and full exercise details (target muscles, goal, progression, rotation — collapsible per-exercise) → log your sets → tap Save. After the last exercise, hit **Finish session** to log knee pain and sleep.

**Adding a second block** (when you get to Week 9): home → tap the active block selector → **New block** → name it "Block 2 — Weeks 9–16" → add days and exercises. Or quick-start a copy of Block 1 and edit the exercises to the Week 8+ rotations.

**Editing anything:** Settings (gear icon) → Manage blocks → tap a block → tap any exercise to edit. All fields editable, including the goal/target/progression text shown during sessions.

**Backing up:** Settings → **Export to text file** (downloads a JSON file you can save anywhere — Notes, iCloud Drive, email to yourself) or **Copy to clipboard** (paste into Notes directly).

**Restoring:** Settings → **Import from text** → paste the JSON. Overwrites everything currently in the app.

---

## Updating the app later

If you ever want to change something (add features, fix something, etc.):

1. Edit `index.html` on your computer
2. Go to your GitHub repo → click `index.html` → click the pencil icon (Edit)
3. Paste the new content, scroll down, **Commit changes**
4. Wait 1 minute, then on your iPhone, open the app. It'll update automatically.

If the update doesn't seem to take effect, close the app, then in iPhone Settings → Safari → Advanced → Website Data → search "github.io" → swipe to delete just that entry. Reopen the app.

---

## Privacy and data

- All workout data is stored in `localStorage` on your iPhone only
- GitHub Pages hosts only the app code (3 files), never your data
- The app makes zero network requests once loaded (works offline)
- No analytics, no tracking, no telemetry

---

## Limitations (honest list)

- **iOS may clear local storage** if your phone fills up, or if you clear Safari history. Export weekly to be safe.
- **No Apple Watch integration.** Requires Xcode/native development.
- **No notifications.** Use iPhone Reminders separately.
- **Charts are simple SVG.** No zoom, no fancy interactions — just clean line charts.
- **One device.** If you want the same data on iPad too, export from phone → import on iPad manually.
# training-log
