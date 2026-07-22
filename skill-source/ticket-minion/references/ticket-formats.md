# Ticket formats

Use the exact template for the ticket type. Headings are level 2 (`##`) when the ticket is delivered as markdown text; adapt to the target tool's fields when creating in Jira (Title → Summary, everything else → Description).

## User Story

```
## Title
[Verb-first, outcome-focused, under 10 words. e.g. "Enable Dashboard Data Export to CSV"]

## Executive Summary
[2 to 4 sentences: what the application must allow, and why it matters to the perspective chosen. Written so a stakeholder with zero context understands the value.]

## User Story
As a [perspective], I want [capability] so that [benefit].

## Acceptance Criteria
1. [The system/dashboard/page must ... — visible entry point for the capability]
2. [When the [perspective] does X, the system must Y — the core happy path]
3. [Data/content fidelity requirement — output matches source]
4. [Format/compatibility requirement if relevant]
5. [Completion requirement — the action finishes successfully from the user's side]
6. [Empty state — if there is nothing to act on, the system must prevent the action or explain clearly]
7. [Error state — if the operation fails, the system must show an appropriate message and allow retry]
```

Include 5 to 8 criteria. Always include the empty state and error state criteria; adapt their wording to the feature. Add permission/access criteria when the perspective implies restricted data.

## Bug

```
## Title
[What is broken, where. e.g. "CSV export downloads empty file on Safari"]

## Executive Summary
[2 to 3 sentences: what is broken, who it affects, and the impact.]

## Affected Perspective
[Who hits this and in what context.]

## Steps to Reproduce
1. [Precondition: environment, account type, data state]
2. [Action]
3. [Action]

## Expected Behavior
[One or two sentences.]

## Actual Behavior
[One or two sentences. Include exact error text if known.]

## Acceptance Criteria
1. [Following the steps above must produce the expected behavior]
2. [Regression guard: the fix must not break adjacent behavior X]
3. [If applicable: the fix must apply across the affected environments/browsers/roles]

## Environment
[Browser/OS/app version/build if known; write "Unknown" rather than omitting.]
```

If the user cannot supply repro steps, write the steps as best-guess and mark them "(unconfirmed)". Ask for severity only if triage matters to the user.

## Epic

```
## Title
[The initiative in a phrase. e.g. "Self-Serve Data Export"]

## Executive Summary
[3 to 5 sentences: the problem space, who it serves, and what done looks like.]

## Goal
[One sentence, measurable where possible.]

## Perspectives Served
[The roles this epic touches and what each gets.]

## In Scope
1. [Capability]
2. [Capability]

## Out of Scope
1. [Explicit non-goal — prevents scope creep]

## Candidate Stories
1. [Story-sized slice, written as "As a X, I want Y so that Z"]
2. [Story-sized slice]
3. [Story-sized slice]

## Success Criteria
1. [Observable/measurable outcome that marks the epic done]
2. [Outcome]
```

Offer to expand any candidate story into a full user story ticket.

## Spike

```
## Title
Spike: [the question to answer. e.g. "Spike: Evaluate CSV generation libraries for large datasets"]

## Executive Summary
[2 to 3 sentences: what decision this spike unblocks and why it cannot be made yet.]

## Question(s) to Answer
1. [Specific answerable question]
2. [Specific answerable question]

## Timebox
[Ask the user; default suggestion 2 to 3 days.]

## Deliverable
[What artifact ends the spike: a written recommendation, a prototype, a benchmark table.]

## Acceptance Criteria
1. Each question above must have a documented answer with evidence.
2. The deliverable must include a recommendation with trade-offs.
```

## Task

```
## Title
[Verb-first. e.g. "Upgrade PostgreSQL to version 16 on staging"]

## Executive Summary
[1 to 3 sentences: what and why.]

## Details
[Whatever specifics the user provided: systems, versions, configs, links.]

## Acceptance Criteria
1. [Verifiable done-state]
2. [Verification step, e.g. "must pass X after the change"]
3. [Rollback/safety note if the task is risky]
```
