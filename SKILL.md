---
name: structural-checklist-from-exemplars
description: Derives a reusable, mechanically verifiable structural checklist for any document genre (papers, reports, proposals, technical postmortems, long-form posts, grant applications, etc.) by comparatively analyzing a set of strong exemplar documents at the structure level, then applying that checklist to a target draft. Invoke when someone needs to write or revise a document in a genre they want to get structurally right, has (or can gather) several strong examples of that genre, and wants a standard derived from close reading of those examples rather than from convention, memory, or a generic template.
---

# Structural Checklist from Exemplars

## What this skill does

Given a target document (a draft, or a document about to be written) and a genre it belongs to, this
skill produces two artifacts:

1. **A governing-pattern report** — a structural analysis of how a set of exemplar documents in the
   same or a closely adjacent genre actually organize themselves, dimension by dimension, with every
   claim traceable to a specific passage in a specific exemplar.
2. **A structural checklist** — a short, numbered list of mechanically verifiable items, derived from
   that report, that a reviewer can check a document against without re-deriving the analysis.

Optionally, it also produces a **paragraph-by-paragraph or section-by-section template** that
operationalizes the checklist for the specific target document.

The method is genre-agnostic. It has been used for a scholarly paper's introduction and literature
sections; it applies equally to a technical postmortem, a grant proposal, a product one-pager, a
long-form blog post, an API design doc, or a legal brief — anything with enough real exemplars to
compare.

## When to invoke this skill

- The user is about to write, or has drafted, a document in a genre where structural convention
  matters (peer review, an editor, a funding board, or a reader's trust depends on the document
  "looking right" for its kind).
- The user has access to several — ideally 6 or more — documents that are recognized as strong or
  representative examples of that genre, or can identify where to find them.
- The user wants the standard to come from **evidence** (what real documents in this genre actually
  do) rather than from a generic template, a style guide's abstract advice, or the writer's own
  habit.
- A red flag has already been raised about a draft's structure ("this doesn't feel like a real X"),
  and the user wants a rigorous, defensible account of exactly what is off and why.

Do not invoke this skill to produce prose, to copy-edit sentences, or to check facts/citations —
it produces and applies a *structural* standard only. It also does not substitute for having actual
exemplars: if fewer than roughly 4–5 real exemplars are available, name that limitation explicitly
in the output rather than proceeding as if the sample were adequate.

## Governing principle

**Every structural claim in the output must be traceable to a passage actually read in this task —
never to memory, convention, or "papers like this usually do X."** If a claim cannot be pointed at a
specific location in a specific exemplar, it does not go in the report. This discipline is what
makes the resulting checklist defensible to a skeptical reviewer, and it is the single most
important rule in this skill.

---

## Step 1 — Define the target and the dimensions of interest

Before touching any exemplar, write down:

- **The target document**: what it is, its genre/venue, and (if it exists) its current draft.
- **The stakes**: who evaluates this document and what "structurally right" would buy the writer
  (a reviewer's trust, a funder's confidence, a reader finishing the piece).
- **A first-pass list of structural dimensions worth comparing.** These are the axes along which
  documents in this genre can differ in organization — not content. Examples of dimensions from
  different genres:
  - *Opening architecture*: how the document establishes context, states its purpose, and previews
    what follows, paragraph by paragraph.
  - *Evidence/precedent engagement*: whether prior work or precedent is woven into argument or
    segregated into its own section, and how disagreement between sources is staged.
  - *Problem/gap justification*: how a document argues that a gap, need, or problem is real, as
    opposed to merely asserting it.
  - *Differentiation*: whether and how the document positions itself against its nearest
    comparable neighbors (competing products, competing methods, competing prior claims) rather
    than only against abstract background.
  - *Proportions*: how much of the total length each section or move actually occupies.
  - *Closing architecture*: how the document ends — summary, call to action, limitations, next
    steps — and how much space that gets.

  This list is a starting hypothesis. It will be revised once exemplars are actually read — some
  dimensions will turn out not to vary interestingly, and reading will surface dimensions not
  anticipated here (this is normal and expected; note new dimensions as they appear).

