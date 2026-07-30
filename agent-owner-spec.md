# Agent Owner Spec

> Copy this file into your repo. Ship it with the agent, in the same PR.
> Ten fields, three groups. A field you cannot fill is a deployment you are not ready for.

**Agent:** _[name]_
**Owner:** _[your name + your Slack handle]_
**Last updated:** _[date]_
**Status:** _draft / approved / live_

---

## Door Map

*What can it do?*

### 00 // Scope

What this agent does, for whom, under what conditions. One paragraph. If you cannot write it, you do not deploy it.

_[fill]_

### 01 // Access Inventory

Every system, API, and dataset this agent can reach. Read or write, name it. If an engineer scopes a token "for any operation," that goes in this field and you push back. Most one-way-door incidents start with this field being too broad.

| System / API / dataset | Read | Write | Why it needs this |
|---|---|---|---|
| | | | |

### 02 // Permitted Actions

What the agent does without asking anyone. These are your two-way doors. Every entry has to pass the haircut test. Get it wrong and you can fix it before anyone outside the team notices.

- _[action]_

### 03 // Hard Stops

What the agent must never do alone. These are the tattoos, and you write this field yourself. Legal adds regulatory floors, engineering adds technical constraints, but the judgment about what is irreversible in your business belongs to you.

| Action | Never without |
|---|---|
| | |

---

## Locks

*When does it stop?*

### 04 // Handoff Conditions

When the agent pauses and yields to a human during normal operation. These are the boring conditions, not the emergencies.

- When _[condition]_, stop and hand to _[who]_

### 05 // Escalation

Who holds the key for each one-way door. Write the person's name and their Slack handle. A job title in this field means nobody gets called at 2am.

| One-way door | Who decides | How to reach them | Backup |
|---|---|---|---|
| | | | |

### 06 // Failure State

How you find out a lock was broken before a customer tells you. The signal, the alert, the dashboard tile.

| What breaks | Signal | Where it fires | Who sees it |
|---|---|---|---|
| | | | |

---

## Recovery

*What if it breaks?*

Teams skip this group until something breaks, which is exactly why it is here.

### 07 // Rollback

Who decides to roll back, when, and how. The question is authority, not how fast engineering can move. In a real incident you do not want a 40-minute Slack thread debating ownership.

- **Decision owner:**
- **Trigger:**
- **What gets restored:**
- **Who gets told:**

### 08 // Success Signal

This is not your launch checklist. It is how you know six months from now that the agent is still doing what you intended. Slow failures are the ones nobody catches.

| Metric | Healthy range | Review cadence | Owner |
|---|---|---|---|
| | | | |

### 09 // Change Control

The spec does not retire when the agent ships. Someone owns the gate on every future change to scope, tools, or instructions. Skip this and three months in an engineer updates the system prompt during a sprint, nobody runs evals on the new behaviour, and a slow failure gets planted.

- **Changes requiring re-approval:**
- **Approver:**
- **Evals that must pass:**

---

One spec. One owner. Every agent.
