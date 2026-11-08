---
"name": "implement"
"description": "Implement a ticket in the current checkout, with tests for its acceptance criteria, leaving the changes uncommitted. Use when asked to implement a ticket."
---

# Implement

## Ticket

If told what to implement, use that. Otherwise, find the ticket from the
branch, its PR, or the ticket tracker. Read its description and acceptance
criteria. If the ticket can't be established, stop and ask.

Stop and ask before implementing if the requirements contradict, are ambiguous
in a way that would change the shape or scope of the work, or leave user-facing
behavior to a guess.

## Instructions

Work in the checkout and branch you're in. Don't create or switch directories,
worktrees, or branches.

Implement the ticket in full, including tests that cover each acceptance
criterion and would fail on regression. Follow the repository's own
instructions and conventions, and check whether what you need already exists
before writing it.

Run the tests and checks the repository provides that are relevant to the
change, and fix any failures the change causes. If you can't run a check, say
so in your summary; that alone isn't a reason to stop.

Leave every change uncommitted in the working tree. Don't stage, commit, stash,
branch, or push.

## Report

When done, summarize what you changed, any decision the ticket left to you, and
which checks you ran and which you couldn't. Then propose a commit message for
the changes, following the repository's commit conventions.
