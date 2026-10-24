# Clearline Bookkeeping — marketing site

Static, no-build marketing website for a QuickBooks setup/cleanup/monthly-bookkeeping business. Plain HTML/CSS/JS, no dependencies, no backend.

## Before launch, update:

- **Business name** — currently a placeholder, "Clearline Bookkeeping". Find & replace it across `index.html` and update the `<title>`/meta description.
- **Contact info** in `index.html` (`#contact` section) and `script.js` (`CONTACT_EMAIL`):
  - Email is set to `ericlipkind@verizon.net`.
  - Phone and service area are left as bracketed placeholders — fill them in or remove the `<li>` if you don't want to list them.
- **Pricing** in the `#pricing` section — the numbers are reasonable starting points for a solo QuickBooks ProAdvisor but should reflect your actual rates.
- **Testimonials** — the three quotes are placeholders, clearly labeled. Swap in real client feedback once you have some, or remove the section until then.
- **Credentials/trademark language** — the "QuickBooks Online Certified" claim in the hero should only stay if you are actually a certified QuickBooks ProAdvisor. The footer already includes a standard disclaimer that this business isn't affiliated with Intuit, which you should keep regardless.

## How the contact form works

There's no backend. Submitting the form builds a `mailto:` link pre-filled with the visitor's details and opens the user's email client. If you'd rather use a real form backend (e.g. Formspree, or your own serverless function), swap out the submit handler in `script.js`.

## Deploying

This is a static site: `index.html`, `styles.css`, `script.js` at the repo root, nothing to build.

- **GitHub Pages**: in the repo's Settings → Pages, set the source to the `main` branch, root folder. The site will be live at `https://<username>.github.io/bookkeeping-website/` (or a custom domain you attach).
- **Any static host** (Vercel, Netlify, Cloudflare Pages, etc.): point it at this repo with no build command and a publish directory of `/`.
