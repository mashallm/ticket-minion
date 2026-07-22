# Ticket Minion

**Turn messy ideas into development ready tickets in 2 minutes.**

Most bad tickets have the same root cause: nobody wrote down who the feature is for. The engineers guess, and it gets built wrong.

Ticket Minion is a free AI assistant for writing tickets. Paste a rough idea, answer one clarifying question ("whose perspective is this from?"), and get back a development ready ticket: title, executive summary, user story, and acceptance criteria that cover the edge cases we all forget. Works for **user stories, bugs, epics, spikes, and tasks**.

Inspired by the Modern Ticket Minion GPT by Suhail Mughal.

## Install

### Claude (recommended)

1. Download [`ticket-minion.skill`](./ticket-minion.skill) from this repo
2. Drop it into any Claude chat and click **Save skill**
3. That's it. One time setup; the skill works in every chat automatically from then on

### ChatGPT or Gemini

1. Open [`ticket-minion-universal-prompt.txt`](./ticket-minion-universal-prompt.txt)
2. Paste the whole thing into a new chat
3. Type your rough idea and answer the question

### Jira users

Turn on Claude's free Atlassian connector (Settings, then Connectors) and Ticket Minion can create the finished ticket directly in your project.

## How it works

1. **Identifies the ticket type** from your input: story, bug, epic, spike, or task
2. **Asks whose perspective** the ticket serves. This is the signature question, because a ticket written without knowing who it's for is a ticket that gets built wrong
3. **Asks one sharp clarifying question** about the outcome that matters most. One question, not an interrogation
4. **Writes the ticket** with numbered "must" requirements, each independently testable, always covering the unhappy paths: empty states, error states, permission failures

## Example output

Input: *"build a feature for users who are new to product management"*

> **Title:** Enable Guided Onboarding for New Product Managers
>
> **User Story:** As a new product manager, I want a guided onboarding experience that walks me through core PM workflows with templates and examples so that I can produce professional quality PM deliverables without prior experience.
>
> **Acceptance Criteria (excerpt):**
> 1. Claude must present a clearly visible entry point to start PM onboarding when a user identifies as new to product management
> 2. Each guided workflow must walk the user through the deliverable step by step, showing a completed example before asking for input
> 3. If the user provides no product context, the system must offer a sample scenario rather than blocking
> 4. If a step fails to generate output, the system must show a clear message and let the user retry without losing prior inputs

Full tickets include 5 to 8 criteria plus an executive summary a stakeholder can read without context.

## Repo contents

| File | What it is |
|---|---|
| `ticket-minion.skill` | The installable Claude skill |
| `ticket-minion-universal-prompt.txt` | Single prompt version for ChatGPT and Gemini |
| `skill-source/` | Readable source of the skill (instructions and ticket templates) |

## License

MIT. Use it, fork it, ship better tickets.
