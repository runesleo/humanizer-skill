# Humanizer Skill

**中文:** [README.md](./README.md)

---

A single-file Claude Code skill. It rewrites prose using Wikipedia’s “Signs of AI writing” pattern set, then pushes the result toward natural rhythm, opinions, and human voice—not just “clean” text.

## When to use

- You are **editing or reviewing** natural language so it reads more human and less templated (matches the `when_to_use` field in `SKILL.md` frontmatter).
- Drafts came from LLM-assisted writing and need a structured pass for the issues enumerated in `SKILL.md` (significance inflation, promo tone, shallow `-ing` add-ons, vague attributions, high-frequency “AI vocabulary,” dash abuse, and more).
- You need to strip chatbot-style artifacts (“hope this helps,” cutoff disclaimers, hollow upbeat endings) while **keeping the meaning**.
- You want the built-in loop in `SKILL.md` (identify → rewrite → short “what still screams AI?” pass before the final version).

## When NOT to use

- The task **does not** call for humanizing reader-facing prose (inverse of `when_to_use`; examples: only machine-readable config or structured data where tone work does not apply).
- There is no real body of text to edit, so the scan → rewrite → audit flow in `SKILL.md` has nothing to attach to.
- Your runner **cannot** honor the multi-step output contract in `SKILL.md` (draft, brief audit notes, final). Fix the environment; the skill is written assuming those steps exist.

## Quick Start

1. Copy `SKILL.md` into your Claude Code skills directory, e.g. `~/.claude/skills/humanizer/SKILL.md`.
2. If you publish through `npx skills add …`, point it at the path your registry uses, then invoke the skill per `SKILL.md`.
3. Check `allowed-tools` in the frontmatter before enabling the skill in a project.

## Typical scenarios

- Pre-publish pass on posts, newsletters, or product copy.
- Replacing vague “experts say” claims with attributed facts where the draft already has sources.
- Stripping collaborative-chat filler that leaked into an article.
- Pairing with an in-house style guide: keep terminology, reduce mechanical bolding and emoji headings.

## Repository layout (contributors)

| Path | Role |
|------|------|
| `SKILL.md` | Entire skill: metadata, 24 pattern groups, process, output shape—edit behavior here. |
| `LICENSE` | License text. |
