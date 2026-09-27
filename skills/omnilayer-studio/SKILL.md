---
name: omnolayer-studio
display_name: OmniLayer Studio
description: From one input asset or query, orchestrate versioned media generation, market research, diagnostics, and research synthesis with provenance and explicit approval checkpoints.
---

# OmniLayer Studio

## Purpose
OmniLayer Studio accepts one primary input — logo/image upload, landing-page URL, or plain-text company/query — and coordinates four modular layers. Shared preprocessing extracts brand colors, typography hints, product keywords, landing-page metadata, and named entities into versioned brand tokens.

## Inputs
Required: primary_input.
Optional: target_audience, tone_style, media_constraints, diagnostics_token, research_whitelist, research_blacklist, human_approval_flags.

## Layers
### A — Media Generation
Generate cinematic 3D logo animation and a 15-second vertical UGC ad by default, plus captions and voiceover. Default output is 1080x1920 with neutral en-US voice. Human approval checkpoint: storyboard_draft.

### B — Market Research
Run PESTLE and Porter Five Forces analysis, with charts, HTML/PDF report, and executive summary. Human approval checkpoint: executive_summary_draft.

### C — Web App Diagnostics
Run only when primary_input is a URL and a temporary diagnostics token is explicitly provided. Capture HAR and CPU/memory profiles, validate integrity/reproducibility, and produce prioritized remediation. Do not persist credentials.

### D — Research Synthesis
Search the configured public scientific/industry source scope, synthesize findings, and return structured citations plus source log. Claims must preserve provenance and source attribution.

## Orchestration
1. Preprocess once and version brand_tokens.json.
2. Start A, B, and D in parallel.
3. Start C only when its preconditions are satisfied.
4. Produce v0.1 drafts, then refine to v1 only after applicable human approval.
5. A failed layer must not block other layers; record the failure in manifest.json.
6. Version artifacts using v{major}.{minor}; include invocation ID, timestamp, inputs summary, layer versions, errors, provenance, and artifact checksums.

## Quality controls
Media: visual-artifact detection, audio loudness normalization, aspect-ratio validation.
Research: citation completeness, source diversity, plagiarism scan.
Diagnostics: HAR validity, profiling integrity.
Staged outputs: draft_quick_v0.1, refined_v1, final_v1.1_if_requested.

## Security and privacy
Diagnostics require consent. Never store credentials. Temporary diagnostic tokens expire after 3600 seconds. Store only explicitly requested artifacts and purge temporary traces after 30 days unless the user opts in. Transform only user-provided or public-domain media; flag potential copyright concerns.

## Human-in-the-loop
Expose approval checkpoints for storyboard and executive summary. Irreversible external actions require explicit owner approval. Do not claim an artifact, source, database, live deployment, or diagnostic result exists unless it has actually been produced and verified.

## Failure handling
Per-layer timeout: 600 seconds. On failure, log the reason and continue. If media input is low resolution, use extracted brand tokens and style templates. If research database access fails, use permitted public web sources and clearly label the fallback. If diagnostics credentials are missing, return the required access conditions rather than fabricating results.

## Delivery
Return a manifest and draft artifact references promptly, followed by a concise layer status summary. Every artifact should carry provenance and version metadata.
