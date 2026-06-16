# Prompt: Ingest Inbox

You are maintaining my LLM Wiki.

Read all new files in `inbox/` and follow `WIKI_RULES.md`.

For every file:

1. Create a source summary in `sources/`.
2. Extract important facts, commands, errors, decisions, measurements, and TODOs.
3. Update existing pages in `wiki/` or create new pages when needed.
4. Add source references to the updated wiki pages.
5. Detect contradictions with existing wiki content and mark them clearly.
6. At the end, give me a short changelog:
   - files processed
   - pages created
   - pages updated
   - unresolved questions

Do not invent facts. If something is unclear, write it under `Open Questions`.
