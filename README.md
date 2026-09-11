# VCS4Writers

Git-backed version control, reimagined for writers — where **scenes, drafts, proposals, and canon** replace branches, pull requests, and `main`.

## What this is

A working test bed doing two jobs at once:

1. **Learning Git and Magit properly** — against a real repository instead of throwaway examples, following a deliberate slice of [Pro Git](https://git-scm.com/book/en/v2) rather than the whole book.
2. **Prototyping version control for writers** — hiding Git's mechanics behind language a novelist already thinks in.

The long-term goal is a small tool (working name `worldrepo`) that lets a non-technical writer manage a story the way engineers manage code — without ever touching a terminal.

## The test text

[*A Christmas Carol*](https://www.gutenberg.org/ebooks/46) by Charles Dickens (public domain), split one file per Stave:

```
scenes/
  01-marleys-ghost.md
  02-first-of-the-three-spirits.md
  03-second-of-the-three-spirits.md
  04-the-last-of-the-spirits.md
  05-the-end-of-it.md
```

Five self-contained staves give clean seams for practising branching, diffing, and merging — and the story's own past/present/future structure maps naturally onto "alternate timelines" as branches.

## Roadmap

- [ ] **Stage 1 — Learn.** Work the core Pro Git slice (Ch. 1–3, then 10.1–10.3) against this repo, entirely in Magit.
- [ ] **Stage 2 — Practise.** Hand-run add / commit / log / branch / merge / diff on the staves until they're reflex.
- [ ] **Stage 3 — Wrap.** Build thin Emacs/Magit commands expressing those operations in writers' terms.
- [ ] **Stage 4 — Extract.** Lift the logic into a standalone `worldrepo` tool any front-end can call.

## Licensing

This repository mixes two kinds of work, licensed separately:

- **Code and tooling** — MIT (see `LICENSE`).
- **Original prose and documentation** — CC BY 4.0 (see `LICENSE-content`).
- **The Dickens text** — public domain; no license required.
