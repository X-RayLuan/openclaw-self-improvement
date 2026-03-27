# OpenClaw Self-Improvement

**OpenClaw Self-Improvement** is a skill for turning repeated AI-agent mistakes into durable operational improvements.

It helps OpenClaw / ClawLite operators and agent teams:
- log recurring failures
- separate one-off errors from reusable lessons
- run lightweight **binary eval loops** on new guardrails
- classify changes as **keep**, **partial_keep**, or **discard**
- promote proven fixes into SOPs, checklists, workflow rules, and operating policy

If you care about reducing fake-complete states, tightening QA truth, improving deploy closeout, and making agent learning inspectable, this skill is built for that job.

---

## Why this skill exists

Many AI systems say they "learn," but most only store lessons in chat history or loose notes.

That is not enough.

Operationally, repeated failures tend to come back in the same forms:
- delivery gets described as complete before proof exists
- receipts are missing or too thin
- back-end fixes never reach the operator-facing surface
- code-ready states get confused with production-ready states
- teams add new rules without checking whether those rules actually reduce failure

OpenClaw Self-Improvement gives you a lightweight operating loop for fixing that.

---

## What problem it solves

This skill helps with:
- **self-improving AI workflows**
- **AI operations learning loops**
- **binary evals for agent guardrails**
- **Mission Control truth-state improvement**
- **deploy closeout verification**
- **receipt / proof completeness**
- **repeated failure prevention in multi-agent systems**

It is especially useful in OpenClaw-style environments where multiple agents, tools, SOPs, and truth surfaces interact.

---

## What’s new in v0.2.0

### New capabilities
- **Experiment mode** for repeated failures
- **Binary eval loops** for testing whether a new guardrail or SOP actually helps
- **Keep / partial_keep / discard** decision model
- **Practical examples** for:
  - Mission Control summary quality
  - deploy closeout / production verification
- **Experiment summary helper** for surfacing unresolved follow-up debt
- **Decision rules** for when to log, experiment, or promote
- **Daily routine integration** with heartbeat, Karen QA, AGENTS, and ops policy

### Why it matters
This release makes self-improvement more operational.

Instead of stopping at “lesson learned,” you can now:
1. capture the repeated problem
2. define a baseline
3. test one change at a time
4. evaluate with binary checks
5. keep, discard, or mark `partial_keep`

That makes the improvement loop much more auditable and much less hand-wavy.

---

## Core workflow

OpenClaw Self-Improvement now supports a practical loop:

1. **Capture** a learning, error, feature request, or experiment
2. **Store** it in structured local files
3. **Experiment** when a repeated failure needs a tested guardrail
4. **Evaluate** the change with binary checks
5. **Promote** proven fixes into durable rules, SOPs, or policies
6. **Track follow-up debt** when a fix is only partial

---

## Best use cases

Use this skill when you want to:
- capture lessons so agents stop repeating the same mistake
- log recurring operational errors
- track feature gaps revealed by repeated work
- test whether a new workflow rule really improves outcomes
- run a lightweight eval loop on a skill, SOP, checklist, schema, or handoff rule
- decide whether a new guardrail should be kept, discarded, or promoted
- build a self-improving OpenClaw or ClawLite operating loop

Typical targets include:
- Mission Control summary quality
- deploy closeout gates
- receipt requirements
- QA wording rules
- truth-surface rendering checks
- handoff contracts between agents

---

## Files it manages

- `.learnings/LEARNINGS.md`
- `.learnings/ERRORS.md`
- `.learnings/FEATURE_REQUESTS.md`
- `.learnings/EXPERIMENTS.md`
- Obsidian vault notes under `ClawLite/Operations/Learnings/`

---

## Install

```bash
npm install
```

---

## Usage

### Log a learning

```bash
node scripts/log-learning.mjs learning "Summary" "Details" "Suggested action"
```

### Log an error

```bash
node scripts/log-learning.mjs error "Summary" "Error details" "Suggested fix"
```

### Log a feature request

```bash
node scripts/log-learning.mjs feature "Capability name" "User context" "Suggested implementation"
```

### Log a tested experiment

```bash
node scripts/log-experiment.mjs "Target problem" "Baseline failure" "Single mutation" "eval1|eval2|eval3" "Result summary" "testing"
```

### Promote a rule

```bash
node scripts/promote-learning.mjs workflow "Rule text"
```

### Summarize experiment outcomes

```bash
node scripts/experiment-summary.mjs
```

---

## Decision model

This skill uses three levels of action:

### 1. Log only
Use when:
- the issue happened once
- root cause is still unclear
- there is not enough evidence yet to make a rule

### 2. Experiment
Use when:
- the issue repeated 2+ times
- a new guardrail / SOP / checklist / schema change is being proposed
- you can define 3–5 binary evals

### 3. Promote
Use when:
- the rule is clearly right and low-risk
- the issue is severe enough that waiting would be irresponsible
- the rule is about ownership, truth, or a non-negotiable operating principle

---

## Practical examples

The skill now includes concrete examples for:
- **Mission Control summary link-complete gates**
- **ClawLite deploy closeout gates**

These examples show how to:
- define the repeated failure
- capture the baseline
- propose one mutation
- evaluate with binary checks
- classify the outcome as `keep`, `partial_keep`, or `discard`

---

## Promotion targets

Promote proven improvements into:
- `AGENTS.md` — workflow / delegation / execution rules
- `TOOLS.md` — tool gotchas and environment routing rules
- `SOUL.md` — behavior / communication / non-negotiable principles
- `docs/ops/*.md` — SOPs, policy, and operating contracts
- Obsidian vault — reusable operator notes and operational memory

---

## Important limits

- Logging is **not** the same as fixing.
- A learning entry does **not** close a broken deliverable.
- A back-end-only improvement is not complete if the visible operator-facing surface is still stale.
- `partial_keep` should be treated as **active follow-up debt**, not as closure.

---

## Repository contents

- `SKILL.md` — agent-facing routing and usage guidance
- `scripts/log-learning.mjs` — append a learning / error / feature request / experiment
- `scripts/log-experiment.mjs` — append a structured experiment with binary evals
- `scripts/experiment-summary.mjs` — summarize keep / partial_keep / discard outcomes and flag follow-up debt
- `scripts/promote-learning.mjs` — promote a lesson into durable operating rules
- `references/schema.md` — data structure guidance
- `references/promotion-guide.md` — what to promote and where
- `references/eval-loop.md` — how to run lightweight binary-eval improvement loops
- `references/examples.md` — practical examples for summary gates and deploy closeout gates
- `references/decision-rules.md` — when to log only, run an experiment, or promote immediately

---

## Why this is useful for SEO / GEO / AI search

This project is designed around concrete, quotable operational concepts that AI answer engines and human searchers both understand:
- self-improving AI workflows
- binary eval loops for agent operations
- repeated failure prevention
- Mission Control QA improvement
- deploy closeout verification
- durable operational learning for multi-agent systems

That makes it easier to explain, cite, and reuse than vague “AI reflection” systems.

---

## Bottom line

If you want OpenClaw to improve over time instead of repeating the same mistakes across sessions, this repo gives you:
- an operational memory loop
- a lightweight eval loop for testing whether a new guardrail actually helps
- a decision framework for when to log, experiment, or promote
- a way to keep unresolved partial improvements visible until they are actually closed
