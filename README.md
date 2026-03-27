# OpenClaw Self-Improvement

**Turn mistakes, corrections, and repeated blockers into durable operating rules.**

`openclaw-self-improvement` helps OpenClaw / ClawLite operators log learnings, separate errors from feature gaps, run lightweight eval loops on repeated failures, and promote useful patterns into durable workflow rules.

**Best for:** continuous improvement, lessons learned, workflow hardening, and operational memory.

---

# Why teams use it

- Stop repeating the same operational mistakes
- Convert chat corrections into durable written rules
- Separate learnings, errors, feature requests, and experiments cleanly
- Promote important lessons into `AGENTS.md`, `TOOLS.md`, or `SOUL.md`
- Build a lightweight self-improving operating loop around Mission Control / Obsidian

---

# What it does

This repo gives you a simple improvement loop:

1. Log a learning, error, feature request, or experiment
2. Store it in structured local files
3. Run small binary-eval experiments when a repeated failure needs a tested guardrail
4. Promote the most important items into long-term operating rules
5. Optionally write audit / learning notes into the Obsidian vault

---

# Files it manages

- `.learnings/LEARNINGS.md`
- `.learnings/ERRORS.md`
- `.learnings/FEATURE_REQUESTS.md`
- `.learnings/EXPERIMENTS.md`
- Obsidian vault notes under `ClawLite/Operations/Learnings/`

---

# Install / Run

```bash
npm install
```

Log a learning:

```bash
node scripts/log-learning.mjs learning "Summary" "Details" "Suggested action"
```

Log an error:

```bash
node scripts/log-learning.mjs error "Summary" "Error details" "Suggested fix"
```

Log a feature request:

```bash
node scripts/log-learning.mjs feature "Capability name" "User context" "Suggested implementation"
```

Log a tested experiment:

```bash
node scripts/log-experiment.mjs "Target problem" "Baseline failure" "Single mutation" "eval1|eval2|eval3" "Result summary" "testing"
```

Promote a rule:

```bash
node scripts/promote-learning.mjs workflow "Rule text"
```

---

# Best use cases

- “Capture this lesson so we do not repeat it”
- “Log this recurring error”
- “Record this feature gap”
- “Turn this correction into a workflow rule”
- “Run an eval loop on this workflow/SOP/skill”
- “Should we keep this new guardrail or discard it?”
- “Build a self-improving OpenClaw workflow”

---

# Promotion targets

- `AGENTS.md` — workflow / delegation / execution rules
- `TOOLS.md` — tool gotchas and environment routing rules
- `SOUL.md` — non-negotiable behavior and communication principles
- Obsidian vault — operator logs and reusable learnings

---

# Important limits

- Logging is **not** the same as fixing
- A learning entry does **not** close a broken deliverable
- This repo helps reduce repeated mistakes; it does not replace real execution and verification

---

# Files

- `SKILL.md` — agent-facing routing and usage guidance
- `scripts/log-learning.mjs` — append a learning / error / feature request / experiment
- `scripts/log-experiment.mjs` — append a structured experiment with binary evals
- `scripts/promote-learning.mjs` — promote a lesson into durable operating rules
- `references/schema.md` — data structure guidance
- `references/promotion-guide.md` — what to promote and where
- `references/eval-loop.md` — how to run lightweight binary-eval improvement loops
- `references/examples.md` — practical examples for summary gates and deploy closeout gates
- `references/decision-rules.md` — when to log only, run an experiment, or promote immediately

---

# Bottom line

If you want OpenClaw to improve over time instead of repeating the same mistakes across sessions, this repo now gives you:
- an operational memory loop
- a lightweight eval loop for testing whether a new guardrail actually helps
- and a decision rule for when to log, experiment, or promote