## Step 2 — Select N exemplars

**Target N**: enough exemplars to distinguish a genuine convention from one writer's habit, and
enough to see genre-internal variation, not just genre-external contrast. Ten is a reasonable
default for a paper-scale document; fewer (5–6) is workable for a shorter genre; more is better
whenever exemplars are cheap to obtain.

Selection should be deliberate and logged, not just "whatever was on hand." For each exemplar,
record in a table: **slug/identifier, venue or context, sub-genre, and the specific reason it was
chosen.** Reasons should cover at least these categories across the set:

- **Nearest genre match** — one or more exemplars that are the closest available analog to the
  target document's own genre and stakes (an argued-position piece if the target argues a position;
  a system/build paper if the target describes something built).
- **Nearest technical/topical neighbor** — an exemplar chosen not for genre closeness but because it
  covers the closest comparable subject matter, so its differentiation and scoping moves are
  directly instructive.
- **Register/venue diversity** — exemplars spanning different venues, formality levels, or space
  constraints (a short compressed piece, a long unconstrained one, a practitioner venue, an academic
  one), so that conventions can be tested against genre and space rather than assumed universal.
- **Deliberately added for a missing data point** — after an initial pass through the "obvious"
  exemplars, look for what dimension of interest (Step 1) has no example yet — a particular
  structural feature, a particular proportion pattern, a particular closing convention — and add an
  exemplar specifically because it supplies that missing data point. Name this reason explicitly
  when it applies; it is a legitimate and often the most valuable selection criterion.

Do not select exemplars solely because they are famous, solely because they are convenient, or
solely because they already agree with a structure the writer wants to justify. A set that is
secretly cherry-picked to confirm what the writer already believes produces a checklist that is
decoration, not a standard.

## Step 3 — Read each exemplar fully, at the structure level

For each exemplar, read the complete text (not an abstract, not a summary, not a memory of having
read something similar before). While reading, note for each structural dimension from Step 1:

- **Where** the relevant move happens (paragraph number, section number, or page/locator if the
  source exposes one).
- **How** it happens — the actual mechanism, described concretely enough that another reader could
  find the same passage.
- A **short supporting quotation** (a phrase or clause, not a full paragraph) that anchors the
  observation to the text, with its locator.

Do this reading pass exhaustively before drawing any conclusions across exemplars — cross-exemplar
comparison in Step 5 depends on having genuinely observed every exemplar, not on generalizing from
the first two or three read.

If an exemplar's source format makes some data unrecoverable (e.g., a scanned document without
page boundaries, or a proportion that can't be computed because section lengths aren't stated),
say so explicitly rather than guessing or omitting the exemplar silently.

## Step 4 — Build the per-dimension comparison table

For each dimension from Step 1, build one table with exemplars as rows and the dimension's
sub-features as columns. This is the evidentiary backbone of the whole report — it is what lets a
skeptical reader verify the findings in Step 5 rather than take them on faith.

Populate every cell with what was actually found in Step 3: a paragraph/section locator, a short
description of the mechanism, and (where useful) an inline short quotation. Where a dimension does
not apply to a given exemplar (no such move exists in that document), record that explicitly as an
absence — absences are data, not gaps in the table.

## Step 5 — Derive governing-pattern findings

Read across each table's rows and write a small numbered list of **findings** — the actual
reconciliation of N observations into a stated pattern. Each finding should:

