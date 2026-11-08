---
"name": "review-for-completion"
"description": "Review whether a change satisfies its claimed acceptance criteria and tests their behavior. Use when asked whether a ticket or scoped PR is complete."
---

# Review for completion

## Scope

If told what to review, use that.

Otherwise, inspect `git status --short`; prefer unstaged changes, or staged if
no unstaged exist. If all work is committed and the branch holds a single unique
commit, use that. Stop and ask before reviewing an entire multi-commit branch.

## Context

Identify the change's tickets from what you're told, or from the branch,
commits, or PR body. The same sources, or the user's request, may limit it to
some of those tickets' ACs. If the tickets or their ACs cannot be established,
report that instead of reviewing.

## Instructions

Judge the change against its tickets' acceptance criteria, and read them before
the diff. If the change is limited to some of those ACs, hold it to only those;
otherwise every AC is required. Don't invent requirements.

- Map each required AC to implementation evidence. Flag unmet, partial, or
  quietly reinterpreted criteria.
- Does each required AC have a test that would fail on regression? Check the
  tickets' edge cases and unhappy paths. Check for repo norms before requiring a
  test for every edge case.

Verify findings by reading and tracing the code, not by running it. Don't rerun
existing test suites, builds, or checks. Note what you couldn't verify with the
finding it affects, or in your summary.

Name the AC each finding is about.

## Reporting Findings

List each finding, clearly identifying the file name, line number, and a
description of the rule that was violated + a proposed change if relevant. No
more than one or two sentences for each finding.

Be courteous of the implementor's time. Each finding is a request for them to
switch context and consider your feedback. No valuable, actionable findings is a
valid outcome.

Offer fixes, but edit only when explicitly authorized.
