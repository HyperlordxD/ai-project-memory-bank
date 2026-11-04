# AI Project Memory Bank

Give your next AI session enough context to resume a technical project. Keep one current Markdown note per project, check off verified work, and keep a dated record of decisions that future contributors might revisit.

## Give this to your AI

Copy this prompt into an agent that can read the repository and edit your chosen workspace:

```text
Set up a project memory bank for me using https://github.com/HyperlordxD/ai-project-memory-bank. Follow the “Agent setup procedure” in its README. Make the files, configure startup, and tell me how to test a fresh session.
```

### Agent setup procedure

1. Identify the technical project and the user's preferred location. Default to `docs/memory/` in the current project. If they want Obsidian, ask for the vault folder if unknown. If they want the bank shared across projects, use one bank and a distinct note per project. Confirm any desired model restriction or callsign. Default to this technical project with no callsign.
2. Copy the workflow, templates, reference, and next-actions note into the destination, preserving relative paths. Create `projects/` and `logs/`. If the bank already exists, reuse it and preserve existing notes. Work in the user's copy of the template.
3. Create `projects/<project-slug>.md` from the project template. Fill in the goal, source location, verified state, and one actionable checkbox tagged `#project-next`. Inspect available project evidence. Ask for missing goals and label unverified claims explicitly.
4. Add a short startup rule to the agent's supported persistent project instructions (for example, an existing `AGENTS.md` when supported). Preserve existing instructions. For an explicitly requested cross-project setup, use supported user-level instructions and scope the rule to the selected projects and model. On startup, read the bank workflow and the matching current note. For a new project, create its note from the template. Use the chosen callsign only after reading the bank. Keep machine-specific vault paths in local settings. If persistent instructions are unavailable, give the user the filled-in startup rule to paste in each fresh chat.
5. Follow WORKFLOW.md for verification and handoffs. Load the full UX reference for interface work. In Obsidian, the optional Tasks plugin renders next-actions.md. Keep actionable checkboxes in the project notes so plain Markdown also works.
6. Verify the startup rule points to the real workflow and project note, and that the note contains the intended next action. Report the files created or reused. Give the user the exact phrase “Resume <project name>” with the name filled in. Record fresh-session recovery as verified only after a separate session succeeds or the user confirms it.

## Set up your copy manually

1. **GitHub:** Fork or download this repository, or copy its files into a folder such as `docs/memory/` in your project. Give your agent access to that working copy. **Obsidian:** Open the downloaded folder as a vault, or copy it into an existing vault. Either setup works with a Markdown editor alone.
2. Copy [the project template](templates/project.md) to `projects/<project-slug>.md`. Create the directory if needed. Replace the prompts with your goal, the source location, and one concrete next action. See the [worked example](examples/csv-export.md).
3. Add the instruction below to your agent’s project instructions, or paste it into a new chat. Replace the angle-bracket fields yourself or ask your agent to fill them in. Use a repository-relative path for a bank stored alongside code. For a separate vault, keep its local path in your own agent settings.

> For <project scope>, use the memory bank at <bank path>. Read its WORKFLOW.md and projects/<project-slug>.md. Summarize the last verified result and the next action. Update the source note when work is verified.

To restrict the workflow to a particular model, include its name in the scope. To use a callsign, add “After reading the note, begin the first update with <callsign>.”

## Test the handoff

Start a fresh session and ask it to resume your project. Can it name the goal, cite the last verified result, and identify the next action from the files? After completing that action, check that the original checkbox is marked done. *Tip: Use a callsign to check if the agent is receiving the information at the start of the project*

## What's inside

- [Workflow](WORKFLOW.md) — how to resume, verify, and hand off.
- [Milestone template](templates/milestone.md) — a short record for consequential changes.
- [Engineering and UX reference](reference/engineering-and-ux.md) — consult the relevant engineering guidance and use the full design review for interface work.
- [Obsidian next actions](next-actions.md) — optional view across projects.

This workflow draws on [Cline’s Memory Bank](https://cline.bot/blog/memory-bank-how-to-make-cline-an-ai-agent-that-never-forgets). Keep personal project history and credentials out of a publicly shared copy.
