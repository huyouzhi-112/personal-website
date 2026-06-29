# youzhihu.com — personal website

A simple, single-page personal site. No build step, no framework — just `index.html`
and `styles.css`. You can open `index.html` in any browser to preview it.

```
Personal Website/
├── index.html     ← all the text/content lives here
├── styles.css     ← colors, fonts, layout (leave alone unless changing design)
├── images/        ← put your product photos / videos here (create this folder)
└── README.md      ← this file
```

---

## 1. Push to GitHub

Open **Terminal**, then run these (replace `YOUR-USERNAME` and the repo name with
what you created on GitHub):

```bash
cd "/Users/huyouzhi/Claude/Projects/Personal Website"
git init
git add .
git commit -m "First draft of personal website"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/personal-website.git
git push -u origin main
```

After this, your code is on GitHub. To publish future changes:

```bash
git add .
git commit -m "describe what you changed"
git push
```

---

## 2. Deploy with Cloudflare Pages (free)

Since your domain is already on Cloudflare, this is the smoothest path.

1. Go to the **Cloudflare dashboard** → **Workers & Pages** → **Create** → **Pages**
   → **Connect to Git**.
2. Select your `personal-website` repo.
3. Build settings: **Framework preset = None**, leave the build command **empty**,
   and set **Build output directory = `/`** (the root). Click **Save and Deploy**.
4. You'll get a free URL like `personal-website.pages.dev` within a minute.

Every time you `git push`, Cloudflare rebuilds automatically.

---

## 3. Connect youzhihu.com

In the Pages project → **Custom domains** → **Set up a domain** → enter
`youzhihu.com` (and add `www.youzhihu.com` too). Because the domain is already in
your Cloudflare account, the DNS records are added for you in one click. Give it a
few minutes to go live with HTTPS.

---

## 4. Editing your content later

Everything you'll want to change is in **`index.html`**, marked with `TODO` comments:

- **Add product images/videos** — create an `images/` folder, drop files in, then
  replace the `<div class="media-placeholder">…</div>` block for each product with
  `<img src="images/your-file.jpg" alt="..." />` (or a `<video>` tag).
- **Research papers** — under each product's *Related research*, replace the
  placeholder `<li>` lines with real APA citations linked to each paper. The
  "View all publications on Google Scholar" button is already wired to your profile.
- **Michael Kors internship** — in the About timeline, fill in the exact role title
  and dates where the placeholder entry is.

Search `index.html` for the word `TODO` to find every spot that's waiting on you.
