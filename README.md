# fchambo.com

Personal website for Facundo Chambó: Fractional CTO/CPO, technology advisory for VCs and boards, and product engineering for early-stage companies.

Plain static HTML/CSS. No build step.

## Structure

| Path | Page |
| --- | --- |
| `index.html` | Home |
| `fractional-cto-cpo/` | Fractional CTO/CPO service |
| `technology-advisory-vc-board/` | Technology advisory for VCs & boards |
| `product-engineering-startups/` | Product engineering for early-stage companies |
| `assets/` | Styles, favicon, Open Graph image |
| `sitemap.xml`, `robots.txt`, `404.html` | SEO and hosting files |
| `tools/og-image.html` | Source for `assets/og-image.png` (screenshot at 1200x630) |

## Run locally

```sh
python3 -m http.server 8000
```

## Domain

URLs assume `https://fchambo.com`. To use another domain:

```sh
grep -rl 'https://fchambo.com' --include='*.html' --include='*.xml' --include='*.txt' . | xargs sed -i '' 's#https://fchambo.com#https://YOUR-DOMAIN#g'
```

## Deploy

Any static host works (GitHub Pages, Cloudflare Pages, Netlify). For GitHub Pages, enable Pages on `master` / root and add a `CNAME` file with your domain.

After deploying, submit `sitemap.xml` in Google Search Console and Bing Webmaster Tools.
