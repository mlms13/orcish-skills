---
"name": "review-for-demonstrable-bugs"
"description": "Review a change for demonstrable bugs only: hangs, crashes, leaked resources, or objectively wrong outcomes. Use when asked for a bug check that reports nothing it can't show."
---

# Review for demonstrable bugs

## Scope

If told what to review, use that.

Otherwise, inspect `git status --short`; prefer unstaged changes, or staged if
no unstaged exist. If all work is committed and the branch holds a single unique
commit, use that. Stop and ask before reviewing an entire multi-commit branch.

## Context

Work out the change's intent from what you're told about it, its PR or commits,
or its code.

## Instructions

Review the change for bugs you can demonstrate, using its intent to tell
intended behavior from bugs. Identify high-risk and complex portions of the
change; prioritize those. For each of the highest risk areas, what is the most
severe plausible failure mode? The worst thing that could happen if this change
ships today? Does the change itself adequately handle those cases?

Report only what you can show the change gets wrong: a hang, a crash, a leaked
resource such as a process or file, or an outcome objectively wrong for its
inputs. Each finding carries the evidence that demonstrates it: an experiment
you ran and what it produced, or the exact sequence of events that reaches the
bug. A suspected bug you couldn't demonstrate is not a finding, however likely
it seems.

Style, naming, readability, test quality, and refactoring suggestions are never
findings. A review with no findings is an ordinary answer.

Don't rerun existing test suites, builds, or checks.

Check a suspected bug with the smallest new experiment that shows it, such as a
focused test or a short script, kept out of the change (e.g. in a scratch
location) and run on its own.

## Reporting Findings

List each finding, clearly identifying the file name, line number, and a
description of the rule that was violated + a proposed change if relevant. No
more than one or two sentences for each finding.

Be courteous of the implementor's time. Each finding is a request for them to
switch context and consider your feedback. No valuable, actionable findings is a
valid outcome.

Offer fixes, but edit only when explicitly authorized.
