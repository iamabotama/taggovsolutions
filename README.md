# TAG Government Solutions — proof of concept

A dependency-free, responsive single-page website based on the supplied navy-and-gold collateral. The official PDF's TEGEX artwork is intentionally displayed temporarily while page copy and copyright use TAG Government Solutions, as requested.

## Run locally

```sh
python3 -m http.server 3000 --bind 0.0.0.0 --directory site
```

Open http://localhost:3000. Deploy the contents of `site/` to any static host. No installation, compilation, database, or backend is required. All asset URLs are relative so the page works under a GitHub Pages repository path or at a custom-domain root.

## Structure

`site/index.html` contains the semantic page and dialogs; `site/styles.css` contains responsive navy/gold styling; `site/app.js` contains accessible demo interactions. `site/assets/` contains the user-supplied PDF logo, security badge, Capitol crop, and downloadable original brand sheet. `site/manus-routes.json` declares the single page. `docs/` contains migration instructions and production recommendations.

## Demonstration boundaries

The login opens an explanation only; it does not accept credentials or authenticate. The contact dialog starts with an email address, progressively reveals name, organization, service, and message fields, and discards entries on completion or dismissal. It has no form action, network call, analytics event, cookie, browser storage, or server submission. Explicit demo notices appear before entry and on completion. The working footer mailto link separately opens the visitor's email app; it is not a submission backend.

Do not enter sensitive information. The demo notices are not a production privacy policy. Hosting providers may retain ordinary request logs.

## Hosting and repositories

Temporary hosting is through Manus. The source is copied to `iamabotama/taggovsolutions`, and the deployable contents of `site/` are copied to `iamabotama/taggovsolutions.io`. These are separate copies, not the managed website's canonical repository. GitHub Pages and custom-domain activation are deferred until the user is ready to move hosting. See `docs/GITHUB_PAGES.md`.

No credentials belong in these files, public repositories, build output, or Git URLs. Revoke the token shared in chat after delivery and use a replacement fine-grained credential limited to the two intended repositories.
