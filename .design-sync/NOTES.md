# loeuf · Claude Design sync notes

## Status
- **Bundle ready** at `ds-bundle/` — 9 `@dsCard` preview cards across 5 groups + `styles.css` + `README.md` (conventions header).
- **Not yet uploaded.** This environment cannot authorize DesignSync (`/design-login` needs an interactive terminal). The bundle is the *"provide the project files directly"* path.

## Groups / cards
- **Brand** — Wordmark, The œuf motif
- **Colors** — Palette
- **Type** — Typography
- **Foundations** — Spacing & radius
- **Components** — Buttons, Badges & tags, Product card
- **Social** — Instagram post (4:5), Instagram story (9:16)

## How to make `loeuf` appear in claude.ai/design (run from an authorized session)
From a Claude Code session signed into your claude.ai (Claude **subscription**) account, in this repo:

```
/design-sync
```
…or drive the tool directly:
1. `DesignSync(create_project, name:"loeuf")` → copy the returned `projectId` into `.design-sync/config.json`.
2. `DesignSync(finalize_plan, localDir:"./ds-bundle", writes:["components/**","styles.css","README.md"])` → returns `planId`.
3. `DesignSync(write_files, planId, files:[ … each ds-bundle file via localPath … ])`.

After upload + the app's manifest rebuild, `loeuf` shows up in the design-system picker next to *ash homes*, each card browsable by group.

## To add real code components later
These cards are static HTML previews (no compiled React). For the design agent to build with *real* loeuf components, convert an actual component repo (Storybook or npm package with a `dist/`) and re-run `/design-sync` — the converter will replace these previews with bound components.
