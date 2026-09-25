# A11pro Profit Growth Research Integration — 2026-09

## Research signals
- B2B software discovery is increasingly split between traditional search and conversational/answer-based discovery. G2's June 2026 buyer research reports that more than 80% of buyers sourced recommendations from a chatbot in the prior two years, while evaluation remains a major friction point.
- Buyers increasingly expect transparent pricing logic, ROI evidence, implementation detail, security evidence and material they can take to internal approvers.
- Marketing measurement is moving toward triangulation: tactical attribution + incrementality experiments + MMM. IAB's 2026 State of Data recommends faster MMM refreshes, scenario simulation, automated diagnostics and direct integration into planning workflows.
- Privacy and signal loss make business-owned first-party data increasingly important.
- Enterprise B2B retention/expansion remains a major economic lever; current benchmarks show materially higher NRR for enterprise segments than SMB-focused SaaS.
- Variable-cost products create margin pressure; pricing must expose usage economics and value rather than hide cost.

## A11pro operating changes

### 1. Answer-discovery layer
Create an Answer Presence surface that tracks category, problem and comparison queries; vendor/entity mentions; factual accuracy; proof availability; citation/source coverage; and competitor displacement opportunities. Do not optimize for mentions alone. Connect discovery visibility to qualified enquiries and revenue.

### 2. Evaluation Pack
Every commercial offer should expose outcome, scope, implementation path, pricing logic, expected economics, security/trust evidence, relevant proof, risks/constraints and next action before unnecessary sales friction.

### 3. Measurement Triad
Use attribution for daily optimization, incrementality tests for causal validation on material spend, and MMM/aggregate modeling for portfolio allocation when data maturity justifies it. If methods disagree, create an investigation task.

### 4. Profit unit
Use OFFER × CUSTOMER SEGMENT × SOURCE × PERIOD. Calculate revenue minus direct fulfilment, variable infrastructure/usage, sales, marketing and transaction costs to produce contribution profit; then track CAC, payback, retention, expansion and expected value.

### 5. Capital allocation
Create a recommendation queue: increase, maintain, test, repair, pause, retire. Recommendations never imply execution. Owner approval is required before material spend changes.

### 6. Lifecycle revenue recovery
Cover abandoned enquiry, abandoned checkout, missed contact, dormant customer, renewal risk, expansion and referral opportunities. Record trigger, action, outcome and incremental cost.

### 7. Offer architecture
Maintain explicit variants: entry diagnostic, fixed-scope intervention, implementation, managed operating layer, recurring support and expansion modules. Test price, packaging, contract length and outcome framing independently where possible.

### 8. Margin guard
Gross Margin = (Revenue - direct variable delivery cost) / Revenue. Use an owner-approved minimum margin threshold and flag pricing, packaging or delivery changes when economics deteriorate.

### 9. Evidence-first conversion
Use verified results, before/after measurement, implementation artifacts, security/control evidence, customer-approved proof and reproducible tests. No invented metrics, logos, testimonials or live-status claims.

### 10. Decision latency
SIGNAL → DIAGNOSIS → PROPOSED ACTION → OWNER APPROVAL → EXECUTION → VERIFICATION → LEDGER.

## Data model
campaigns, offers, channels, segments, opportunities, customers, experiments, attribution_events, incrementality_tests, profit_snapshots, lifecycle_events, pricing_variants, evidence_items, allocation_decisions.

## Core surfaces
Profit Radar; Demand & Answer Presence; Conversion Observatory; Revenue Recovery; Retention/Expansion; Experiment Lab; Capital Allocation; Evidence Ledger; Margin Guard; Executive Decision Queue.

## Security / governance
Separate public marketing from private economics, customer-level data, credentials and operational evidence. Preserve owner approvals and decision evidence.

## Implementation sequence
1. schema + evidence contracts
2. profit/event ingestion
3. Profit Radar + Decision Queue
4. Answer Presence + Evaluation Pack
5. lifecycle recovery
6. experiment/incrementality
7. aggregate MMM/scenario planning
8. verified commercial deployment

No automated background process is required. Execution is event-driven or manually initiated unless explicitly enabled by the owner.
