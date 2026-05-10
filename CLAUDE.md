# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is an **LLM Wiki** — a markdown knowledge base for AI engineering practice, not a traditional code repo. It captures experience in vibe coding, harness engineering, skills, MCP, prompt engineering, and AI engineering landing using the three-layer pattern from Andrej Karpathy's LLM Wiki approach.

## Directory Structure

| Directory | Role | Mutability |
|-----------|------|------------|
| `raw/` | Original source materials (articles, chat exports, screenshots, docs) | Read-only — never rewrite originals |
| `inbox/` | Unprocessed ideas, notes, and conversation excerpts | Temporary — process into `raw/` or `wiki/` |
| `wiki/` | LLM-maintained synthesized knowledge in structured markdown | Maintained by LLM |
| `wiki/concepts/` | Core concept pages | Maintained |
| `wiki/collections/` | Reusable asset indexes (prompts, skills, MCPs, patterns) | Maintained |
| `wiki/templates/` | Templates for source summaries and query notes | Stable |
| `skills/` | Repo-local Claude Code skills | Maintained |
| `AGENTS.md` | Full schema, maintenance protocol, writing rules, and safety rules | Authoritative |

## Key Files

- **`AGENTS.md`** — The authoritative schema and maintenance protocol. Read this for the full ingest/query/lint workflows, writing rules, and safety boundaries.
- **`wiki/index.md`** — Content index. Must be updated whenever wiki pages are added, renamed, or removed.
- **`wiki/log.md`** — Maintenance log. Append an entry for every ingest, query, lint, or refactor operation.

## Maintenance Protocol (from AGENTS.md)

### Ingest (when user provides new material into `raw/` or `inbox/`)
1. Read the material, identify topic, source, date, reliability
2. Generate or update relevant wiki pages — retain references to original sources
3. Update `wiki/index.md`
4. Append to `wiki/log.md`
5. If material contradicts existing pages, flag the conflict; do not silently overwrite

### Query (when answering questions from wiki knowledge)
1. Check `wiki/index.md` first, then read relevant pages
2. Fall back to `raw/` for original sources when needed
3. Distinguish facts, inferences, suggestions, and unverified items in output

### Lint (periodic health checks)
Check for: orphan pages, duplicate/conflicting concepts, strong claims without sources, stale tool/API/MCP info, important concepts missing dedicated pages, index-to-file mismatches.

## Writing Conventions

- Default language: Chinese; retain English technical terms where appropriate
- Every long-term page should include: one-sentence definition, applicable scenarios, inapplicable scenarios, operational methods, common pitfalls, related pages, references
- Do not dump conversational conclusions directly into wiki; rewrite as stable knowledge
- Do not assert certainty without a source; if it's a current judgment, label it as "待验证" (to be verified)

## Repo-Local Skills

Located in `skills/`. Currently: `clarify-to-build` — combines Socratic questioning, first principles, and Occam's razor to clarify vague requirements into implementation-ready breakdowns.

## Safety Rules (hard constraints)

- **Never batch-delete** files or directories. Delete only one explicitly specified file at a time.
- **Never commit** keys, tokens, credentials, secrets, or private materials.
- **Check for sensitive content** before every commit.
- **Do not trigger compilation** for UnrealEngine/UE projects or plugins.
