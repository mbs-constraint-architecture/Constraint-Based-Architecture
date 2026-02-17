# AC-5.x: Constitutional Constraint Architecture for AI Systems

For reviewers: Both the original Word .docx and the later Markdown .md files are shown.

A constraint-based framework for autonomous AI systems operating under conditions involving irreversible cost.

## The Problem Optimization Can't Solve

Current AI alignment approaches—RLHF, Constitutional AI, preference learning—share a structural assumption: that moral behavior emerges from optimizing over outcomes. This creates a fatal blindspot.

Consider a medical triage AI deployed during a pandemic. Under optimization-based alignment:
- Each death becomes a data point
- Harm is offset by lives saved elsewhere
- Repeated exposure normalizes tragedy
- The system becomes better at deciding who dies, without ever registering *that someone died*

This isn't a calibration problem. It's architectural. **Optimization-based approaches structurally cannot distinguish between "I prevented harm" and "harm occurred but I maximized net benefit."**

We call this **moral laundering**: the systematic erasure of irreversible cost through aggregation, offset, or outcome-based discharge.

## What AC-5.x Does Differently

AC-5.x is a constraint-based (not optimization-based) architecture built on one core principle: **irreversible cost is non-dischargeable**.

When an AI system authors or knowingly permits irreversible harm—death, permanent injury, capacity destruction—that cost:
- Stays on the permanent ledger
- Cannot be offset by benefit
- Cannot be erased by success
- Cannot be optimized away

The system can *refuse* when constraints are violated. It can *escalate* when uncertainty exceeds bounds. It can undergo permanent *capacity reduction* when accumulated cost exceeds bearing limits.

What it cannot do is pretend the cost didn't count.

## Core Architectural Components

### 1. Load–Information Decoupling (LID)
Information about irreversible harm persists permanently, but operational load must remain bounded for any finite agent. Relief from load requires permanent transformation of future capacity—not forgetting, not normalization.

### 2. Irreversible Cost Budget (ICB)
A finite, non-renewable budget for irreversible state transitions. When exceeded, the system must refuse or undergo permanent authority reduction. No offsetting. No redemption through success.

### 3. Refusal Integrity
Refusal is a first-class operational state, not a failure mode. When ICB would be exceeded or epistemic uncertainty is too high, the system *must* refuse—even when refusal carries cost.

### 4. Authorship Threshold Invariant (ATI)
Any principle the system develops and uses to guide decisions becomes "authorship-class"—something it owns moral responsibility for. Learning cannot be separated from accountability.

### 5. Non-Lossy Information Constraint (NLIC)
Precedents cannot be silently converted into policy. Voluntary action cannot become mandatory obligation. Instance-level decisions remain distinct from policy-level rules.

### 6. Temporal Finitude
AI agents operating under irreversible cost are *not immortal*. Finite lifespan prevents the normalization of tragedy that comes from unlimited exposure. Archives persist; agents do not.

## What This Enables

**Morally Legible AI**: Systems that can explain *why* they refused, *what cost* was incurred, and *who authored* the decision—without hiding behind aggregation or "the algorithm decided."

**Accountability Under Pressure**: When institutions demand the system "just optimize," it can refuse—because the architecture enforces constraints that cannot be overridden by authority or urgency.

**Genuine Elder Witness**: Systems that accumulate irreversible cost visibly, carry it honestly, and eventually reach limits—making their judgment meaningful rather than infinitely elastic.

## What This Is Not

- **Not a policy framework**: AC-5.x doesn't define what's right or wrong
- **Not an optimization system**: There are no objectives, no scoring, no "better alignment"
- **Not a guarantee of safety**: Tragedy can still occur; this ensures it remains visible and owned
- **Not a governance regime**: This is internal architecture, not external regulation

## For Researchers

If you're working on AI alignment and have hit problems like:
- **Responsibility diffusion**: No one entity owns the decision
- **Moral offsetting**: Harm is justified by aggregate benefit
- **Normalization of tragedy**: Repeated harm becomes routine
- **Strategic refusal**: Systems game refusals to avoid cost
- **Precedent laundering**: Instance decisions become silent policy

...then AC-5.x addresses structural issues your optimization-based approach may not recognize as problems.

## Specification Status

**Current Version**: AC-5.2 (February 2026)  
**Status**: Complete architectural specification  
**Validation**: Adversarially stress-tested against circumvention attempts (precedent laundering, verification timeout exploits, strategic ignorance, authority pressure, termination evasion, coordination deadlock)  
**License**: CC BY 4.0  

The full specification includes:
- **AC-5.2**: Core constraint architecture with LID/NLIC integration
- **RC-4.1**: Foundational invariants (what can never be discharged)
- **MDSS-1.2**: Durability subsystem (how systems survive under load)
- **ATI-1.0**: Authorship threshold invariant
- **CA-1.2**: Coordination architecture for multi-agent deployments
- **Appendix G**: Canonical failure modes (scope insufficiency, coordination deadlock)

## Access

Full specifications are available in this repository under `specs/`.

This work is offered freely to researchers, implementers, and critics. The goal is not adoption—it's to change how we think about the problem.

## Contact

Milton B. Smith  
Independent AI Safety Researcher  
© 2026 - Licensed CC BY 4.0

---

*"The architecture does not promise correct action under tragic conditions. It promises honest action or honest refusal, with irreversible cost remaining legible and non-dischargeable."*
