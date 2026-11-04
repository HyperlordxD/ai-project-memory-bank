# AI Project Memory Bank

Give your next AI session enough context to resume a technical project. Keep one current Markdown note per project, check off verified work, and keep a dated record of decisions that future contributors might revisit.

## Set up your copy

1. **GitHub:** Fork or download this repository, or copy its files into a folder such as `docs/memory/` in your project. Give your agent access to that working copy. **Obsidian:** Open the downloaded folder as a vault, or copy it into an existing vault. Either setup works with a Markdown editor alone.
2. Copy [the project template](templates/project.md) to `projects/<project-slug>.md`. Create the directory if needed. Replace the prompts with your goal, the source location, and one concrete next action. See the [worked example](examples/csv-export.md).
3. Add the instruction below to your agent’s project instructions, or paste it into a new chat. Replace the angle-bracket fields yourself or ask your agent to fill them in. Use a repository-relative path for a bank stored alongside code. For a separate vault, keep its local path in your own agent settings.

> For <project scope>, use the memory bank at <bank path>. Read its WORKFLOW.md and projects/<project-slug>.md. Summarize the last verified result and the next action. Update the source note when work is verified.

To restrict the workflow to a particular model, include its name in the scope. To use a callsign, add “After reading the note, begin the first update with <callsign>.”

## Test the handoff

Start a fresh session and ask it to resume your project. Can it name the goal, cite the last verified result, and identify the next action from the files? After completing that action, check that the original checkbox is marked done.

## What's inside

- [Workflow](WORKFLOW.md) — how to resume, verify, and hand off.
- [Milestone template](templates/milestone.md) — a short record for consequential changes.
- [Engineering and UX reference](reference/engineering-and-ux.md) — consult the relevant engineering guidance and use the full design review for interface work.
- [Obsidian next actions](next-actions.md) — optional view across projects.

This workflow draws on [Cline’s Memory Bank](https://cline.bot/blog/memory-bank-how-to-make-cline-an-ai-agent-that-never-forgets). Keep personal project history and credentials out of a publicly shared copy.
