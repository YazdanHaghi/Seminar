# Prompt: Code Review Into Wiki

Review the code files in `inbox/` and update the LLM Wiki.

For each important code file:

1. Summarize what the file does.
2. Identify parallelized sections, if any.
3. Identify performance bottlenecks.
4. Identify correctness risks.
5. Suggest improvements for CPU execution.
6. Suggest improvements for FPGA/VCK190 execution, if relevant.
7. Add build and run commands if present.
8. Update related wiki pages.

Keep exact function names, flags, and command-line options when available.
