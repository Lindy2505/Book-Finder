# BookFinder (129 themed books)

Static site for GitHub Pages — search by title, author, age, or keyword.

## What’s included
- `index.html` — app UI (Tailwind, Merriweather + Quicksand)
- `books.json` — **129 cleaned entries** (links point to Google Books search)
- `assets/book.svg` — default cover illustration

## Deploy on GitHub Pages
1. Create a new repository on GitHub.
2. Upload **all files at repo root** (keep `index.html` at the top level).
3. Commit to the `main` branch.
4. Repo → **Settings → Pages** → Build and deployment: **Deploy from a branch** → Branch: `main`, Folder: `/ (root)` → Save.
5. Wait ~1 minute. Your site will be at `https://<your-username>.github.io/<repo-name>/`.

## Verify it’s live
- Visit `https://<your-username>.github.io/<repo-name>/books.json` → you should see 129 items.
- If you get a 404, check that `index.html` and `books.json` are in the **repo root**, not in a subfolder.

## Customise
- **Colours**: change Tailwind utility classes in `index.html` (look for `bg-`, `text-`, gradient `from-` / `to-`).
- **Fonts**: change the Google Fonts link in `<head>`.
- **Default cover**: replace `assets/book.svg` (keep the same file name, or update the path in `index.html`).
- **Per-book images**: add an `"image": "assets/yourfile.jpg"` to a book in `books.json` and the app will use it.

## Data format
Each book has:
```json
{
  "title": "…",
  "author": "…",
  "age": "7-9",
  "keywords": ["…"],
  "summary": "…",
  "link": "https://www.google.com/search?tbm=bks&q=<title+author>"
}
```

## Troubleshooting
- **Case sensitivity**: `books.json` and `assets/book.svg` must be lower-case exactly.
- **YouTube links**: Not used. The app also **guards** against `youtube.com`/`youtu.be` and will fall back to a Google Books search.
- **Nothing happens on search**: You might be viewing the file with `file://`. Use GitHub Pages (or a local server).

