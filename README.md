# TAG Government Solutions — proof of concept

A dependency-free, responsive single-page website based on the supplied navy-and-gold collateral. The official PDF's TEGEX artwork is intentionally displayed temporarily while page copy and copyright use TAG Government Solutions, as requested.

The latest revision uses larger, higher-contrast text, 16–17px service bullets, metallic-gold accents, and the bold icon medallions extracted directly from the supplied reference. The Capitol-and-flag image is a cleaned derivative of the supplied artwork with stray lettering removed. No independent stock imagery is used. The page has no visible builder credit.

## Run locally

```sh
python3 -m http.server 3000 --bind 0.0.0.0 --directory site
```

Open http://localhost:3000. Deploy the contents of `site/` to any static host. No installation, compilation, database, or backend is required. All asset URLs are relative so the page works under a GitHub Pages repository path or at a custom-domain root.

## Structure

`site/index.html` contains the semantic page and dialogs; `site/styles.css` contains responsive navy/gold styling; `site/app.js` contains accessible demo interactions. `site/assets/` contains the supplied PDF logo, cropped reference medallions, cleaned Capitol image, and downloadable original brand sheet. `docs/` contains migration instructions and production recommendations.

## Demonstration boundaries

The login opens an explanation only; it does not accept credentials or authenticate. The contact dialog starts with an email address, progressively reveals name, organization, service, and message fields, and discards entries on completion or dismissal. It has no form action, network call, analytics event, cookie, browser storage, or server submission. Explicit demo notices appear before entry and on completion. The working footer mailto link separately opens the visitor's email app; it is not a submission backend.

Do not enter sensitive information. The demo notices are not a production privacy policy. Hosting providers may retain ordinary request logs.

## Hosting and deployment

The source repository is `iamabotama/taggovsolutions`; the Pages repository is `iamabotama/taggovsolutions.io`. The source repository's existing `.github/workflows/deploy-pages.yml` runs on pushes to `main`, selects `site/` for this dependency-free version, and copies the deployable files to the Pages repository. It uses the repository's `PAGES_DEPLOY_KEY` secret and preserves Git metadata and the custom-domain file during synchronization.

The workflow sets `taggovsolutions.io` as its custom-domain value. Actual public hosting still depends on a successful workflow run, Pages configuration, and correct DNS. See `docs/GITHUB_PAGES.md`. This revision does not change the deployment workflow, Pages settings, or DNS.

No credentials belong in source files, public repositories, build output, or Git URLs. Replace the token shared in chat with a fine-grained credential limited to the intended repositories and required operations.
