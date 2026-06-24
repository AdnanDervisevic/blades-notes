# blades-notes

Shared campaign notes for our **Blades in the Dark** game, kept as an [Obsidian](https://obsidian.md) vault under version control.

The notes themselves live in **`The Creed Vault/`**. Open that folder as a vault in Obsidian (see below).

## What is Obsidian?

Obsidian is a free note-taking app that works on plain Markdown (`.md`) files stored in a local folder called a *vault*. Two features we rely on:

- **Wikilinks** — write `[[Doskvol]]` to link to another note. Click it to jump there; Obsidian shows backlinks and a graph of how everything connects.
- **Frontmatter** — the `---` block at the top of each note holds metadata (type, heritage, crew, etc.) Obsidian can filter and query on.

Because it's just Markdown in a folder, the whole vault drops cleanly into Git — no proprietary format, readable diffs, easy merges.

## How to open the vault

1. Install Obsidian: https://obsidian.md/download
2. *Open folder as vault* → select `The Creed Vault`.
3. Start at **`Home.md`**, which indexes every page.

## Vault structure

```
The Creed Vault/
├── Home.md            Index / table of contents
├── Characters/        The player characters (PCs)
├── NPCs/              Non-player characters and factions
├── Locations/         Districts, the city, the wider world
├── Crew/              The Creed (crew sheet + lore)
├── Reference/         Rules summaries (playbooks, crew types)
└── Sessions/          Session logs + open questions
```

## Conventions

- **Wikilink everything.** New character, place, or faction → make a note and link it.
- **Frontmatter on each note**, with a `type:` field (`pc`, `npc`, `location`, `faction`, `reference`, `session`).
- **No blank line between the frontmatter and the `# Title`.**
- **Page citations** refer to the *Blades in the Dark* core rulebook, v8.2.
- The rulebook PDF and zip exports are **not** committed (see `.gitignore`) — they're large and copyrighted.

## Working with Git + Obsidian

We use the **Obsidian Git** community plugin, so you can commit and sync without leaving Obsidian.

**One-time setup**
1. On desktop you must have regular [Git](https://git-scm.com/downloads) installed (GitHub Desktop alone is not enough).
2. In Obsidian: *Settings → Community plugins → Browse →* search **Git** → install and enable.
3. In the plugin settings, set your commit name/email under *Authentication / Commit Author*.

**Day-to-day**
- Run **"Commit-and-sync"** from the command palette (`Ctrl/Cmd+P`) — it stages, commits, pulls, then pushes in one step. You can set it to run automatically every few minutes in the plugin settings.
- Pull before a session, sync after, so everyone stays current.

**Guides**
- Obsidian Git — official docs: https://publish.obsidian.md/git-doc/Start+here
- Obsidian Git — plugin repo: https://github.com/Vinzent03/obsidian-git
- Obsidian help (vaults, linking, Markdown): https://help.obsidian.md

> Note: Obsidian Git is unstable on mobile — desktop is recommended for syncing.

If you'd rather use Git directly, the usual `git pull` → edit → `git add -A` → `git commit` → `git push` works too, since the vault is just files.
