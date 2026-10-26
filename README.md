# Senda de Palabras

A bilingual English/Spanish portfolio of selected writing, translation, and longer literary projects.

**Live portfolio:** https://andaranda.github.io/senda/  
**Blogger archive:** https://senda-de-palabras.blogspot.com/

## How the site works

This is a lightweight static website built with HTML, CSS, and vanilla JavaScript. It has no framework, package manager, database, or build step.

- `index.html` is the main portfolio, with sections for selected work, writing, longer projects, and a short biography.
- `work.html` provides dedicated work pages, selected by a query parameter (for example, `work.html?work=diamond-sutra`).
- The English/Spanish toggle switches the site's bilingual interface and available descriptions.
- Most work titles open an in-page dialog. Some dialogs show a project description; others load selected published texts from the public Blogger feed.
- “Dharma of Ordinary Things” is a curated collection. The exact Blogger post titles included in it are listed in the `miniSutras` array in `index.html`.
- “No Mountain” has a dedicated description and links to its English and Spanish editions on Amazon. Its cover images are referenced at `images/books/no-mountain-en.png` and `images/books/no-mountain-es.png`.

The portfolio is intentionally selective rather than a complete archive. Work status and language availability are stated on the page. The Blogger site remains the chronological archive for earlier posts.

## Files and content

- `index.html` — homepage, styles, language toggle, portfolio dialogs, and Blogger-feed integration.
- `work.html` — individual work pages.
- `images/` — local images used by the site, including book covers when added.
- `README.md` — project notes and publishing instructions.

Homepage copy, card descriptions, project statuses, and the mini-sutra selection are currently maintained directly in the HTML/JavaScript. Blog-based text is retrieved at runtime from Blogger, so those dialogs need an internet connection and the public Blogger feed to remain available. If the feed cannot be reached, the site shows a fallback message and links visitors to the blog.

## Adding book covers or other images

Keep image files in the repository and reference them with relative paths so they work on GitHub Pages. The No Mountain cover paths currently expected by `index.html` are:

- `images/books/no-mountain-en.png`
- `images/books/no-mountain-es.png`

Git does not track empty folders, so create the `images/books/` path when uploading the first image. Keep the filenames and letter case exactly as written in the HTML.

## Preview locally

Open `index.html` in a browser, or run the project with VS Code's Live Server extension. Some content in dialogs is loaded from Blogger, so test those features with an internet connection.

## Publish with GitHub Pages

The site is intended to publish from the repository's `main` branch and the root folder:

1. Open the repository on GitHub and go to **Settings**.
2. Open **Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Select branch `main` and folder `/(root)`, then save.

After publishing, check the Pages URL, the English/Spanish toggle, work dialogs, dedicated work pages, Blogger-loaded texts, and images on both desktop and mobile. If the site is already live, GitHub Pages normally deploys updates after changes are committed to the publishing branch.

## Maintenance checklist

- Keep the portfolio selective; the Blogger archive is the home for the chronological collection of older posts.
- Check language labels and project statuses when adding or revising work.
- When adding a Blogger post to “Dharma of Ordinary Things,” use its exact published title in the `miniSutras` array.
- Test the language toggle and dialog behavior after editing `index.html`.
- Confirm all referenced images exist in the repository and use the correct path and capitalization.
- Review links and test the layout at mobile widths before sharing significant updates.
