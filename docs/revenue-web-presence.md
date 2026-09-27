# MindReply Revenue Web Presence

## Deployment policy
This is a revenue architecture and implementation specification. Never claim production readiness, live payments, active subscriptions, real-time metrics, or successful deployments unless verified.

## Hosting
Current deployment direction: Cloudflare / ResellerPro. Do not prescribe Vercel as the default.

## Revenue surfaces
- Pricing and plan comparison.
- Protected account/dashboard surfaces.
- Upgrade prompts tied to real usage or entitlement state.
- Subscription, usage-based, one-time purchase, and referral/commission models where actually implemented.
- Revenue reporting based on verified payment and subscription data.

## Payment safety
- Keep payment credentials server-side and out of source control.
- Use signed webhook verification and idempotent processing.
- Record payment events in an auditable ledger.
- Do not trigger irreversible payouts or fulfillment from an unverified event.
- Keep live billing disabled until explicit owner approval and successful test-mode verification.

## Product entitlements
Plans and limits must be represented as server-side entitlements, not only UI conditions. Upgrade prompts must reflect actual account state and real limits.

## Metrics
Where data exists, track MRR, ARR, active subscriptions, churn, LTV, CAC, and ARPU with explicit calculation definitions and source timestamps. Never fabricate projections or present assumptions as observed revenue.

## Growth experiments
Upsell, onboarding, retention, win-back, referral, and usage-limit flows may be implemented as experiments. Avoid hard-coded conversion claims unless supported by measured data.

## Testing
Before live launch: verify products/prices; test checkout; verify webhook signatures and idempotency; verify ledger reconciliation; verify entitlements; verify cancellation/refund handling; verify public Terms and Privacy pages; obtain explicit owner approval before enabling live billing.

## Multi-app reuse
ResellerPro, Nowline, Market Intelligence, OTA Suite, and future apps should consume a common revenue/entitlement contract where practical rather than duplicating billing logic.