1. **State the pattern in one or two sentences**, specific enough to be actionable (e.g., in the
   incident-postmortem genre: "the root cause is named in a single sentence within the first three
   structural moves of the document" — not "postmortems explain what happened early").
2. **Name which exemplars support it and which deviate**, and for deviations, explain *why* —
   usually genre, venue space constraint, or sub-genre convention, not quality. A pattern that
   holds across every exemplar regardless of sub-genre is a **universal invariant** for this genre
   family; a pattern that tracks sub-genre or venue is a **conditional convention** and must be
   labeled as such. Conflating the two is the most common way this method goes wrong — never assert
   a convention as universal because most of the exemplars happen to follow it if the deviations
   cluster by genre rather than being scattered noise.
3. **State what does NOT vary** as well as what does — a dimension where every exemplar behaves
   identically regardless of sub-genre is often the strongest and most defensible checklist item,
   because it is not contingent on matching the target document's exact sub-genre.
4. Where relevant, extract the underlying **mechanism**, not just the surface convention — e.g. not
   "remediation items are listed" but "every remediation item names both a specific owner and a
   verification method, never left as a bare intention with no way to confirm it happened." A
   mechanism-level finding generalizes to checklist items that are hard to satisfy by surface mimicry
   alone.

A useful sub-pattern worth checking explicitly in most genres: **how does a document position itself
against its nearest neighbors** — not just against a general background or literature, but against
the specific comparable things a reader would otherwise reach for (competing products, competing
methods, competing prior claims, the "next most obvious" alternative)? Documents that skip this move
often read as unearned or naive to an expert reader even when everything else is well-argued; check
for its presence across the exemplar set as its own finding.

## Step 6 — Extract structural quotations

Collect a small set (roughly 3–6) of short, precisely located quotations (a phrase or a single
sentence, not a paragraph) that each crisply exemplify one governing-pattern finding. These serve as
calibration examples in the final checklist and template — they let a future reader see the pattern
in the exemplars' own words rather than only in paraphrase. Keep them short enough that they
illustrate a *structural move* (a sentence-opening formula, a transition, a naming convention), not
long enough to constitute a content excerpt from the exemplar.

## Step 7 — Measure proportions, where recoverable

Where exemplar section or page lengths can be determined, build a proportions table: what share of
total length each major section or move occupies, per exemplar. This is often the most concretely
actionable output of the whole method, because writers reliably over- or under-allocate space to
sections (front matter, caveats/limitations, differentiation, close) relative to genre norms without
noticing it.

Note explicitly which exemplars' proportions could not be recovered and why (rather than silently
dropping them from this step), and flag which recovered exemplar is the **closest genre/sub-genre
analog** to the target document — its proportions carry more weight than a distant one's.

## Step 8 — Compare the target document against the derived patterns

With the governing-pattern findings and (if available) proportions table in hand, walk the target
document (or the plan for a not-yet-written one) against each finding and produce a **deviations
list**: places where the target's current or planned structure departs from a finding established in
Step 5. For each deviation, state:

- What the finding says.
- What the target actually does.
- Why the deviation matters (what it costs the reader, or what convention it violates) — grounded in
  the exemplar evidence, not in taste.
- Whether the deviation is defensible given something genuinely distinctive about the target's own
  genre position (name the justification explicitly) or is simply an oversight to fix.

Rank deviations roughly by how much structural work they cost the target document, and be willing to
name the single or top-few biggest ones plainly — a report that treats every finding as equally
urgent is less useful than one that says clearly "these three matter most."

## Step 9 — Synthesize the checklist

Convert the governing-pattern findings into a short, numbered checklist. This is the primary
deliverable and it has a specific bar to clear: **every item must be answerable by inspection of the
target document alone, without needing to re-read the exemplar analysis.** Concretely, that means:

