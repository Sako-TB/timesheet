# Tomorrow Biostasis — Timesheet

A printable, fillable timesheet for work at the European Biostasis Foundation (EBF) in Rafz, Switzerland. One page, runs in any browser, no backend.

## How to use

1. Open the page.
2. Under **Employees**, type the name of the first employee. Click **Add another employee** for each additional person who worked the same hours.
3. Fill in the **Period** (e.g. "April 2026").
4. Click **Add day** for each day worked. Enter morning start/end and afternoon start/end times — lunch is automatically excluded.
5. Click **Print / Save PDF** in the top right.
6. One A4 page will be printed per employee, each pre-filled with the same dates and times. Signatures are done by hand on each printed page.

Total hours are calculated automatically in both `h:mm` and decimal format.

---

## Deploy to GitHub Pages (free hosting)

This is how to publish the timesheet at `https://<your-username>.github.io/<repo-name>/`.

### 1. Create the repository

- Go to [github.com/new](https://github.com/new)
- Give it a name (for example `timesheet`)
- Pick **Public** (required for free GitHub Pages)
- Click **Create repository**

### 2. Upload the files

On the empty repo page, click **"uploading an existing file"** (the link in the setup instructions), then drag in both files:

- `index.html`
- `README.md`

Click **Commit changes**.

### 3. Turn on GitHub Pages

- In the repo, go to **Settings → Pages** (left sidebar).
- Under **Build and deployment → Source**, select **Deploy from a branch**.
- Set the branch to **`main`** and the folder to **`/ (root)`**, then click **Save**.

### 4. Open the site

Wait about a minute. Refresh the Pages settings page — the URL of the live site will appear near the top, e.g.

```
https://your-username.github.io/timesheet/
```

That's the link to share with employees.

---

## Run it without hosting

Just double-click `index.html` — it opens straight in your browser and works fully offline after the first load.

---

## How to customize

The whole app is one file: `index.html`. Open it in any text editor.

- Change the **company name, subtitle, or header text** → search for `Tomorrow Biostasis GmbH` and `Time sheet for work at EBF in Rafz` near the top of the JSX.
- Change the **declaration text** → search for `I hereby confirm`.
- Change the **colors** → the palette uses Tailwind's `stone` scale (`bg-stone-100`, `text-stone-900`, etc.). Swap `stone` for another Tailwind palette like `slate`, `neutral`, or `zinc`.
- Change the **fonts** → update the Google Fonts `<link>` in the `<head>` and the `font-family` rules in the `<style>` block.

Commit and push the change — GitHub Pages redeploys automatically within a minute.

---

## Files

- `index.html` — the entire app (React + Tailwind loaded from CDN, no build step).
- `README.md` — this file.
