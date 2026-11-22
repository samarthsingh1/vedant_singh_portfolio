# Vedant Singh: portfolio

A one-page professional portfolio for Vedant Singh, LL.M. candidate at Columbia Law School (2027) and former Corporate / M&A and Private Equity associate at AZB & Partners and Trilegal.

All content comes from `assets/Vedant_Singh_Resume_2026.pdf`. Nothing on the page goes beyond what the CV says.

## What's on the page

| Section | Source in the CV |
| --- | --- |
| Hero | Name, practice area, Columbia LL.M., prior firms, bar status |
| Representative matters | Page 2, all 13 matters in the CV's three groups |
| Experience | AZB & Partners, Trilegal (associate and intern) |
| Education | Columbia Law School, Jindal Global Law School |
| Credentials | Bar admissions, CIPP/E, deal technology, publications, policy work, languages, interests |
| Contact | Email, location, CV download |

The design uses the M&A deal tombstone: the hero and each representative matter are framed tombstones. The contact section is laid out as an agreement signature block.

## Structure

```
index.html                 the whole site (static HTML, no JavaScript)
favicon.svg
assets/css/styles.css      design tokens, layout, light and dark themes, print styles
assets/fonts/              self-hosted Libre Caslon and Libre Franklin (SIL Open Font License)
assets/Vedant_Singh_Resume_2026.pdf
```

There's no build step and no dependencies.

## Preview locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Editing content

Everything lives in `index.html`.

- **Add a matter:** copy one `<li>` inside the relevant `<ul class="deals">` and update the group's "N matters" count. Leave out `deal__value` when there's no public figure. The grid resizes on its own, and a lone tombstone at the end of a row widens to fill it.
- **Update the CV:** replace `assets/Vedant_Singh_Resume_2026.pdf`. If you rename the file, also update the three links that point to it.
- **Colours and type:** the tokens at the top of `assets/css/styles.css` (`:root`) control the palette for both light and dark mode.

## Privacy

- The phone number from the CV is deliberately **not** on the web page. The downloadable PDF still contains it. Remove or replace the PDF before publishing if you don't want the number public.
- Unnamed clients stay anonymised exactly as they are in the CV.

## Deploying

The site is static, so any static host works:

- **GitHub Pages:** Settings → Pages → Deploy from branch → `main` / root. A private repository needs GitHub Pro, Team or Enterprise to publish to Pages. The published site is public even when the repository is private.
- **Netlify, Vercel or Cloudflare Pages:** import the repository with no build command and set the publish directory to `/`.

## Licences

The fonts are licensed under the SIL Open Font License 1.1; see `assets/fonts/LICENSE-*.txt`.
