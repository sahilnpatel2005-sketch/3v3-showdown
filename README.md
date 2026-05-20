# 3v3 Street Showdown — Tournament Website

A simple one-page website for your boys 3v3 basketball tournament. No install, no frameworks — just open `index.html` in a browser.

## Quick start (open on your computer)

1. Open this folder in Finder (or File Explorer).
2. Double-click **`index.html`** — it opens in Chrome, Safari, or Edge.
3. Click around to make sure links and buttons work.

**Optional:** run a local server from Terminal:

```bash
cd "/Users/sahilpatel/Coding/Backyard Basketball"
python3 -m http.server 8000
```

Then visit [http://localhost:8000](http://localhost:8000) in your browser.

## Customize your site (one place to edit)

Open **`index.html`** and find the **`CONFIG`** block near the top of the page (right after `<body>`). Change these values:

| Setting | What to put |
|---------|-------------|
| `GOOGLE_FORM_URL` | Your Google Form link (see below) |
| `VENMO_URL` | e.g. `https://venmo.com/YourName` |
| `CASHAPP_URL` | e.g. `https://cash.app/$YourHandle` |
| `TOURNAMENT_DATE` | e.g. `Saturday, June 14, 2026` |
| `VENUE_NAME` | Court or park name |
| `VENUE_ADDRESS` | Full address |
| `MAPS_URL` | Google Maps link to the venue |
| `CHECKIN_TIME` | e.g. `8:30 AM` |
| `PHONE` | Your text/call number |
| `EMAIL` | Your email for questions |
| `HASHTAG` | e.g. `#RunTheRack` |

Save the file and refresh your browser to see changes.

## Set up Google Form registration

1. Go to [Google Forms](https://forms.google.com) and create a new form.
2. Add these questions (suggested):
   - **Team name** (short answer)
   - **Captain name** (short answer)
   - **Captain phone** (short answer)
   - **Captain email** (short answer)
   - **Player 2 name** (short answer)
   - **Player 3 name** (short answer)
   - **Preferred time slot** (dropdown):
     - 9:00 AM — Ages 14 & Under
     - 11:30 AM — Ages 15–17
     - 2:00 PM — Open Run 18+
     - 5:00 PM — Championship Finals (spectator / qualifier)
   - **Payment method** (multiple choice: Venmo, Cash App, Cash at check-in)
   - **Payment handle or note** (short answer)
3. Click **Send** → link icon → shorten link if you want.
4. Copy the link (looks like `https://forms.gle/xxxxx`).
5. Paste it into `GOOGLE_FORM_URL` in the CONFIG block in `index.html`.

All **Register** buttons on the site will open that form in a new tab.

## Publish online (free)

### Option A: Netlify Drop (easiest)

1. Go to [https://app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag this entire folder onto the page.
3. Netlify gives you a URL like `https://random-name.netlify.app` — share that link.

### Option B: GitHub Pages

1. Create a GitHub account and a new repository.
2. Upload `index.html` (and `README.md` if you want).
3. In the repo: **Settings** → **Pages** → Source: **main** branch → Save.
4. Your site will be at `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/`.

## Before you share the link — checklist

- [ ] `GOOGLE_FORM_URL` is your real form (not `REPLACE_ME`)
- [ ] Venmo and Cash App links open correctly
- [ ] Date, venue, and map link are correct
- [ ] Phone and email are yours (not placeholders)
- [ ] You submitted a test entry on the Google Form and received it

## Files in this project

| File | Purpose |
|------|---------|
| `index.html` | The whole website (edit CONFIG here) |
| `3v3-tournament.html` | Original backup copy (optional; you can delete it) |
| `README.md` | This guide |

## Need help?

If something does not work, check that you saved `index.html` and hard-refreshed the browser (Cmd+Shift+R on Mac). Registration only works after you add a real Google Form URL.
