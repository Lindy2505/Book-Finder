# BookFinder (static site)

A no-code, single-page book search app you can deploy on **GitHub Pages**.

## What you get
- `index.html` — the app (works out of the box with sample data)
- `books.sample.json` — example data structure
- `assets/book.svg` — clean book illustration used as a cover placeholder

## Use your own data
1. Create a file named **`books.json`** in the repo root.
2. Paste your list of books as a JSON array, e.g.

```json
[
  {
    "title": "The Day You Begin",
    "author": "Jacqueline Woodson",
    "age": "7-9",
    "keywords": ["belonging","diversity"],
    "summary": "…",
    "link": "https://example.com"
  }
]
```

> If `books.json` is present, the app will load it. If not, it falls back to the inline sample.

## Deploy to GitHub Pages
1. Create a new repo on GitHub and upload these files (drag & drop in the web UI is fine).
2. Commit to the **main** branch.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to “Deploy from a branch”; choose **Branch: main** and **/ (root)**. Save.
5. Wait ~1–2 minutes. Your site will be available at `https://<your-username>.github.io/<repo-name>/`.

## Customise
- **Colours**: Tailwind utility classes in `index.html` control colours; search for `bg-`, `text-`, and `from-…/to-…` gradient classes.
- **Fonts**: Currently using **Merriweather** (headings) and **Quicksand** (UI). Change the Google Fonts link in `<head>` if desired.
- **Icons/cover**: Replace `assets/book.svg` with your own image. The app uses it for all items unless you extend the data model.

## Troubleshooting
- Searching locally by opening `index.html` with `file://` may block loading `books.json`. Use GitHub Pages or a local server.
- If no results appear, open the browser console to check for JSON syntax errors.
