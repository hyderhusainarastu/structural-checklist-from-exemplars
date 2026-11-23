# structural-checklist-from-exemplars

An Agent Skill that derives a structural checklist for any document genre by comparatively
analyzing a set of strong exemplar documents — instead of relying on convention, memory, or a
generic template, it builds the standard from what real documents in that genre actually do.

## What it does

Give it a target document (a draft, or a plan for one) and a handful of strong exemplars in the same
or an adjacent genre — papers, grant proposals, incident postmortems, product one-pagers, long-form
posts, whatever the target is. It walks through a repeatable method:

1. **Selects and logs why** each exemplar was chosen (nearest genre match, nearest topical
   neighbor, register/venue diversity, or added specifically to fill a data point the others miss).
2. **Reads every exemplar in full** at the structure level — noting where each structural move
   happens and how, anchored to a specific passage, never to memory of "how these usually go."
3. **Builds a comparison table** per structural dimension (opening architecture, evidence
   engagement, gap justification, differentiation from nearest neighbors, proportions, closing
   architecture, or whatever dimensions matter for the genre).
4. **Reconciles the table into governing-pattern findings** — distinguishing conventions that hold
   universally from ones that track sub-genre or venue, and naming which is which.
5. **Produces a short, numbered, mechanically verifiable checklist** — each item checkable by
   inspection alone, no re-derivation required — plus, optionally, a paragraph-by-paragraph template
   for drafting the target document itself.
6. **Applies the checklist to the target draft**, if one exists, producing a ranked list of the
   biggest structural deviations and why each one matters.

The output is evidence-based and falsifiable: every claim in the governing-pattern report traces
back to a specific passage in a specific exemplar, and every checklist item can be marked pass/fail
by a reviewer holding only the target document.

## Works with

| Surface | How | Status |
|---|---|---|
| Claude Code | native skill (`./install.sh --claude`) | not tested |
| Codex | native skill via `.agents/skills` (`./install.sh --agents`) | not tested |
| Gemini CLI | native skill via `.agents/skills`, or pointer (`--gemini`) | not tested |
| Cursor | native skill via `.agents/skills`, or `AGENTS.md` (`--cursor`) | not tested |
| Copilot | pointer to the skill (`--copilot`) | not tested |
| ChatGPT / Claude.ai / Gemini (chat) | prompt (`PROMPT.md`) | not tested |

The installer itself is tested offline (`bash test_install.sh`). The skill is instructions only; the SKILL.md follows the open [Agent Skills specification](https://agentskills.io/specification).

## Quick start

```sh
git clone https://github.com/hyderhusainarastu/structural-checklist-from-exemplars
cd structural-checklist-from-exemplars
./install.sh --claude              # ~/.claude/skills/structural-checklist-from-exemplars
./install.sh --agents --project .  # .agents/skills (Codex, Cursor, Gemini CLI)
./install.sh --help                # all targets; --dry-run and --uninstall supported
```

Chat UIs: paste `PROMPT.md`, or the short version below.

### Copy-paste prompt

```
I want a structural checklist for this document genre: <genre>.
Below are <N> strong exemplars. Read each in full; do not use memory of the genre.
1. Compare them on structure (opening, evidence, gap, differentiation, proportions, closing), quoting passages.
2. Separate universal conventions from sub-genre or venue ones.
3. Output a numbered checklist where every item is pass/fail by inspection, then audit my draft against it and rank the biggest deviations.
```

## Usage example (synthetic)

`examples/synthetic-postmortem-example.md` walks through a small, fully synthetic run of the method
end to end: five invented incident-postmortem "exemplars," one structural dimension worked through
in full (how each states its root cause), and an excerpt of the resulting checklist. It shows the
shape of the output — the exemplar-selection table, the per-dimension comparison table, a
governing-pattern finding distinguishing a universal convention from a genre-conditional one, and the
checklist items that finding produces.

A typical real run is larger: 6–12 real exemplars and 5–8 structural dimensions, applied to an actual
target draft, ending in a ranked deviations list against that draft.

## No bundled script

This skill is instructions-only — there is no CLI tool to run. The method is meant to be executed by
an agent (or a person) working directly with the exemplar texts and the target document; the value is
in the close reading and reconciliation, which doesn't reduce to a script.

## License

MIT — see [LICENSE](./LICENSE).

## How it differs

Generic writing templates and genre guides give a fixed outline. This skill builds the checklist from the exemplars you supply and ties every item to a located passage, so it can be checked and challenged.

## Limits

- Instructions only; quality depends on the exemplars you give and on the model reading them in full.
- Fewer than three exemplars gives weak, non-generalizable findings.
- Proportion measures need the full text of each exemplar.

## Related

- [pre-submission-manuscript-audit](https://github.com/hyderhusainarastu/pre-submission-manuscript-audit)
- [manuscript-mechanical-qa-sweep-pipeline](https://github.com/hyderhusainarastu/manuscript-mechanical-qa-sweep-pipeline)
- [hallucinated-citation-checker](https://github.com/hyderhusainarastu/hallucinated-citation-checker)

## Keywords

structural checklist, genre analysis, exemplar comparison, document structure, technical writing, postmortem, editing, agent skill, SKILL.md

---
Part of palimnote-skills - more at https://github.com/hyderhusainarastu
