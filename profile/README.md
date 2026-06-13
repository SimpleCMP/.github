<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/SimpleCMP/.github/main/profile/logo-dark.svg">
  <img alt="SimpleCMP" src="https://raw.githubusercontent.com/SimpleCMP/.github/main/profile/logo-light.svg" width="320">
</picture>

**An open-source Consent Management Platform with auto-detection, a shared service database, and a CMS bridge.**

SimpleCMP helps websites collect, document, and honour user consent for cookies and trackers without locking integrators into a vendor SaaS. It ships as a small Lit-based web-component library that runs anywhere, plus first-party integrations for popular CMS platforms.

[**simplecmp.eu**](https://simplecmp.eu) · [Live demo](https://simplecmp.eu/en/demo.html) · [Docs](https://simplecmp.eu/en/docs.html) · [Roadmap](https://simplecmp.eu/en/roadmap.html)

---

## What makes SimpleCMP different

- **Record mode** — discover the trackers your own site actually loads, instead of writing a service list by hand.
- **Shared service database** — curated, versioned classifiers for the most common trackers; no proprietary lookup service.
- **CMS bridge** — a documented webhook protocol (HMAC-signed, schema v2) that lets any CMS push detections into the consent backend and pull banner / service config back out.
- **Headless engine** — the same JS core runs in plain HTML, in a CMS plugin, in a SPA, or behind a server-rendered template. Pick the integration layer that fits.
- **Click-to-enable embeds** — blocked YouTube, Vimeo, or Maps embeds get an in-place consent prompt instead of disappearing silently.
- **Universal pre-consent blocking** — block third-party scripts, iframes, and pixels (and optionally stylesheets such as Google Fonts) before consent, with click-to-enable recovery — no per-embed markup required.
- **Region-aware regimes** — drive opt-in (GDPR), opt-out (US / CCPA "Do Not Sell"), or no-banner behaviour per visitor region.
- **Google Consent Mode v2** — signal a site's existing Google tags from the consent state; SimpleCMP never loads gtag/GTM itself.
- **Compliance audit** — built-in DSGVO / WCAG checks (equal-prominence buttons, contrast, accessible names) you can run against a live banner.
- **GDPR-default UX** — "Reject all" sits equal to "Accept all"; no dark patterns, no pre-checked categories.
- **Browser consent signals** — honours `Sec-GPC` (Global Privacy Control) where applicable.
- **26 language packs** out of the box — German, English, French, Italian, Spanish, and more.

## Repositories

| Repo | What it is | Status |
|---|---|---|
| [`simplecmp`](https://github.com/SimpleCMP/simplecmp) | Core engine: web components, detection, region regimes, Consent Mode v2, compliance audit, CMS-bridge sender | active |
| [`t3-simplecmp`](https://github.com/SimpleCMP/t3-simplecmp) | TYPO3 v14 extension: backend detection triage, service registry + library browser, Theme Designer, managed trackers (Consent Mode v2), webhook receiver | active |
| [`services-library`](https://github.com/SimpleCMP/services-library) | Shared service database: 360+ curated tracker classifiers as JSON, plus a thin PHP loader | active |
| `wp-simplecmp` | WordPress plugin: settings page, block-editor trigger, detection dashboard, multisite, WPML / Polylang | planned — see [the WordPress page](https://simplecmp.eu/en/wordpress.html) |

## Getting started

The fastest way to see what SimpleCMP does is the [live demo](https://simplecmp.eu/en/demo.html) — banner, consent modal, click-to-enable embeds, and the recorder all run in your browser.

For projects:

- **TYPO3:** `composer require simplecmp/t3-simplecmp` — see the [TYPO3 page](https://simplecmp.eu/en/typo3.html) for configuration.
- **Plain HTML / SPA / custom backend:** drop the bundle in, point it at your service config, done.
- **WordPress:** follow [the WordPress page](https://simplecmp.eu/en/wordpress.html) — the plugin is in planning, but the headless engine works today.

## Contributing

Issues and pull requests are welcome on any of the repositories above. The source, configuration keys, JSON schemas, and ADRs are all in English; the user-facing documentation is currently German-first while the English translation catches up — [help with translation](https://github.com/SimpleCMP/simplecmp/issues) is genuinely appreciated.

## License

BSD 3-Clause — permissive, commercial-friendly, no copyleft. Use SimpleCMP in client work, in proprietary products, in agency stacks, wherever you need it.

## Behind the project

SimpleCMP is built and maintained by [**WapplerSystems**](https://wappler.systems), a TYPO3 agency operating since 2009. The platform grew out of our day-to-day work integrating consent management into production TYPO3 sites — migrating away from OneTrust, Usercentrics, and CCM19, dealing with multilingual sites, and trying to make consent audits a thing humans can actually run.

If you need help with a SimpleCMP integration, a custom theme, a GDPR audit, or editor training, [get in touch](https://wappler.systems/kontakt).
