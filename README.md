# Schulz Lab website

The entire website is one file: **`index.html`**. It is hosted for free by **GitHub Pages**.
You don't need any software beyond a web browser.

---

## Part 1 — One-time setup (about 15 minutes)

### 1. Create a GitHub account
1. Go to <https://github.com/signup> and create an account.
2. Your **username** will appear in the website address, e.g. username `schulzlab` → `https://schulzlab.github.io`.
   Choose it with that in mind.

### 2. Create a repository (the folder that holds the site)
1. Once signed in, click the **+** in the top-right corner → **New repository**.
2. **Repository name** — choose one of these:
   - `YOURUSERNAME.github.io` (e.g. `schulzlab.github.io`) → the site lives at **https://schulzlab.github.io** ← *recommended, cleanest address*
   - anything else, e.g. `lab-website` → the site lives at `https://YOURUSERNAME.github.io/lab-website`
3. Set it to **Public** (free GitHub Pages requires this).
4. Leave everything else as is and click **Create repository**.

### 3. Upload the website files
1. On the new, empty repository page, click the link **"uploading an existing file"**.
2. Unzip the `schulzlab-website.zip` you downloaded. Drag **`index.html`**, **`README.md`**, and the **`images`** folder into the browser window.
3. Scroll down and click the green **Commit changes** button. ("Commit" is GitHub's word for "save".)

### 4. Turn on GitHub Pages
1. In the repository, click **Settings** (top menu, gear icon).
2. In the left sidebar, click **Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Under **Branch**, choose **main** and **/ (root)**, then click **Save**.
5. Wait 1–2 minutes and refresh the page. A box will show **"Your site is live at …"** with the link.

That's it. The site is live.

---

## Part 2 — Updating the site later

Every edit happens in the browser:

1. Open your repository on github.com and click **`index.html`**.
2. Click the **pencil icon** (✏️ "Edit this file") in the top-right of the file view.
3. Make your change (see recipes below).
4. Click **Commit changes…** → **Commit changes**.
5. The live site updates in about a minute. (If you don't see the change, hard-refresh: Ctrl+Shift+R on Windows, Cmd+Shift+R on Mac.)

Tip: in the editor, press **Ctrl+F / Cmd+F** to jump to the section you want. Each section is marked with a banner comment like `<!-- ===================== PEOPLE ===================== -->`.

### Recipe: add a new publication
Search for `PUBLICATION — copy from here`. Copy that whole `<li class="pub reveal"> … </li>` block, paste it **just below** the `<ol class="pubs">` line (so the newest paper sits at the top), and edit the year, title, authors, journal, and DOI link.

### Recipe: add or remove a lab member
Search for `LAB MEMBER — copy from here`. Copy one `<div class="member reveal"> … </div>` block, paste it next to the others, and edit it.
To remove someone, delete their whole block, from `<div class="member reveal">` through its closing `</div>`.
The two letters in `<div class="avatar">AR</div>` are their initials.

### Recipe: add photos
1. In the repository, open the **`images`** folder → **Add file → Upload files** → upload e.g. `rosete.jpg` → **Commit changes**.
2. In `index.html`, replace the initials with the image:
   `<div class="avatar"><img src="images/rosete.jpg" alt="Arturo Rosete"></div>`
3. To host your own PI photo instead of linking to the Mizzou website, upload `images/schulz.jpg` and change the `src="https://biology.missouri.edu/..."` to `src="images/schulz.jpg"`.

Keep photos under ~500 KB (square for lab members, portrait for the PI).

### Recipe: change colors or fonts
Near the top of `index.html`, under `COLORS & FONTS`, change the values, e.g. `--gold: #f1b82d;`.

---

## Optional extras

- **Custom domain** (e.g. `schulzlab.org`): buy the domain from any registrar, then go to **Settings → Pages → Custom domain** and follow GitHub's instructions. Mizzou IT may also be able to point a `missouri.edu` subdomain at it.
- **Retire the Wix site:** update the "Lab website" link on your Mizzou faculty profile to the new address, and add a link on the Wix home page pointing to the new site.
- **Preview before publishing:** double-click `index.html` on your computer to open it in your browser.

If something breaks after an edit, open the file's **History** (clock icon at the top of the file) to view and restore an earlier version.
