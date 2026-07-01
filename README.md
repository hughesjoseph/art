# Your portfolio site — how to edit & host

Everything lives in one file: **`index.html`**. Your pictures go in an **`images`**
folder next to it. That's the whole site.

```
your-site-folder/
├─ index.html
├─ images/
│   ├─ 1.jpg   2.jpg   3.jpg   4.jpg   5.jpg   ← your artworks
│   └─ portrait.jpg                            ← photo of you (About panel)
└─ files/
    └─ cv.pdf                                   ← optional, add later
```

---

## 1. Add your images
Drop your artwork files into the `images` folder and name them `1.jpg`, `2.jpg`,
`3.jpg`, and so on. Any web format works (`.jpg`, `.png`, `.webp`) — if you use a
different name or format, just match it in the `src:` line for that work (below).
Add a photo of yourself as `images/portrait.jpg` for the About panel.

## 2. Edit the text (open `index.html` in any text editor)
Scroll down to the part that says **EDIT EVERYTHING BELOW THIS LINE**.

**The captions (bottom-left of each slide)** — edit the `WORKS` list. Each work
is one block:

```js
{
  src:        "images/1.jpg",
  title:      "Untitled (Beaded Curtain)",
  year:       "2024",
  materials:  "Cast acrylic beads, steel jump rings",
  dimensions: "300 × 240 × 12 cm",
  context:    "Installation view, Gallery Name, City"
},
```

Change the words inside the quotes. Leave any line as `""` to hide it. To add
another work, copy a whole block (from `{` to `},`) and paste it in. To remove
one, delete its block. The rotation adjusts automatically.

**Your name & timing** — near the top:
- `SITE_NAME` — your name (top-left, and it opens the About panel).
- `INTERVAL_MS` — how long each image holds, in milliseconds (`3000` = 3 seconds).

**The About panel** — edit the `ABOUT` block:
- `portrait` — path to your photo.
- `bio` — each line in quotes becomes a paragraph. Add or remove lines.
- `cv` — leave as `""` for now. To add a CV later, put a PDF in a `files` folder
  and set `cv: "files/cv.pdf"`. The download button then appears by itself.

Save the file, refresh your browser — done. (Tip: keep a backup copy before big edits.)

---

## 3. Put it online (free)

The site is just static files, so hosting is easy and free. Two simple routes:

### Easiest — Netlify Drop (no account setup, no code)
1. Go to **https://app.netlify.com/drop**
2. Drag your **whole site folder** (the one containing `index.html`) onto the page.
3. It publishes in seconds and gives you a live link like
   `your-name.netlify.app`. To update later, drag the folder again.
   (Make a free account if you want the same address to stick and to add a custom domain.)

### Also great — GitHub Pages or Cloudflare Pages
- **Cloudflare Pages** (https://pages.cloudflare.com) — connect a folder/repo, free, fast.
- **GitHub Pages** — upload the files to a repository, enable Pages in settings.

### Your own domain (e.g. yourname.com)
Buy a domain (Namecheap, Cloudflare, etc.), then in Netlify/Cloudflare's dashboard
choose "Add custom domain" and follow the steps. All three hosts above support this for free.

---

## Controls (built in)
- Auto-rotates left every 3 seconds.
- **Click the left half** of the screen = previous work; **right half** = next.
- **Spacebar** pauses/plays. It also pauses while you hover.
- **Click your name** (top-left) to open About; **× or Esc** closes it.

Nothing to install — it runs in any modern browser.
