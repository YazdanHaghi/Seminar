# Yazdan LLM Wiki

This is a starter LLM Wiki for organizing your engineering projects, notes, code experiments, logs, PDFs, and application documents.

## Folder structure

```text
yazdan_llm_wiki/
├── inbox/       # Put new files here first
├── raw/         # Original processed files
├── sources/     # One source summary per processed file
├── wiki/        # Clean human-readable knowledge pages
├── prompts/     # Prompts you can copy into ChatGPT or another LLM
├── logs/        # Optional processing/update logs
└── assets/      # Images, diagrams, screenshots
```

## Basic workflow

1. Put new files, notes, code, logs, PDFs, or screenshots into `inbox/`.
2. Open ChatGPT or another LLM with file/folder access.
3. Copy the prompt from `prompts/01_ingest_inbox.md`.
4. The LLM should create source summaries in `sources/` and update pages in `wiki/`.
5. Move processed files from `inbox/` to `raw/`.
6. Use `prompts/02_ask_wiki.md` whenever you want to ask questions about your knowledge base.

## Main rule

Do not let the wiki become a dump of raw text. The `wiki/` folder should contain organized, readable, linked pages. The `sources/` folder should keep traceability back to original files.
