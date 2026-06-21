# ScrapeFlow — Playbook

> Reusable lessons, patterns, and operational knowledge.
> Updated by OWL and agents as lessons are learned.

## Product Patterns

### Chrome Extension Architecture (MV3)
- Content scripts declared in `manifest.json` are auto-injected on page load
- Programmatic injection via `chrome.scripting.executeScript()` requires re-injection after page navigation
- Detection/utility scripts must be listed BEFORE main content script in manifest
- Service worker is ephemeral — don't store state there, use `chrome.storage.local`

### Tier System Pattern
- Storage-based licensing (no server) for v1 — use `chrome.storage.local`
- License key format: `PRO-XXXX-XXXX` (prefix-based validation)
- Feature gating: check tier at action time, not at load time
- Upgrade flow: show banner → link to options page → license entry

### Pricing
- Free: enough to get started, limited enough to feel the pain
- Pro: 2-3x the free limit, unlocks the "wow" feature
- Team: collaboration features, priority support

## GTM Patterns

### Chrome Web Store
- $5 one-time developer fee
- Review process: 1-3 days for new extensions
- Screenshots: 1280x800 recommended, show the popup UI + in-context usage
- Description: lead with the problem, then features, then pricing

### Landing Page
- Dark theme for dev tools (matches the product aesthetic)
- Hero → Problem → Solution → How It Works → Pricing → FAQ → CTA
- Single page, no external dependencies

## Mistakes & Fixes
- **detection.js not injected**: Was missing from manifest content_scripts. Fixed by adding it before content-script.js.
- **Service-worker.js malformed**: Duplicate comment block from patch conflict. Rewrote cleanly.
- **Element ID mismatch**: popup.js referenced IDs not in popup.html. Verified all IDs match.

## TODO
- Add Stripe integration for self-serve upgrades
- Add analytics (even just a simple counter in chrome.storage)
- Create onboarding flow for first-time users
