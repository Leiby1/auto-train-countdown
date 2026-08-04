# 🚂 Auto Train Adventure — Cinematic Countdown

A cinematic, dark-gold vertical countdown to Amtrak Auto Train 53 —
Lorton, VA → Sanford, FL. The live scene (stars, train, sparks, smoke,
headlight glow) is drawn with SVG/canvas/CSS. A separate static image
(`og-image.png`) is included just for link previews — apps like
iMessage or Slack can't render the live animation, so they need a
plain picture to show instead.

## Files

- `index.html` — the entire app (self-contained: HTML, CSS, JS, audio)
- `og-image.png` — the picture shown when you **share the link**
  (iMessage, WhatsApp, Slack, X, Facebook, etc. — wired up automatically
  via the meta tags already in `index.html`)
- `favicon.svg`, `favicon-32.png` — browser tab icon
- `apple-touch-icon.png`, `icon-512.png` — home-screen icon if someone saves the link

## Upload to GitHub (no command line needed)

1. Go to **github.com** and sign in (create a free account if you don't have one).
2. Click the **+** in the top right → **New repository**.
3. Name it something like `auto-train-countdown`, set it to **Public**,
   and click **Create repository** (leave everything else unchecked).
4. On the next page, click **uploading an existing file**.
5. Drag in every file from this zip: `index.html`, `og-image.png`,
   `favicon.svg`, `favicon-32.png`, `apple-touch-icon.png`, `icon-512.png`.
6. Scroll down and click **Commit changes**.

## Turn on the live link (GitHub Pages)

1. In your repo, go to **Settings** (top menu) → **Pages** (left sidebar).
2. Under "Build and deployment": **Source → Deploy from a branch**,
   **Branch → main**, folder **/ (root)** → **Save**.
3. Wait about a minute, then refresh the page — GitHub shows your live
   link at the top, in the form:
   `https://<your-username>.github.io/<repo-name>/`
4. That's your shareable countdown. Open it once yourself to confirm
   it loads, then share the link however you like.

## One extra step for the best-looking share preview

Some apps (iMessage especially) want the preview image as a full web
address rather than a filename. Once your Pages link is live:

1. In GitHub, open `index.html` → click the pencil (✏️) to edit.
2. Find these two lines near the top:
   ```
   <meta property="og:image" content="og-image.png">
   <meta name="twitter:image" content="og-image.png">
   ```
3. Replace `og-image.png` in both with your full Pages URL, e.g.
   `https://<your-username>.github.io/<repo-name>/og-image.png`
4. Commit changes. Give it a few minutes — some apps cache old
   previews, so if it doesn't show up right away, try sharing to a
   different chat.

## Notes

- The departure target is set in `index.html` — search for
  `2026-09-14T16:00:00` if the date/time ever needs to change.
- `og-image.png` is a fixed snapshot, not a live countdown — link
  previews can't tick in real time. The actual site always shows the
  correct live countdown.
- Sound is synthesized in-browser (engine rumble, horn, bass hit) and
  unlocks on the first tap, since phones block autoplaying audio.
- Best viewed on a phone in portrait — it's built for a 9:16 frame.
