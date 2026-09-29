# Engineering-Design-Notebook

## How to add an entry

1. **New note** (⌘N) — it lands in `Entries/`.
2. Rename it `YYYY-MM-DD Short title`.
3. **Insert template**: press **⌘P** (Ctrl+P on Windows) to open the command palette, type `insert template`, and pick **Entry**. Or click the *Insert template* icon in the left ribbon. It adds the properties; the rest of the note is up to you.
4. Fill in `authors` and `sprint` — the table in [Notebook](Notebook.md) shows them.
5. If the entry's work lives in a GitHub commit, paste its URL into `commits` (e.g. `https://github.com/MIE243/Engineering-Specifications/commit/2b59cb6`). The URL names both the repo and the commit; add one per line if there are several.

One entry per file, one author per entry where possible — separate files keep merge conflicts rare.

## Exporting to one document

The **Export** section of `Notebook.md` embeds every note in `Entries/` automatically, oldest first (by file name), using the Dataview plugin. Nothing to add by hand — new entries appear on their own.

To hand the notebook in as a single PDF: open `Notebook.md` in reading view, check the entries are all there, then command palette → *Export to PDF*.

**First time on a machine:** Dataview is a community plugin and is committed with the vault, but Obsidian won't run it until you allow it: Settings → Community plugins → *Turn on community plugins*, then make sure **Dataview** is toggled on.
