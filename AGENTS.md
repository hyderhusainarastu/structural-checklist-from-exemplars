# structural-checklist-from-exemplars

An instruction-only Agent Skill that derives a structural checklist for a document genre from strong exemplars and audits a draft against it.

## Using this in your project

- Use it when someone wants to write or revise a document in a genre and can supply (or gather) several strong examples of that genre.
- Invoke it by reading `SKILL.md` and following its steps. Native skill loaders pick it up after `./install.sh`; chat UIs can use `PROMPT.md` instead.
- Read every exemplar in full before comparing. Anchor each claim to a located passage, never to memory of "how these usually go".
- Output: a comparison table per dimension, governing-pattern findings, a numbered pass/fail checklist, and (if a draft exists) a ranked list of deviations. Write it where the user asks, otherwise return it in the reply.
- Never invent exemplars, quotations or proportions. If an exemplar is missing or unreadable, say so.
- Keep the user's draft and exemplars unmodified; this skill only reads them.

## Working on this repo

- No code and no build. Test the installer: `bash test_install.sh` (offline).
- Keep `SKILL.md` frontmatter: `name` lowercase-hyphen, `description` at most 300 characters.
- Keep `PROMPT.md` self-contained and under 6000 characters.
- Do not add synthetic data that resembles real people or unpublished text to `examples/`.
