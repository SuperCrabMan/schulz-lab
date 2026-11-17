# Schulz Lab — website

A fast, responsive, accessible lab website for the Schulz Lab at the University of Missouri. No frameworks, subscriptions, compilation, or paid hosting needed.

## See it on your computer first

Open `index.html` in Chrome, Safari, or Firefox. If you want to preview through a local web server instead, run `python3 -m http.server 8000` in this folder and visit `http://localhost:8000`.

## Publish on GitHub Pages — beginner method (no coding software)

1. Go to https://github.com and sign in (or create a free account).
2. Click the **+** at the top right, then **New repository**.
3. Name the repository `schulz-lab` (or another name); select **Public**; click **Create repository**.
4. On the new repository page, select **uploading an existing file** (or **Add file > Upload files** if this option is shown).
5. **Unzip the downloaded project first.** Upload the *contents* of the `schulz-lab-website` folder, not the ZIP itself. GitHub must show `index.html` in the repository's top level. Ensure the `assets` folder and its SVG files are uploaded too. If GitHub's web upload does not preserve folders, upload the two SVG files using **Add file > Create new file** and name each `assets/favicon.svg` and `assets/social-card.svg`, pasting the SVG content from the downloaded files.
6. Scroll down and click **Commit changes**.
7. Open **Settings** in your repository → **Pages** (in the left sidebar).
8. Under **Build and deployment**, select **Deploy from a branch**. Choose branch **main** and folder **/(root)**, then click **Save**.
9. When publishing completes, return to **Settings → Pages**. Your site URL will be shown. It normally looks like `https://YOUR-USERNAME.github.io/schulz-lab/`.
10. Test your site on a phone and a computer. Send the link to colleagues for proofreading before sharing broadly.

> GitHub Pages can take several minutes to show the first version. If it shows a 404, confirm that the repository is public, Pages uses `main` / `/(root)`, and `index.html` is in the top level rather than nested inside a folder.

## Make changes later

- In GitHub, open `index.html` and click the **pencil** icon (Edit this file). Change the words and click **Commit changes**. The live site will update after GitHub republishes it.
- `styles.css` changes colors, layout, and fonts.
- `script.js` is optional small functionality for the mobile menu and copyright year.
- To add a lab member, copy the HTML block beginning `<div class="person-feature">` in `index.html`, paste another block below it, and replace name, initials, and description. Or keep the page streamlined with only the PI.
- To add a paper, copy one `<a class="pub-row" ...>...</a>` item, replace its link, year, title, authors, and journal; keep newest first.
- To change the email address, search all files for `schulzd@missouri.edu`.
- To change the main heading, search `The nervous system` in `index.html`.

## Important prelaunch edits

- **Verify** your team's names, titles, publications, research directions, and whether you are recruiting before sharing broadly. This draft deliberately omits the old Wix member list rather than treating it as current.
- The selected publications are manually curated; the Google Scholar button points to the current listing.
- Add photos **only if you have permission** to use them; you can add an `<img>` or replace the designed neuron illustration if desired.
- The prospective-student note invites inquiries, **not** a guarantee that a funded position exists.
- The Google Fonts stylesheet requires internet. The page still works with Georgia/Arial fallback fonts offline.
- If you want a custom domain later, GitHub Pages supports it; first get the default `.github.io` address working, then follow https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site .

## Search visibility

The site contains descriptive page titles, a summary, heading hierarchy, structured data (schema.org), and public links to your faculty profile and Scholar page. Once published, link to this new URL from your MU faculty page, Scholar profile (if editable), program site, and email signature. You can also submit your site to https://search.google.com/search-console . To identify the *site's canonical URL*, replace the research organization `url` in the JSON-LD block of `index.html` with the actual new GitHub Pages address after launch.

## File list

- `index.html`: full page content and metadata
- `styles.css`: design and mobile responsiveness
- `script.js`: mobile navigation and year
- `assets/favicon.svg`: browser tab icon
- `assets/social-card.svg`: social preview image (some platforms prefer a PNG and an absolute URL)
- `.nojekyll`: ensures GitHub Pages serves the exact static files

## Notes on accuracy

Built using the publicly available University of Missouri faculty page, the prior lab site, the MU Interdisciplinary Neuroscience Program profile, and identifiable journal links. The live Google Scholar list could not be directly retrieved, so the selected papers are **not** claimed to be the latest papers. Check citations and any new manuscripts before launch.
