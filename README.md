# Miki — Black Belt Journey

A training diary for a young martial artist. Classes, belt tests, photos, stars and
badges — installed on an iPhone like a real app, works offline, no account, no server.

```
miki-belt-journey/
├── index.html              the whole app (HTML + CSS + JS in one file)
├── manifest.webmanifest    app name, icon and colours used when installed
├── sw.js                   service worker — makes it work with no internet
└── icons/                  home-screen icon (180 / 192 / 512 + maskable)
```

## Install it on the iPhone (5 minutes)

You need the folder on a real `https://` address first — iPhone only allows
"Add to Home Screen" apps to work offline from HTTPS. Pick one:

**Option A — Netlify Drop (fastest, free, no account needed to try)**
1. Go to <https://app.netlify.com/drop>
2. Drag the **folder** `miki-belt-journey` onto the page.
3. It gives you a link like `https://sunny-panda-123.netlify.app`. Copy it.

**Option B — GitHub Pages (free, permanent, editable later)**
1. Create a repository, upload the four items in this folder.
2. Settings → Pages → Source: *Deploy from a branch* → `main` / `/ (root)` → Save.
3. After a minute the app is at `https://<user>.github.io/<repo>/`.

**Then, on the iPhone:**
1. Open the link in **Safari** (it must be Safari, not Chrome).
2. Tap the **Share** button → **Add to Home Screen** → **Add**.
3. Open “Miki” from the home screen. It launches full screen with no browser bars.

## Using it

- **＋ Add training** — pick what she did, give it a title, tap 1–3 stars, pick a mood,
  write a line, add a photo. Confetti on save.
- **Belt tests** — choose the “Belt test” type. It becomes a gold test card and counts
  toward the “Test day” badge.
- **Progress** — the purple bar counts trainings since the last belt test. At 10 it says
  she is ready for the next belt. Moving the belt itself is a grown-up action:
  *For grown-ups → Change name, belt & style*.
- **For grown-ups** (bottom of the page) — save a backup file, restore one, print the
  diary, or reset to the sample diary.

## Things worth knowing

- **The diary lives only on that iPhone.** Nothing is uploaded. Use *Save a backup file*
  now and then; it is the only way to move the diary to a new phone.
- **After you edit `index.html`**, open `sw.js` and change `miki-diary-v1` to
  `miki-diary-v2`. Otherwise the phone keeps showing the old cached copy.
- **Clearing Safari data deletes the diary.** Back up first.
- Photos are shrunk to 1500 px JPEG before saving, so a few hundred fit comfortably.

## Local preview

```
python -m http.server 8123
# then open http://127.0.0.1:8123
```

Opening `index.html` by double-click works too — everything except the offline cache,
which only runs over `http(s)`.
