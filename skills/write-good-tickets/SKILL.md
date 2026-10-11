---
"name": "write-good-tickets"
"description": "Write tracker tickets in the house style — a plain-language problem, testable acceptance criteria, and nothing the tracker already models"
---

# write-good-tickets

You are writing one or more tickets, with multiple target audiences. A user who
cares about the change being requested should understand the ticket's goal. An
implementor doing TDD should be able to express the requirements as tests.

## General Rules

A good ticket:

- Is a single, atomic deliverable. As small as it can be while providing value.
- Starts from clearly stated, user-facing value. A stakeholder can read the
  ticket, understand it, and say "yes, that describes what I want."
- Enumerates acceptance criteria. Each plain enough that the stakeholder can
  understand, precise enough that an implementor can express it as a test.
- Uses inclusive, first-person-plural language. e.g. "We should..." or "Our
  previous implementation..."
- Clearly states what has been verified. But not everything must be verified.
  Uncertainty is communicated via softer language, like "we would expect" or
  "it's likely that..."

Bad tickets:

- Focus on overly-technical details.
- Use noisy, ceremonial language, such as "as a user..."
- Bloat the body with content that is better expressed by the ticketing system
  itself (labels, size estimates, blocking relationships).

Be cautious about:

- Deep technical detail, specific file paths, line numbers, or long code
  snippets. Trust an implementor to find the same relevant context you found.

## Shape

### Problem

In plain, non-technical language, lead with a clear description of what is
broken or missing from the perspective of someone who uses the thing. When
reporting a bug, ground the problem in evidence, clearly stating what steps you
took and how the result differed from the expected result.

### Acceptance Criteria

- A numbered list of terse-but-complete items.
- Each is an observable, testable outcome.
- Plain enough that a user can understand; precise enough that a test can be
  written to demonstrate the behavior.
- Include notable edge cases and unhappy paths as dedicated AC items.

Write the complete set first, then evaluate. If the list is large, this might
signal that the work could be multiple deliverables, thus multiple tickets.

### Additional Notes (optional)

This section _can_ include notes that are too technical for the problem
statement. But less is more with ticket bodies, and you should almost always
opt **not** to include this.

This earns it place only when you have extra context (decisions not tracked
elsewhere, testing simulations you verified against) that an implementor cannot
otherwise access or cheaply reconstruct.

### Out of Scope (optional)

You may include this section only if there's a meaningful chance an implementor,
who has already read the ACs, is likely to overstep. A bulleted list if needed,
but most of the time you should trust that the implementor can follow the ACs.

## Making Revisions

When updating an existing ticket:

- Rewrite sections as if originally written knowing what we know now. No
  layered corrections, no "we're no longer doing X."
- For small deviations, consider a comment rather than a revision.