- Each item states a concrete, checkable condition ("X appears no later than paragraph N," "every
  remediation item names an owner and a verification method, never left as a bare intention," "no
  single alternative or competitor is discussed for more than one paragraph before the document
  states its own position"), never a vague aspiration ("the introduction should be engaging").
- Each item is falsifiable — a reviewer with the document in hand and no other context can mark it
  pass/fail (or pass-with-note) and point at the specific place in the document that decided it.
  Prefer wording that names *quantities or locations* (a paragraph number, a percentage of length, a
  count of named comparators) over wording that relies on subjective judgment.
- Items that encode a **conditional convention** (Step 5) should say so in the item itself, or state
  the condition under which it applies, rather than presenting a genre-contingent norm as absolute.
- Keep the list short enough to actually be used — roughly 8–12 items for a document-length genre.
  If more than that many distinct findings emerged, group related ones into a single compound item
  rather than listing every finding separately.
- Include at least one item on **proportions** (if Step 7 produced usable data) and at least one on
  **differentiation from nearest neighbors** (if that sub-pattern from Step 5 applies to this genre)
  — these are the two structural moves most often missing from checklists written from memory or
  convention rather than from actual exemplar reading.

## Step 10 (optional) — Build a section-by-section or paragraph-by-paragraph template

When the target document is being freshly drafted (not just checked), turn the checklist into a
template: one entry per paragraph or section of the target, each stating:

- **Its function** — what structural job this paragraph/section does, referencing the checklist item
  or governing-pattern finding it satisfies.
- **A drafting note on register**, drawn from how the exemplars actually handle tone at this point
  (hype-avoidant vs. rhetorically forceful, citation-dense vs. sparse, formal vs. conversational) —
  grounded in what was actually observed, not generic writing advice.
- **What content/evidence it may draw on**, if the target document has its own source material —
  keep this as a pointer to the target's own inputs, described generically (e.g., "the background
  material already gathered on X"), never by reproducing exemplar content here.
- **Any hard constraint that already binds this section** — stakeholder rulings, prior editorial
  decisions, non-negotiable claims or omissions the target document is already committed to. Where
  such constraints exist, name them as placeholders (e.g., `{{APPROVED_THESIS_WORDING}}`,
  `{{EDITORIAL_CONSTRAINT}}`) rather than inventing content, and instruct the drafter to fill them
  from the target project's own governance record.

Close the template with one paragraph stating **what it removes relative to the current draft** (if
one exists) — naming the specific material that no longer belongs where it currently sits, and where
(if anywhere) it relocates to under the exemplar-derived convention. This "what changes" statement is
often more useful to a writer than the template itself, because it converts an abstract standard into
a concrete edit.

## Step 11 — Write the summary for the caller

Close the whole deliverable with a short summary section containing:

- **A one-paragraph template summary** — the target document's structure restated as a compressed
  recipe, referencing the checklist.
- **The top 2–4 structural deviations** of the current draft (if one exists) from the exemplar norm,
  stated plainly, each with its evidentiary basis (which finding it violates, and by how much).

This summary is what a time-pressed reader (an editor, a co-author, a reviewer) will read first and
sometimes only — it should stand alone.

---

## Output format

Structure the final deliverable as a single document with these sections, in this order:

```
# Structural Checklist: <target genre>

**Status / provenance note:** derived from direct reading of N exemplars listed below, not from
memory or convention.

**Exemplars read (N):** <table — slug/identifier, venue, sub-genre, why chosen>

## 1. <Dimension 1 name>
### Per-exemplar table
### Governing-pattern findings (numbered)
### Structural quotations (short, located)

## 2. <Dimension 2 name>
...

## N. Proportions
<proportions table + findings>

## N+1. <Target Genre> Structural Checklist
<the numbered, mechanically verifiable checklist — the primary deliverable>

## N+2. (optional) <Target Document> Template
<paragraph/section-by-section plan>

## Summary for the caller
<template summary + top deviations>
```

## Common failure modes to avoid

- **Asserting a pattern from one exemplar as if it were general.** A single-exemplar precedent is
  worth naming (it may be the *only* available model for an unusual genre feature), but it must be
  labeled as single-exemplar, not folded into a "the pattern is" finding.
- **Treating absence of a convention as an error.** Some exemplars lack a section or move entirely
  (no roadmap sentence, no dedicated related-work section) because their genre or space doesn't call
  for it, not because they are deficient. Findings must say *why* a convention is genre-conditional
  before a checklist item can treat its absence in the target as a problem.
- **Letting quality bias exemplar reading.** A weaker exemplar's structural choices are still data
  about the genre; do not silently discount an exemplar's structural pattern because the writer
  judges its content weaker.
- **Writing a checklist item that can't be checked without re-reading the whole report.** If an item
  requires interpretation the reader wasn't given, it is not yet in checklist form — push the
  judgment call back into the governing-pattern finding and state a bright-line rule in the item
  itself.
- **Confusing this method with a generic style guide.** The value of this method is that every claim
  traces to a real, read passage. A checklist item that could have been written without reading any
  exemplar (e.g., "use clear language") does not belong in the output.
