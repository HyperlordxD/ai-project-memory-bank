# CSV export · fictional example

## Goal
Let a support analyst open exported ticket titles in a spreadsheet with one row per ticket.

## Technical context
The export writer lives in `src/export/`. The parser round-trip test is the acceptance check.

## Current state
A title containing a comma survives the round trip. Embedded line breaks still need coverage.

## Actions
- [x] Verify that a title containing a comma stays in one field.
- [ ] Add a case with an embedded newline and verify the parsed row count. #project-next
