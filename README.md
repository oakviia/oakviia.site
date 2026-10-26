# oakviia.com — GitHub Pages site

## Files
```
index.html  contact.html  style.css  CNAME
images/
  hero.jpg        ← the sunset photo of oakviia singing
  logo-white.png  ← white logo (transparent background) — sits on the photo
  logo-black.png  ← black logo (transparent background) — used in the nav
```
Images are already included. To swap one, keep the same file name.

## Who should own the GitHub account?
**Recommended: oakviia makes her own free GitHub account.** The site, domain and history stay hers.
A helper can still do all the work: she adds them as a **collaborator**
(repo → Settings → Collaborators → Add people). They can push changes; she keeps ownership.

(Someone else *can* host it on their account, but then the site lives at their username,
and if they leave or lose access she loses control. Not recommended.)

## Publish
1. Sign up at github.com (e.g. username `oakviia`).
2. New repository → name it `oakviia.github.io` → Public → Create.
3. "uploading an existing file" → drag in all files + the `images` folder → Commit.
4. Settings → Pages → Source: *Deploy from a branch* → `main` / `(root)` → Save.
5. Within a minute it's live at `https://oakviia.github.io`.

## Move oakviia.com from WordPress to GitHub
Find where the domain's DNS is managed (WordPress.com → Upgrades → Domains if registered there,
or GoDaddy/Namecheap/Squarespace etc.).

1. Remove the existing WordPress A records / any "point to WordPress" setting.
2. Add these records:

| Type  | Host/Name | Value               |
|-------|-----------|---------------------|
| A     | @         | 185.199.108.153     |
| A     | @         | 185.199.109.153     |
| A     | @         | 185.199.110.153     |
| A     | @         | 185.199.111.153     |
| CNAME | www       | oakviia.github.io   |

3. GitHub repo → Settings → Pages → Custom domain: `oakviia.com` → Save
   (the included `CNAME` file does this too).
4. Wait for DNS (minutes to ~24h), then tick **Enforce HTTPS**.
5. Optional but wise: Settings (her account) → Pages → **Verify** the domain to prevent takeover.

⚠️ Before switching: if she uses email @oakviia.com, keep any **MX / TXT** records untouched.
Download/export anything from WordPress she wants to keep first.

## Contact
Contact uses an email button (oakviia@gmail.com) and the Google Form. The older built-in form is saved in `_archive/`.
