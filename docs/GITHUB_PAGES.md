# Move the proof of concept to GitHub Pages

The source repository now has an existing GitHub Actions deployment workflow. A push to `iamabotama/taggovsolutions/main` selects `site/` and copies the static files into `iamabotama/taggovsolutions.io`. The workflow requires the repository's `PAGES_DEPLOY_KEY` secret and sets `taggovsolutions.io` in the Pages repository's `CNAME`. The revision preserves this workflow and does not change Pages settings or DNS.

## Repository roles

`iamabotama/taggovsolutions` contains the source, with deployable files under `site/`. `iamabotama/taggovsolutions.io` contains those same deployable files directly at repository root. Update the source first and allow the existing workflow to synchronize the Pages repository. If deploying manually instead, copy only `site/` and preserve the Pages repository's `.git` directory and `CNAME`.

There are no dependencies or build steps. Relative asset URLs work at both a repository path and a custom-domain root. `.nojekyll` bypasses Jekyll processing. Do not copy tokens, `.env` files, or managed Git configuration.

## Activate hosting when ready

In the [Pages repository settings](https://github.com/iamabotama/taggovsolutions.io/settings/pages), choose **Deploy from a branch**, then **main** and **/(root)**, and save. The initial address should be `https://iamabotama.github.io/taggovsolutions.io/`. Confirm a successful deployment in the repository Actions tab before advertising it. GitHub recommends branch deployment when no special build is needed.[1]

## Point the owned domain

First verify ownership of `taggovsolutions.io` in your GitHub account's Pages settings, using the TXT record GitHub supplies. Then add `taggovsolutions.io` as the custom domain in the Pages repository settings. For branch publishing GitHub creates a root `CNAME` file; pull that commit before your next deployment.[2]

At your DNS provider, configure four **A** records for the apex host, typically named **@**, with these values:[2]

```text
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

Add a **CNAME** record for **www** pointing to **iamabotama.github.io** — do not include the repository name or an `https://` prefix. Review only conflicting web-hosting records; do not alter mail MX, SPF, DKIM, or unrelated TXT records. Avoid wildcard DNS entries.[2]

After DNS propagation and GitHub certificate provisioning, enable **Enforce HTTPS**. GitHub notes that the option may take up to 24 hours to appear. Check both `https://taggovsolutions.io/` and `https://www.taggovsolutions.io/`, plus the styles, logos, PDF download, and dialog interactions.[2]

## Before making this a production website

The page intentionally contains `noindex, nofollow` metadata and a robots exclusion for this proof of concept. Remove those only when the branding, final destination, legal content, and real contact handling are approved. Add canonical and social-preview URLs for the actual live production domain rather than the temporary host.

## References

[1]: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site "GitHub Docs — Configure a publishing source"
[2]: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site "GitHub Docs — Manage a custom domain"
