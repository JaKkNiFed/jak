# Jak — Link Hub Site

A single-file static site (`index.html`) styled around your cyber-eye logo. No build tools, no dependencies beyond two Google Fonts — just open the file in a browser to preview it.

## 1. Before you publish

Open `index.html` in a text editor, scroll to the `<script>` near the bottom, and edit the `SOCIAL_LINKS` array — swap each `"#"` for your real Instagram / X / YouTube / Twitch / TikTok URLs, and replace the placeholder email. Buttons still pointing at `"#"` show a small orange **"edit me"** tag so they're easy to spot; once every link is real, you can remove that tag system by deleting the `show-placeholders` class on the `<body>` tag.

The Discord community links and the logo image are already filled in from your Linktree — no edits needed there unless something's changed.

## 2. Hosting — GitHub Pages (recommended to start)

1. Create a free GitHub account at github.com if you don't have one.
2. Create a new repository (e.g. `jak-site`) — public, no need to add a README since you already have one.
3. Upload `index.html` (and `README.md` if you want) into that repo using GitHub's "Add file → Upload files" button in the browser — no command line needed.
4. Go to the repo's **Settings → Pages**.
5. Under "Build and deployment," set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
6. Wait about a minute, then refresh that settings page — it'll show your live URL, something like `https://yourusername.github.io/jak-site/`.

## 3. Hosting — Cloudflare Pages (if you want it later, or want the speed boost)

1. Push the same GitHub repo (steps above) first — Cloudflare Pages deploys from a GitHub repo, it doesn't take a raw file upload as easily.
2. Sign up at dash.cloudflare.com → **Workers & Pages → Create → Pages → Connect to Git**.
3. Authorize Cloudflare to access your GitHub account, pick the `jak-site` repo.
4. Build settings: framework preset **None**, build command **(leave blank)**, output directory **/** (root). Save and deploy.
5. Cloudflare gives you a `*.pages.dev` URL immediately; you can attach a custom domain later for free under the same project.

## 4. Custom domain (optional, either host)

Both GitHub Pages and Cloudflare Pages let you attach a domain you own (e.g. `jak.dev`) for free — you just point the domain's DNS at the host. Cloudflare is the easier of the two if your domain's DNS is already on Cloudflare.
