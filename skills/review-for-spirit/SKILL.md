---
"name": "review-for-spirit"
"description": "Review whether a change serves its larger goal and the work it unblocks. Use when asked to check downstream expectations or alignment beyond ACs."
---

# Review for spirit

## Scope

If told what to review, use that.

Otherwise, inspect `git status --short`; prefer unstaged changes, or staged if
no unstaged exist. If all work is committed and the branch holds a single unique
commit, use that. Stop and ask before reviewing an entire multi-commit branch.

## Context

Identify the change's tickets from what you're told, or from the branch,
commits, or PR body, then the tickets they block. Use ticket bodies you're
given; retrieve only what's missing. If the change's tickets cannot be
established, report that instead of reviewing. If the tickets they block cannot
be, say so and weigh the change against its own tickets alone.

## Instructions

Before the diff, read its tickets' intent and acceptance criteria, then the
tickets they block. Don't invent needs those tickets don't state.

Determine the larger goal and what downstream work expects from this change.
Flag mismatched contracts or decisions that would force planned work to undo
this implementation, even if its ACs pass. Tie each finding to a concrete
downstream requirement; avoid speculative future-proofing.

Verify findings by reading and tracing the code, not by running it. Don't rerun
existing test suites, builds, or checks.

## Reporting Findings

List each finding, clearly identifying the file name, line number, and a
description of the rule that was violated + a proposed change if relevant. No
more than one or two sentences for each finding.

Be courteous of the implementor's time. Each finding is a request for them to
switch context and consider your feedback. No valuable, actionable findings is a
valid outcome.

Offer fixes, but edit only when explicitly authorized.
