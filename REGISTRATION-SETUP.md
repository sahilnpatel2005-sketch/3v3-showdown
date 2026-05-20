# Team Registration — How It Works

This documents how the **Register Your Team** buttons connect to a Google Form,
and how submissions get recorded in a Google Sheet.

## The flow

```
Visitor clicks "Register Your Team"  →  Google Form opens (new tab)
        →  Visitor submits the form  →  A new row is added to a Google Sheet
```

## How the site is wired (no code changes needed per button)

Every button with the class `btn-register` in `index.html` has its link set
automatically from one place — the `CONFIG` block near the top of the file:

```js
const CONFIG = {
  GOOGLE_FORM_URL: "https://forms.gle/REPLACE_ME",  // <-- put your real form link here
  ...
};
```

A small script at the bottom of `index.html` points every Register button at
that URL and opens it in a new tab. So you only ever change the URL in **one
place**.

Buttons covered: "Register", "Lock In Your Team", "Reserve Your Spot", and the
final "Register Your Team" CTA.

## One-time setup (done inside your Google account)

1. Go to [forms.google.com](https://forms.google.com) and create a form.
   Suggested questions: team name, captain name/phone/email, player 2 & 3 names,
   preferred time slot, payment method, payment handle.
2. Open the form's **Responses** tab → click the green **Sheets** icon →
   **Create a new spreadsheet**. From now on, every submission automatically
   appends a row to that Sheet. *(This is the "documented on a Google Sheet"
   part — it is automatic once linked.)*
3. Click **Send** → the link icon (🔗) → copy the `https://forms.gle/...` link.
4. Paste that link into `GOOGLE_FORM_URL` in the `CONFIG` block in `index.html`.
5. Save and submit one test entry to confirm a row appears in the Sheet.

## Checklist before sharing the site

- [ ] `GOOGLE_FORM_URL` is the real form link (not `REPLACE_ME`)
- [ ] Form responses are linked to a Google Sheet
- [ ] A test submission showed up as a row in the Sheet
