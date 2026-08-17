# Worked Example (Synthetic): Structural Checklist for Incident Postmortems

> **This entire example is synthetic.** The "exemplars" below are invented for illustration only —
> no real company, incident, or document. It shows the method from `SKILL.md` applied at small scale
> (5 exemplars, 2 dimensions) so the shape of the output is clear. A real run would typically use
> more exemplars and more dimensions.

## Target document

A postmortem report for an internal service outage, to be shared with engineering leadership and
posted to an internal knowledge base. Genre: incident postmortem / retrospective report.

## Step 2 — Exemplars selected (synthetic, N=5)

| Slug | Context | Sub-genre | Why chosen |
|---|---|---|---|
| `synth-a-database-outage` | mid-size SaaS co., internal KB post | short, informal | Nearest genre match: same audience (internal eng), similar incident class (data-tier failure) |
| `synth-b-payments-incident` | fintech co., public status-page postmortem | public-facing, high formality | Register diversity: public accountability document, different stakes than internal-only |
| `synth-c-deploy-rollback` | infra team, internal wiki | very short, checklist-style | Space-constraint diversity: shortest exemplar, tests which moves survive compression |
| `synth-d-multi-region-failure` | large cloud provider, public engineering blog | long, narrative | Added deliberately: only exemplar with a genuinely multi-day, multi-cause incident, needed to see how a report handles a *sequence* of contributing failures rather than one root cause |
| `synth-e-security-incident` | internal security team, restricted-access report | internal, high formality | Added deliberately: only exemplar where "what we are not disclosing and why" is itself a structural section — a dimension the other four don't exhibit at all |

## Step 4–5 — One dimension worked through: "Root cause statement"

### Comparison table

| Exemplar | Where | How |
|---|---|---|
| `synth-a-database-outage` | Paragraph 2 of 6 | States root cause in one sentence before any timeline detail: "the outage was caused by an unindexed migration query holding a table lock." |
| `synth-b-payments-incident` | Own labeled section, 3rd of 7 | Root cause stated only after a full timeline section; framed as "Contributing Factors" (plural), not a single cause |
| `synth-c-deploy-rollback` | First line of the document | Root cause is the document's opening line, no context paragraph precedes it at all |
| `synth-d-multi-region-failure` | Not stated as one sentence anywhere; distributed across 3 subsections ("Regional Failover Trigger," "Configuration Drift," "Alert Suppression") | — (see note: this exemplar treats "root cause" as a category error for a multi-cause incident and structurally refuses to name a single one) |
| `synth-e-security-incident` | Own labeled section, 2nd of 6, immediately after a scope/redaction notice | States cause in one sentence, but the sentence is preceded by a boilerplate redaction notice in every instance |

### Governing-pattern finding (example)

1. **A single-sentence root-cause statement, placed early, is the default — but it is a convention
   of single-cause incidents, not a universal rule.** Three of five exemplars (`synth-a`, `synth-c`,
   `synth-e`) state the cause in one sentence within the first one to three moves of the document.
   The one exemplar that deviates by structure rather than placement (`synth-d`) does so because the
   incident itself had multiple independent contributing failures — it replaces the single-sentence
   convention with a small named set of contributing-factor subsections, and does so consistently
   with `synth-b`'s "Contributing Factors" framing. **Conditional convention**: use a single
   root-cause sentence when the incident has one; use a small enumerated set of named contributing
   factors, not a diluted single sentence, when it does not — collapsing a genuinely multi-cause
   incident into one sentence for the sake of the convention would misrepresent the incident, exactly
   as a forced single cause would.
2. Placement varies with formality/audience, not with incident type: the most internal, least formal
   exemplar (`synth-c`) puts the cause first with zero preamble; the most external/formal exemplars
   (`synth-b`, `synth-e`) place it after a framing section. Both are legitimate; the target document
   (internal, moderate formality) sits closer to `synth-a`'s placement.

## Step 9 — Resulting checklist (excerpt, illustrative)

1. If the incident has a single identifiable proximate cause, state it in one sentence within the
   first three structural moves of the document. If it has multiple independent contributing
   causes, do not compress them into one sentence — name each as its own item in an enumerated
   "Contributing Factors" list instead.
2. A timeline, if included, does not substitute for the root-cause statement — the two are separate
   moves and the cause statement should not be inferable only by reading the timeline end to end.
3. Where the document is shared outside the immediate team, a scope/redaction notice (what is
   withheld and why) precedes any cause statement, stated once, not repeated per section.
4. [... further items would continue for the remaining dimensions analyzed, e.g. "Impact statement,"
   "Remediation items," "Timeline granularity," "Blame-language avoidance" ...]

## Note on scale

A real application of this method to a genre like incident postmortems would typically read 8–12
exemplars and work through 5–8 dimensions (root cause, impact/blast-radius statement, timeline,
remediation items and their trackability, blame-language conventions, disclosure/redaction handling,
proportions between narrative and action-items). This excerpt shows one dimension fully worked to
make the mechanics visible, not a complete deliverable.
