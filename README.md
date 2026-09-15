
# VCS4Writers

Git-backed version control, reimagined for writers — where **scenes, drafts, proposals, and canon** replace branches, pull requests, and `main`.

## Why this exists

Most writers keep their life's work the same way: a folder of files named `novel_draft_final_v7.docx`, backed up — if at all — to whatever cloud their writing app happens to rent them. It holds until it doesn't. This project started the afternoon I watched a colleague nearly lose an entire novel to a misplaced USB stick. That night I looked at my own folder of dated `.doc` files and realised that "not losing everything" was not the same as leaving behind a studio someone could actually use.

Plain text and Git are the repair. Plain text is the most durable, portable format we have — readable in fifty years, convertible to PDF, EPUB, or print, and *owned* by you rather than licensed to you through someone else's interface. Git adds a memory: a complete, navigable history of how the work changed, kept in as many copies as you like, on machines you control.

Used this way, version control stops being developer machinery and becomes something a writer recognises — a time machine, and a conversation between the writer you were and the writer you're becoming. Every commit is a short note to your future self: what you changed, and why. Over months those notes accumulate into a documentary of how the work was made — the subplot you abandoned, the ending you rewrote three times, the day a swollen single file finally became a structure that made sense.

When you choose to open it, you publish not just a finished text but its making — a thing that can be read, forked, and extended rather than only consumed. That is the wager here: give writers the power engineers have had for decades, without ever making them touch a terminal.

I've expressed my thoughts on plain text, git and text editors, and why writers ought to embrace them in columns, ([here](https://itsfoss.com/opinion/git-plain-text-writing/), [here](https://itsfoss.com/news/version-control-writers/), and [and here](https://itsfoss.com/opinion/emacs-the-ux-ideal/) if you are interested. 

## Three ways writers already version their work

You already use version control — almost certainly one of the first two kinds below. Git is the third, and it's the one worth learning.

| Approach | What you probably use | What it gives you | Where it fails |
| --- | --- | --- | --- |
| **Local** | `v1`, `v2`, `Final_FINAL.docx` in a folder | Simple, offline, entirely yours | No record of *why* anything changed; easy to overwrite the wrong file; no way to hold two directions at once |
| **Centralized** | Google Docs | Real-time collaboration, one shared copy, some history | You *rent* the single copy; history isn't portable; no real branching; access depends on an account and a company |
| **Distributed (Git)** | — | Full history on every machine; work offline; branch fearlessly; merge into canon on purpose | Steeper mental model; reconciling copies is deliberate, not automatic |

The distributed idea is the unfamiliar one, so picture a writers' room where every writer keeps, on their own desk, not a link to the showrunner's script but the **entire filing cabinet** — every draft, every abandoned alternate, all the way back to the pilot. If one office burns down, any writer's cabinet restores the whole show. Because each copy is complete and independent, you can take an episode somewhere wild on your own branch without touching anyone else's work — and if it's good, you *propose* folding it into canon; if not, you bin the branch and canon never knew. That is what this project gives a writer: the freedom to experiment without fear, and a history no single company owns.

## What this is

A working test bed doing two jobs at once:

1. **Learning Git and Magit properly** — against a real repository instead of throwaway examples, following a deliberate slice of [Pro Git](https://git-scm.com/book/en/v2) rather than the whole book.
2. **Prototyping version control for writers** — hiding Git's mechanics behind language a novelist already thinks in: scenes, drafts, proposals, canon.

The long-term goal is a small tool (working name `worldrepo`) that lets a non-technical writer manage a story the way engineers manage code — without ever touching a terminal.

## The test text

[*A Christmas Carol*](https://www.gutenberg.org/ebooks/46) by Charles Dickens (public domain), split one file per Stave:

```
Stories/AChristmasCarol/
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


### Further Reading

Two arguments that shaped this project:

- [Why I Switched to Plain Text and Git for My Writing](https://itsfoss.com/opinion/git-plain-text-writing/) — my own case for plain text and version control as a writer's infrastructure: memory, ownership, and the long afterlife of a text.
- [The Plain Person's Guide to Plain Text Social Science](https://plain-text.co/) — Kieran Healy's pragmatic guide to a plain-text, version-controlled workflow. Written for social scientists, but its reasoning on version control, backups, and durable formats carries straight over to fiction.



## Licensing

This repository mixes two kinds of work, licensed separately:

- **Code and tooling** — MIT (see `LICENSE`).
- **Original prose and documentation** — CC BY 4.0 (see `LICENSE-content`).
- **The Dickens text** — public domain; no license required.
