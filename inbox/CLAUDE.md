# Inbox Processing

The inbox is a drop zone for raw, unstructured notes. Files placed here can be any format — plain text, markdown, bullet points, stream of consciousness, links, quotes, anything.

## How to Add Notes

Drop a file into `inbox/` with any filename. No formatting required. Examples:

- `my-thought.md` — a quick idea
- `meeting-notes.txt` — raw notes from a meeting
- `interesting-links.md` — a list of URLs with brief descriptions
- `random-idea` — even no extension is fine

## Processing Workflow

Processing is typically done by **Soren** (research agent). The workflow:

1. **Scan** — Read all files in `inbox/` (ignore `_processed/`, `CLAUDE.md`, and `.gitkeep`)
2. **Parse** — For each file, extract the distinct concepts, facts, ideas, or questions
3. **Classify** — Determine what type each extracted item is:
   - **Concept** — a named idea, entity, or topic to track
   - **Fact** — a specific piece of information to attach to an existing concept
   - **Question** — something to investigate further
   - **Task** — something to do (route to Ada for project tracking)
   - **Connection** — an observation about how two things relate
4. **Deduplicate** — Check the existing knowledge base for matches before creating new entries
5. **File** — Create or update concept files in `knowledge/concepts/`, following the template
6. **Connect** — Add edges to `knowledge/graph.yaml` for any relationships identified
7. **Index** — Update `knowledge/_index.md` and relevant topic files
8. **Archive** — Move the original file to `inbox/_processed/` with a date prefix:
   `YYYY-MM-DD-original-filename.md`
9. **Log** — Add an entry to `logs/activity.md` summarizing what was processed

## Triggering Processing

Say any of:
- "Process the inbox"
- "Have Soren process the inbox"
- "Check the inbox"

## Tips for Good Inbox Notes

- One topic per note works best, but multi-topic notes are fine too
- Include context — why does this matter? Where did you hear it?
- Links are great — Soren will create reference entries for them
- Don't worry about formatting — the whole point is that Soren organizes it for you
