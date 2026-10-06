# aura-website

The website of the Aura app, served by GitHub Pages at https://aura-sport.de.

Plain HTML and CSS, no build step. German pages at the root, English pages under `/en/`.

- `index.html`, `en/index.html`: the landing pages, edited here.
- `konto-loeschen/`, `en/delete-account/`: how to delete the account, edited here. Google Play asks
  for this URL in the Data safety form.
- `datenschutz/`, `nutzungsbedingungen/`, `impressum/` and `en/privacy/`, `en/terms/`, `en/imprint/`:
  **generated** from the legal texts of the app, don't edit them here. After changing the texts in the
  app repo, run there (with this repo next to it):

  ```bash
  flutter test tool/website/export_legal_pages.dart --dart-define=OUT=../aura-website
  ```

  and commit the changed pages here.
- `CNAME`: the custom domain for GitHub Pages. `.nojekyll`: serves the files as they are (also
  `.well-known/` for app links later).

No cookies, no tracking, no external resources (system fonts only), see the privacy policy.
