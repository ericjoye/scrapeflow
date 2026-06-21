# ScrapeFlow — Business State

> Current status, hypotheses, and active experiments.
> Updated by OWL each iteration.

## What
Chrome extension: AI-powered web scraping & data export. Users click on page elements to capture structured data, export to CSV/JSON.

## Maturity: v1.0 Built, Pre-Launch

## Revenue Model
- Free: 50 rows/month, CSV only
- Pro: $9/month — unlimited rows, JSON export, AI auto-detection
- Team: $19/month — everything + scheduling + priority support

## Current Metrics
```json
{
  "installs": 0,
  "active_users": 0,
  "free_users": 0,
  "pro_users": 0,
  "team_users": 0,
  "mrr": 0,
  "arr": 0,
  "conversion_rate": null,
  "churn_rate": null
}
```

## Status
- ✅ v1.0 code complete (14 files, 7 commits)
- ✅ Landing page built (`/landing/index.html`)
- ✅ CWS listing assets ready (description, privacy policy, screenshots guide, metadata)
- ✅ Options page with license activation
- ❌ Not published to Chrome Web Store (needs $5 fee)
- ❌ Not tested in Chrome by Eric
- ❌ No payment integration (Stripe) — license keys are manual for now
- ❌ No custom domain or hosting for landing page

## Active Hypotheses
1. Free tier (50 rows) is enough to get installs but limited enough to convert to Pro
2. AI auto-detection is the key differentiator vs. manual scraping tools
3. Chrome Web Store is the primary distribution channel (free organic traffic)

## Next Experiments
1. Publish to CWS → measure install rate over 14 days
2. A/B test landing page headline on conversion
3. Add Stripe integration for self-serve Pro upgrades
4. Post on Product Hunt for launch day traffic

## Blockers
- Eric needs to pay $5 CWS developer fee
- Eric needs to test extension in Chrome
- No Stripe account set up for payment processing
