# What TAG Government Solutions needs before production

## Confirm the brand and contact details

The PDF says **TEGEX Government Solutions**; the reference and page copy say **TAG Government Solutions**. The PDF logo is used exactly as requested for now. Confirm the final legal/business name and provide a matching approved vector logo, rather than combining two logos without brand approval. The PDF's official navy `#0F2447` and gold `#BE9042` guide the design.

Confirm `info@taggovsolutions.com`, the `.com` destination, Florida headquarters wording, and whether the `.io` domain should remain a proof of concept. The contact address and company URL come from the supplied reference; they are not independently verified as active. A public business phone number and named point of contact would make the page more useful to procurement teams.

## Add verified procurement information

If applicable and approved for publication, provide the legal entity, UEI, CAGE code, NAICS codes, current contract vehicles, certifications, service areas, and a properly branded downloadable capability statement. None of these have been invented. Add approved past-performance examples and specific service scopes; avoid implying government endorsement or displaying agency/customer logos without permission.

The downloadable PDF in this demo is the supplied brand sheet, not a procurement capability statement. The Capitol image is extracted from the supplied reference and is only 545 × 320 pixels. Supply a licensed high-resolution original for a sharper production hero. Confirm rights to all supplied artwork.

## Replace demo contact handling and login

The floating contact dialog is intentionally client-side only. Valid email input reveals additional fields; completion or dismissal clears all entries without sending anything. The notice makes this explicit. The email footer link opens a visitor's own email application and is a separate real action.

For production, choose a CRM or form service, the receiving mailbox, consent language, retention rules, spam/rate-limit protection, server-side validation, and truthful success/failure messages. Test delivery and error handling before removing demo labels. Never expose service credentials in client code. Discourage classified, controlled, sensitive procurement, or other restricted information in a public inquiry form.

Define who will use a future client portal and what data it will contain before adding authentication. Prefer a maintained identity provider with appropriate access controls and MFA. The current Login button is only an explanatory modal and never asks for credentials.

## Accessibility, privacy, and security

The implementation includes semantic headings, a skip link, native keyboard-accessible dialogs, focus restoration, visible focus states, labeled fields, validation messages, reduced-motion support, and mobile layouts. Before production, perform browser/device and screen-reader checks against the final content and WCAG 2.2 AA criteria. Do not treat this proof of concept as a formal accessibility certification.

Have the business approve a production privacy policy and, where appropriate, terms and accessibility statement. The current “About this demo” notice is deliberately not presented as a legal privacy policy. Hosting providers may keep ordinary request logs even though the form does not store entries. Optional platform site analytics are disabled for this demo; this is not a promise that every hosting/platform log or badge measurement is disabled.

Revoke the GitHub token shared in chat. Use a replacement fine-grained token limited to the intended repositories and necessary operations, or a properly scoped GitHub integration. Enable HTTPS on the final domain, keep secrets out of repositories, and review production security headers and access controls with the eventual hosting environment.

## Search, analytics, and maintenance

This temporary proof of concept is marked not to be indexed. When launching the approved public site, remove the indexing block, add the final canonical URL, an appropriate social-preview image, a sitemap, and factual organization metadata. Add analytics only after deciding what to collect and updating privacy/consent disclosures.

Agree who owns content updates and deployments. The source repository and Pages repository are separate copies: future changes must be copied or linked by a deliberate deployment workflow. Keep the Pages `CNAME` once added, and preserve existing Git histories. The companion GitHub Pages guide provides the later domain and hosting steps.
