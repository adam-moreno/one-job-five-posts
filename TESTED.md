# What was tested

2026-11-25, version 0.1.0.

**Tested**

- **Claude Code CLI 2.1.332, macOS 15.3.1, project install, from a FRESH CLONE of this repository.** The skill folder was copied into a new, empty project's `.claude/skills/`, with only project settings loaded (`--setting-sources project`) and only the Read tool allowed. Invoked headless as `/one-job-five-posts` with `examples/before/job-notes.md` (a made-up roofer). It was run twice:
  - **First run:** the question post used a customer question the owner never gave. The skill was changed so such a question is marked "(check: do you hear this?)" with the answer left blank.
  - **Second run** (the example): five posts, a 10-step shot list in on-site order, and a posting order. The added question is marked "(check: do you hear this?)". The roof shots go to the helper, and the missing fact is left as a blank.
  - The output is `examples/after/five-posts-plan.md`, unedited.
- **Unit tests** (`python3 -m unittest discover -s tests`): 11 pass, from the fresh clone. The invented-proof check fails on a known-bad line ("Rated 5 stars by 200 owners").

**Not tested**

- A job with no helper on site, or one where the customer said no to filming.
- A personal install in `~/.claude/skills/` (same mechanism as the project install, but not run).
- The Claude Code desktop app, web app and IDE extensions; the Claude apps' skill upload; the Agent SDK.
- Windows and Linux.
- Other businesses and trades, and more than one run. One run on one made-up business is not evidence that every output will be this good. Read what it gives you.
- Whether its output gets more views or customers. Nothing here measures that.
