# Wild Vows — Marketing & legal site

Static HTML for **https://wildvows.app** (GitHub Pages + custom domain).

## What’s here

| Path | Purpose |
|------|---------|
| `index.html` | Home |
| `privacy/index.html` | Privacy policy (canonical: `/privacy/`) |
| `terms/index.html` | Terms of use incl. subscriptions & Apple EULA reference |
| `contact/index.html` | Contact form (emails via FormSubmit) |
| `thanks/index.html` | Post-submit thank-you |
| `privacy.html`, `terms.html`, `contact.html` | Short redirects to `/privacy/`, `/terms/`, `/contact/` |
| `css/styles.css` | Shared styles |
| `CNAME` | Custom domain (`wildvows.app`) |
| `.nojekyll` | Disables Jekyll for predictable static serving |
| `robots.txt` | Crawl rules + sitemap pointer |
| `sitemap.xml` | Sitemap for search engines |
| `404.html` | GitHub Pages custom “not found” page |

## Deploy on GitHub Pages

1. Create a GitHub repo (e.g. `wildvows-website`) and push **this folder’s contents** to the repo root (or use `/docs` if you set Pages to that folder).
2. **Repository → Settings → Pages**
   - **Build and deployment:** Deploy from a branch, pick `main` (or your default), folder **/ (root)** or **/docs** as configured.
3. **Custom domain:** enter `wildvows.app` and save. Keep the **`CNAME`** file in the repo with exactly `wildvows.app`.
4. In your DNS (where `wildvows.app` is registered), add the records GitHub shows (typically **A** / **AAAA** to GitHub Pages, or a **CNAME** to `YOURUSER.github.io` for a `www` subdomain if you use one).
5. Wait for DNS + HTTPS; GitHub will provision a certificate once the domain verifies.

## Contact form → `info@hadalcore.com`

The form uses **[FormSubmit](https://formsubmit.co)** (no backend required).

1. Deploy the live site.
2. Submit the contact form once from **https://wildvows.app/contact/**.
3. Open **`info@hadalcore.com`** and complete FormSubmit’s **one-time verification** for that address.
4. After verification, new submissions are delivered to that inbox.

Optional: use FormSubmit’s dashboard for extra spam controls after the domain is verified.

## Apple App Store Connect

Use stable HTTPS URLs (these match the canonical links in each page):

| Field | Suggested URL |
|--------|----------------|
| **Privacy Policy URL** | `https://wildvows.app/privacy/` |
| **Terms of Use (EULA) URL** | `https://wildvows.app/terms/` |
| **Marketing / support** | `https://wildvows.app/` |
| **Contact** | `https://wildvows.app/contact/` |

The **Terms** page includes subscription disclosure (auto-renewal, cancellation, billing, managing subscriptions, trial/refund pointers) and references Apple’s **Standard EULA** where appropriate—have counsel review before relying on it in review.

**App Store product page:** replace the placeholder App Store link on the home page (`index.html`) with your real listing URL when the app is live.

## Local preview

```bash
cd wildvows-website
python3 -m http.server 8080
# open http://localhost:8080
```

## Legal note

Privacy and terms are starter templates for a small app publisher (Hadalcore). They are **not** legal advice; have them reviewed for your actual data practices, jurisdictions, and paid features.
