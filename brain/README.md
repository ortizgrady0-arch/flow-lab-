---
title: "README: how to use this vault"
tags: [index, readme]
updated: 2026-09-11
---

# README: how to use this vault

## TL;DR

- This folder (`brain/`) is an Obsidian vault and the project memory for **flow-lab**: a research project that asked which three AI-leveraged side hustles a solo US operator (under $500, 10-15 h/week, no audience) should run, with demand and automation evidence for each.
- Start at [[00-Index]]. Its "Context refresh" section summarizes the whole project in under 15 bullets; read it before opening anything else.
- Layout: `reports/<hustle>/` (report, automation-stack, plan for each of the three finalists), `decisions/` (final selection, comparison matrix, three judge notes), `research/` (shortlist, candidate dossiers with two skeptic notes each, eight lens notes, saturated/overhyped hustles).
- Every note is TL;DR-first: YAML frontmatter, then `## TL;DR` (at most 8 bullets), then detail, then `## Sources` last. Read only the TL;DR unless the task needs more.
- Links are wikilinks (double square brackets) by vault-relative path without `.md`, for example `[[research/candidates/linkedin-founder-ghostwriting]]`; an alias goes after `|`, a heading after `#`.
- Open the `brain` folder as a vault in Obsidian (Open folder as vault) to get backlinks, graph view and link resolution; the notes also read fine as plain markdown.
- Token-saving rule for AI sessions: read `00-Index.md` first, then only the `## TL;DR` block of a note unless the task needs the detail; when finishing work, update the relevant note's TL;DR and the index rather than re-explaining in chat.

## What this vault is

`brain/` holds every artifact of the flow-lab research run, dated 2026-09-10 to 2026-09-11: eight lens surveys of the AI side-hustle landscape, a skeptic pass on saturated categories, a shortlist of ten candidates, a dossier plus two adversarial skeptic reviews per candidate, three judge rankings, a final portfolio decision, and a full report package (business report, automation stack, 90-day execution plan) for each of the three finalists. The vault is the single source of truth; chat transcripts are not.

## How it is organized

| Folder | Contents | Start with |
|---|---|---|
| `00-Index.md` | Map of content and context refresh | [[00-Index]] |
| `reports/<slug>/` | `report.md` (business case), `automation-stack.md` (workflow, tools, prompts), `plan.md` (week 1, 30/60/90 days, templates) for each finalist | [[reports/linkedin-founder-ghostwriting/report]], [[reports/youtube-manager-expert-firms/report]], [[reports/ai-front-desk-home-services/report]] |
| `decisions/` | [[decisions/final-selection]], [[decisions/comparison-matrix]], and the three judge notes | [[decisions/final-selection]] |
| `research/` | [[research/shortlist]], [[research/saturated-overhyped]], `candidates/` (dossier + `-skeptic-demand` + `-skeptic-execution` per slug), `lenses/` (eight market lenses) | [[research/shortlist]] |

Slugs are stable identifiers: the same slug names the dossier, its two skeptic notes and its report folder (for example `ai-front-desk-home-services`).

## Opening it in Obsidian

1. Install Obsidian, choose **Open folder as vault**, and select this `brain` folder (not the repository root).
2. Wikilinks are written as vault-relative paths, so leave the setting "New link format" on "Absolute path in vault" if you add notes, and keep the "Use Wikilinks" setting on.
3. Frontmatter `tags` power the tag pane: `index`, `report`, `automation-stack`, `plan`, `decision`, `judge`, `research`, `candidate`, `skeptic`, `lens`, plus one tag per hustle slug.
4. The graph view is most useful filtered to `tag:#candidate` or `tag:#decision`.

## Conventions

- **Frontmatter first:** `title`, `tags` (array), `updated` (ISO date); reports add `hustle` and `type`; skeptic notes add `lens`, `verdict` and `target`.
- **TL;DR first:** `## TL;DR` is the first section, at most 8 bullets, and must stand alone; a reader should be able to stop there.
- **Wikilinks by path:** `[[decisions/final-selection]]`, never bare note names; add `|alias` inside the brackets for display text and `#Heading` for sections.
- **Sources last:** every note ends with `## Sources` as markdown links (external) or wikilinks (internal), with dates where the source is dated.
- **Evidence labels:** dossiers and skeptic notes tag figures as verified / secondary / anecdotal (or [S] snippet, [A] anecdotal, [E] estimate). All external figures in this vault were relayed through search snippets or GitHub mirrors because primary pages were egress-blocked; "no data found" is written explicitly where a search came back empty.
- **Corrections flow forward:** skeptic notes correct dossiers, judge notes use the skeptic-corrected figures, `final-selection` uses the judge view, and the report packages (revised after review) are authoritative for the three finalists. When numbers disagree, the later stage wins.

## Token-saving rule

1. Read [[00-Index]] first; its context-refresh section is meant to replace re-reading the vault.
2. Open a note only when the task needs it, and read just its `## TL;DR` unless the detail is required.
3. When you finish work, update the affected note's TL;DR and `updated:` date, and touch the index, instead of re-explaining in chat.

## Sources

- [[00-Index]]
- [[decisions/final-selection]]
- [[research/shortlist]]
- `/CLAUDE.md` at the repository root (the context-refresh rule and vault conventions this README restates)
