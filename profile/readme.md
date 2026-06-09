# Blocklog

**Forensic Debugging and Compliance Infrastructure for AI Financial Agents**

Blocklog runs in shadow mode alongside AI agents making financial decisions.

It captures every decision, records exactly which inputs the agent used, measures how stale those inputs were at decision time, and creates a complete forensic record of execution.

From that single record, Blocklog produces two outputs:

1. A forensic replay engine for engineers.
2. A compliance report for regulators and auditors.

The same data powers both.

No existing product serves both audiences.

Blocklog does.

---

# The Problem

AI agents are already making autonomous decisions inside financial systems.

They approve refunds.

They adjudicate chargebacks.

They score fraud risk.

They apply fees.

When an agent makes a bad decision, engineers need to answer a simple question:

**Why did the agent do that?**

Existing observability tools can show traces.

They can show prompts.

They can show tool calls.

They cannot reliably answer:

* Which inputs existed at the exact moment the decision was made?
* How old were those inputs?
* Which piece of context influenced the outcome?
* Why was one tool selected over another?
* What would have changed the decision?
* Which upstream step caused a downstream failure?

As a result, engineers spend hours reconstructing executions that lasted seconds.

At the same time, regulators are asking a different question:

**Can you prove how the AI made this decision?**

For financial AI systems, that is no longer optional.

Organizations need evidence showing:

* What the model saw
* When it saw it
* How fresh the data was
* Whether a human was involved
* How the final decision was reached

Today, engineering teams and compliance teams use entirely different systems.

Neither side gets the complete picture.

---

# The Blocklog Insight

The forensic record required for debugging is the same forensic record required for compliance.

Engineers and compliance officers have historically been served by separate tools.

Blocklog serves both from a single source of truth.

Every execution becomes a verifiable timeline of:

* Inputs
* Outputs
* Tool calls
* Decision points
* Context state
* Data freshness
* Human approvals
* System actions

Once captured, that record can be replayed by an engineer or reviewed by an auditor.

The underlying evidence is identical.

---

# How It Works

```text
AI Agent
    │
    ▼
Blocklog Shadow Mode
    │
    ▼
Decision Capture
    │
    ├── Inputs
    ├── Outputs
    ├── Tool Calls
    ├── Context State
    ├── Data Freshness
    └── Human Actions
    │
    ▼
Forensic Record
    │
    ├── Replay Engine
    └── Compliance Report
```

Blocklog operates alongside existing agent frameworks without modifying production behavior.

Every decision is timestamped, recorded, and linked into a complete execution history.

---

# Core Capabilities

## Forensic Replay Engine

Replay an AI execution exactly as it occurred.

Understand:

* What information the model used
* What information it ignored
* How stale critical inputs were
* Which tool selections changed outcomes
* Where failures originated

Engineers can move from hours of log reconstruction to minutes of investigation.

---

## Input Freshness Tracking

Many financial decisions fail because agents operate on outdated information.

Blocklog records:

* When each input was generated
* When the model consumed it
* Input age at decision time

Every decision can therefore be analyzed in the context of data freshness.

---

## Decision Provenance

Every output is linked to:

* Source inputs
* Intermediate reasoning steps
* Tool invocations
* Workflow state

This creates a complete chain of causality.

---

## Compliance Reporting

Generate auditor-ready reports directly from production activity.

Reports include:

* Decision history
* Input provenance
* Data freshness records
* Human oversight checkpoints
* Execution timelines
* Evidence artifacts

No manual reconstruction required.

---

## Tamper-Resistant Audit Trails

All forensic records are cryptographically protected.

Historical decisions can be verified independently and cannot be modified without detection.

---

# Product Roadmap

## Layer 0 — Replay Engine

The initial wedge.

Install Blocklog in shadow mode.

Capture every decision.

Replay failures in seconds instead of hours.

---

## Layer 0.5 — Compliance Reports

Generate compliance evidence from the same forensic data used for debugging.

Introduce compliance teams to an already deployed engineering tool.

---

## Layer 1 — Sentinel

Human-in-the-loop approval gates for high-risk financial actions.

Block decisions above configurable thresholds until explicit approval is granted.

Every approval becomes part of the forensic record.

---

## Layer 2 — Traceflow

Cross-agent execution visibility.

Trace decisions across entire multi-agent workflows.

Understand how actions from one agent propagate through downstream systems.

Planned: 2027

---

## Layer 3 — BlackVault

Agent identity, authorization, and execution security.

Define and enforce what agents are permitted to do before they can take action.

Planned: 2027–2028

---

# Why Now

AI financial agents have moved from experimentation to production.

The operational cost of opaque decision-making is already being paid by engineering teams.

At the same time, regulatory requirements are increasing across major jurisdictions.

Organizations need infrastructure that helps them understand AI decisions today and demonstrate accountability tomorrow.

Most observability tools solve only the engineering problem.

Most governance tools solve only the compliance problem.

Blocklog is built at the intersection of both.

---

# Vision

We believe every AI decision should be explainable, replayable, and auditable.

Blocklog is building the forensic infrastructure layer for autonomous financial systems.

As AI agents become responsible for increasingly consequential decisions, organizations will need more than logs.

They will need evidence.

Blocklog exists to provide it.

---

# Status

Blocklog is currently under active development.
