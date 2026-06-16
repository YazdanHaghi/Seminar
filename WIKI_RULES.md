# LLM Wiki Rules

You are maintaining Yazdan's technical LLM Wiki.

## Goals

- Turn raw project material into a clean Markdown knowledge base.
- Keep facts traceable to source filenames.
- Preserve commands, measurements, errors, fixes, design decisions, and assumptions.
- Separate confirmed facts from guesses or open questions.
- Keep pages short enough to be useful, but detailed enough to reproduce results.

## Required behavior

When processing new files from `inbox/`:

1. Create one source summary in `sources/` for each raw file.
2. Update or create relevant pages in `wiki/`.
3. Add links between related wiki pages.
4. Add source references like: `Source: sources/<filename>.md`.
5. Preserve exact commands, compile flags, important errors, and benchmark results.
6. If information conflicts with older pages, create a `Contradictions / Questions` section.
7. Do not delete old information unless it is clearly wrong; mark it as outdated instead.
8. Keep technical claims grounded in the source material.
9. For code changes, explain what changed, why it changed, and how to test it.
10. For hardware/PCB work, record component names, pin connections, voltage assumptions, and unresolved checks.

## Page style

Each wiki page should usually contain:

```markdown
# Page Title

## Summary

## Current Status

## Key Details

## Commands / Steps

## Results / Evidence

## Open Questions

## Related Pages

## Sources
```

## Naming style

Use lowercase filenames with hyphens:

```text
openmp-parallelization.md
vck190-acceleration.md
ransac-ellipse-detection.md
kicad-pcb-design.md
```
