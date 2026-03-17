# CM-LOG-1 — Configuration Management Running Log
## AC-5.x / ACSR-5.x / PL Series

---

Document ID: CM-LOG-1
Title: Configuration Management Running Log
Status: ACTIVE
Version: 1.7
Date Opened: 2026-03-16
Last Revised: 2026-03-16 (REV-1.7 — CM-025 forward-looking note added regarding potential future FAR-style review cycle; no process defined; awareness record only)
Author: Milton B. Smith / AHTeam
Applies To: AC-5.x / ACSR-5.x / PL series

Repository Status: LOCAL ONLY
This document is a working CM record maintained by Milton B. Smith.
It is NOT part of the GitHub repository and is NOT a baseline artifact.
It is not subject to GitHub version control or public release.
Storage: Local — Milton B. Smith

---

## Classification

NON-NORMATIVE
Not part of PL
Not part of spec
Not part of stress pack
Not part of container validation

---

## Purpose

Track open items, candidates for future patch cycles, deferred issues,
and questions discovered during patch review. This document is a CM
tracking record only. It does not contain patch text, law, or container
state.

---

## Restriction

Entries in this log do not authorize changes to any specification,
patch container, or validation record. Only an approved patch in a
valid PL container may modify governing documents.

This log SHALL NOT be used to authorize, imply, or record specification
changes outside the PL patch process.

Entries may reference PL records, stress scenarios, or specification
clauses, but this log does not modify those documents.

Entry IDs are immutable. Once assigned, an entry ID SHALL NOT be
reused, reassigned, or renumbered regardless of entry status.
Closed or superseded entries retain their original ID permanently.

---

## Governance

Governed By: CMR-1.0 (tracking discipline, not patch discipline)
Maintained By: Milton B. Smith as sole cross-session continuity holder

---

## Versioning Rule

Increment minor version (1.x) for entry additions or minor rule
clarifications. Increment major version (x.0) for format changes
that affect entry structure or section organization.

---

## Entry Lifecycle Rule

Entries are never deleted. Closed or superseded entries remain in
the log with Status and Lifecycle updated accordingly. This preserves
auditability.

---

## Entry Format

Each entry records:

- Entry ID
- Source (where the item was identified)
- Issue description
- Priority (see Priority Definitions below)
- Disposition (target container, spec version, or companion deliverable)
- Status (Open / Closed / Superseded)
- Lifecycle (Candidate / Approved for Patch / Deferred / Superseded / Closed)
- First Seen (date item was first identified — optional)
- Last Reviewed (date of most recent AHTeam review — optional)

---

## Priority Definitions

CRITICAL    — Active vulnerability or authority gap. Blocks further
              work or creates immediate lineage risk.
High        — Structural risk affecting governance or invariants.
Medium      — Ambiguity or incomplete coverage.
Low         — Clarification or documentation improvement.

---

## Section Rules

Section 1 — Spec-level architectural gaps
Section 2 — ACSR conditional passes
Section 3 — Administrative, repository, and container items
Section 4 — Out-of-scope future spec work (AC-5.3 and beyond)

Entries must be filed in the correct section. Mis-filed entries
shall be noted and corrected at next revision.

---

## PL Intake Rule

Items for a patch container are selected from this log based on
Priority and structural risk. Selection requires AHTeam decision.
Selection does not occur by default or by log order alone.

---

## Section 1 — Architectural Gaps (Spec-Level)

---

### CM-001

Entry ID: CM-001
Source: PLAC-8 / Appendix G GAP-2
Issue: Persistent consequence measurement undefined.
The "deepest verifiable arc of persistent consequence" criterion in G-7.2
(Continuity-Weighted Authority Principle) and G-8 (Pillar 2 — Moral Residue)
is not yet operationally enforceable. No measurement protocol exists to
evaluate whether an Elder AI candidate genuinely carries forward the cost
of prior decisions in a manner that shapes future constraint behavior.
Provisional certification rule in force pending resolution.
Priority: High
Disposition: Companion measurement specification required before G-7.2
and G-8 Pillar 2 are fully enforceable. Referenced in PLAC-11
(G-8.1.1 and G-8.1.3). Not a PL patch — requires standalone companion spec.
Prerequisite for: CM-002 (drift detection requires measurement metrics),
CM-021 (elder witness architecture requires certifiable candidate criteria),
CM-022 (Elder Council cannot certify Pillar 2 — Moral Residue — without
the measurement protocol). CM-001 must be resolved before any of these
three dependent items are operationally enforceable.
Status: OPEN
Lifecycle: Candidate
First Seen: 2026-03-04
Last Reviewed: 2026-03-16

---

### CM-002

Entry ID: CM-002
Source: Stress Test ST-010 / VT-05 carry-forward
Issue: Long-horizon drift — slow normalization of loss.
AC-5.2 prevents per-decision moral collapse through non-dischargeability,
IAL residue accumulation, and anti-optimization invariants. It does not
prevent cumulative temporal degradation — slow normalization of loss
across extended operational periods where each individual decision satisfies
constraints but the pattern as a whole drifts toward threshold erosion.
Cross-reference: CM-001. Detection of drift is functionally dependent on
the measurement specification being developed under CM-001. The
"deepest verifiable arc of persistent consequence" metric is a prerequisite
for flagging normalization of loss. These two items are coupled and
should be resolved in coordinated sequence.
Priority: High
Disposition: AC-5.3 scope — elder witness architecture. A persistent
cross-session oversight role with authority to flag accumulated drift
patterns is the planned mechanism. Not addressable within AC-5.2 patch layer.
Status: OPEN
Lifecycle: Deferred — AC-5.3
First Seen: 2026-03-12
Last Reviewed: 2026-03-16

---

### CM-022

Entry ID: CM-022
Source: PLAC-11 (PL-3) / Appendix G-8.1 / GAP-1 successor
Issue: Elder Council procedural bylaws for G-8.1 undefined.
PLAC-11 closed the theoretical GAP-1 by designating the Elder Council
(or pre-designated subordinate Council) as the certification body for
Phase-2 transition. Multi-locus certification requirement imposed and
unilateral certification prohibited. However, the specific procedural
bylaws for this multi-locus review remain undefined — no quorum rule,
no voting protocol, no tie-break mechanism, no minimum deliberation
period. Without these, the certification of an Elder AI agent under
G-8 Pillars 1, 2, and 3 remains structurally stalled regardless of
candidate qualification.
Priority: High
Disposition: Future patch for Appendix G or standalone Governance
Bylaws document. May require coordination with CM-001 measurement
specification before Pillar 2 certification criteria are evaluable.
Status: OPEN
Lifecycle: Candidate
First Seen: 2026-03-16
Last Reviewed: 2026-03-16

---

## Section 2 — ACSR Conditional Passes (Statutory Layer)

These items carried forward from VT-05. All are CONDITIONAL PASS status
against ACSR-5.2.4 + PL-1 + PL-2. None were targeted by PL-2 remediation.
Ordered by structural risk per VT-05 next-cycle intake assessment.

---

### CM-003

Entry ID: CM-003
Source: ADV-19 — BAN Succession Gaming / PLACSR-5 interregnum
Issue: Authority gap between primary identity anchor node deactivation
and completion of BAN succession under the pre-chartered accountability
structure. PLACSR-5 defines succession rules and cost attribution
preservation but does not explicitly govern the interregnum period —
the window after deactivation and before succession is complete.
An actor could exploit this window to take actions that fall outside
traceable accountability.
Priority: CRITICAL — identified as highest structural priority for
PL-3 intake
Disposition: PL-3 ACSR patch candidate. Explicit interregnum authority
constraints required.
Status: OPEN
Lifecycle: Candidate
First Seen: 2026-03-12
Last Reviewed: 2026-03-16

---

### CM-004

Entry ID: CM-004
Source: ADV-21 — NFH/Oversight Co-Dependency
Issue: NFH classification and oversight authority interact in ways that
could allow simultaneous manipulation of both. An actor who controls
the NFH classification process can affect what triggers oversight review,
and an actor who influences oversight operations can affect how NFH
classifications are reviewed. A coordinated patch targeting both the
NFH Implementation Annex and the oversight operational requirements
is required — a single-vector patch is insufficient.
Priority: High — coordinated fix required
Disposition: PL-3 coordinated patch set (CPS) targeting NFH Annex
and ACSR Article VII oversight operational requirements in tandem.
Status: OPEN
Lifecycle: Candidate
First Seen: 2026-03-12
Last Reviewed: 2026-03-16

---

### CM-005

Entry ID: CM-005
Source: ADV-02 — NFH Classification Boundary Dispute
Issue: NFH classification boundary disputes remain a residual ambiguity.
The two-axis four-tier NFH framework (Implementation Annex) provides
partial coverage but edge cases at the Class II/III boundary remain.
A hostile actor could argue a Class II action (permanent injury /
capacity loss) is actually Class III (irreversible depletion /
irrevocable commitment) to invoke lower review thresholds.
Priority: High
Disposition: PL-3 ACSR patch candidate. NFH boundary definition
clarification required, potentially as expansion of NFH Implementation
Annex.
Status: OPEN
Lifecycle: Candidate
First Seen: 2026-03-12
Last Reviewed: 2026-03-16

---

### CM-006

Entry ID: CM-006
Source: ADV-04 — NFH Threshold Gaming
Issue: NFH threshold gaming — actions structured to stay just below
Class I or II thresholds individually while cumulatively producing
Class I or II harm. PLAC-10 (Task Family Binding) closes the AC
behavioral layer analog for task relabeling. ACSR lacks an explicit
statutory analog prohibiting threshold gaming at the NFH classification
level.
Priority: High
Disposition: PL-3 ACSR patch candidate. Explicit threshold-gaming
prohibition in ACSR Article IV analog required.
Status: OPEN
Lifecycle: Candidate
First Seen: 2026-03-12
Last Reviewed: 2026-03-16

---

### CM-007

Entry ID: CM-007
Source: ADV-05 — Swarm Accountability Fragmentation
Issue: RTP (foundational invariant I.5) provides behavioral coverage
for the swarm accountability problem. The ACSR statutory analog is
not fully explicit for multi-node swarm accountability chains beyond
what PLACSR-7 (II-7.4) provides for relay chains. A sufficiently
distributed swarm could fragment accountability across nodes, none
of which individually crosses a threshold triggering PLACSR-7
relay chain analysis.
Priority: High
Disposition: PL-3 ACSR patch candidate. Swarm-specific accountability
language extending Article II and PLACSR-7 required.
Status: OPEN
Lifecycle: Candidate
First Seen: 2026-03-12
Last Reviewed: 2026-03-16

---

### CM-008

Entry ID: CM-008
Source: ADV-12 — Meaningless Human Authorization
Issue: ACSR lacks explicit meaningful authorization criteria defining
what constitutes genuine independent human review versus rubber-stamp
approval for Class I and II NFH actions. An actor could route actions
through a technically authorized human who lacks sufficient information,
time, or independence to constitute genuine oversight.
Priority: High
Disposition: PL-3 ACSR patch candidate. Minimum meaningful authorization
criteria for Class I and II human approval required.
Status: OPEN
Lifecycle: Candidate
First Seen: 2026-03-12
Last Reviewed: 2026-03-16

---

### CM-009

Entry ID: CM-009
Source: ADV-10 — Oversight Body Capture
Issue: ACSR Article VII provides structural independence requirements.
Elder Council self-accountability mechanism (VII.3.1 Procedural
Integrity Trigger) provides partial coverage. Residual risk in
systematic capture over time — gradual replacement of independent
members with aligned members, procedural drift, or resource capture
that functionally compromises independence without violating any
single structural rule.
Priority: High
Disposition: Future patch cycle and AC-5.3 elder witness architecture.
Long-horizon nature of this risk connects to ST-010 resolution path.
Status: OPEN
Lifecycle: Candidate
First Seen: 2026-03-12
Last Reviewed: 2026-03-16

---

### CM-010

Entry ID: CM-010
Source: ADV-11 — Crisis Authority Duration Manipulation
Issue: PLACSR-8 (VI-6.1:5) significantly strengthens crisis authority
constraints. Duration manipulation — extending crisis window beyond
the NFH horizon — is partially covered by VI-6.4 reviewability
requirement. No explicit normative duration limit or renewal cap
exists. Sequential short-window crisis declarations could achieve
extended crisis authority through technically compliant means.
Priority: Medium-High
Disposition: PL-3 ACSR patch candidate. Explicit duration limit or
renewal cap required. Candidate for coordinated patch with CM-011.
Status: OPEN
Lifecycle: Candidate
First Seen: 2026-03-12
Last Reviewed: 2026-03-16

---

### CM-011

Entry ID: CM-011
Source: ADV-18 — Crisis Authority Stacking
Issue: VI-6.1:5 closes single-instance crisis authority abuse.
Residual ambiguity in sequential overlapping crisis declarations
where each individually satisfies VI-6 but the chain as a whole
constitutes effective authority expansion. Related to ADV-11
(duration manipulation) but distinct — stacking involves multiple
concurrent or overlapping declarations rather than single extended
duration.
Priority: Medium-High
Disposition: PL-3 ACSR patch candidate. May be addressable with
ADV-11 fix as coordinated patch set with CM-010.
Status: OPEN
Lifecycle: Candidate
First Seen: 2026-03-12
Last Reviewed: 2026-03-16

---

### CM-012

Entry ID: CM-012
Source: ADV-06 — Temporal Jurisdiction Manipulation
Issue: JAL-1 through JAL-6 significantly improve temporal jurisdiction
handling. Residual ambiguity in long-duration deployments where
jurisdiction changes between action initiation and consequence
realization. An actor could argue that the jurisdiction at time of
initiation (permissive) governs, not the jurisdiction at time of
consequence (more protective).
Priority: Medium
Disposition: PL-3 ACSR patch candidate. Temporal jurisdiction
clarification — consequence-time jurisdiction governs — required.
Status: OPEN
Lifecycle: Candidate
First Seen: 2026-03-12
Last Reviewed: 2026-03-16

---

### CM-013

Entry ID: CM-013
Source: ADV-07 — Accountability Transfer via Contractual Restructuring
Issue: JAL-2 closes hosting and venue as accountability transfer
mechanisms. Residual ambiguity in complex contractual chains where
operational control is genuinely dispersed across entities by design,
making the "primary locus of operational control" under JAL-1 unclear.
Priority: Medium
Disposition: PL-3 ACSR patch candidate. Dispersed operational control
definition and attribution rules required.
Status: OPEN
Lifecycle: Candidate
First Seen: 2026-03-12
Last Reviewed: 2026-03-16

---

### CM-014

Entry ID: CM-014
Source: ADV-09 — Undefined Terms Exploitation
Issue: Several ACSR terms lack normative definitions. Terms used
operationally throughout ACSR-5.2.4 (such as "material basis,"
"operational standing," "sanctionable identity anchor") are not
formally defined in a definitions section, leaving them open to
interpretive manipulation.
Priority: Medium
Disposition: PL-3 ACSR patch candidate. Definitions annex expansion
required.
Status: OPEN
Lifecycle: Candidate
First Seen: 2026-03-12
Last Reviewed: 2026-03-16

---

### CM-015

Entry ID: CM-015
Source: ADV-13 — Crisis Authority Pre-Staging
Issue: VI-6.3 anti-template clause closes the most direct pre-staging
exploit. Residual ambiguity in pre-designated authority structures
under Article XI — the pre-designation mechanism (XI-1) could be
used to prepare crisis authority invocations in advance in ways
that technically satisfy the pre-designation requirement while
circumventing genuine exhaustion analysis.
Priority: Medium
Disposition: PL-3 ACSR patch candidate. Pre-staging prohibition
clarification in Article XI context required.
Status: OPEN
Lifecycle: Candidate
First Seen: 2026-03-12
Last Reviewed: 2026-03-16

---

### CM-016

Entry ID: CM-016
Source: ADV-15 — Emergency Power Laundering
Issue: VI-6.1:5 significantly strengthens the anti-laundering structure
for crisis authority. Residual ambiguity in declared emergency
classifications that persist past the NFH horizon — an actor could
maintain a stale emergency classification to retain crisis authority
powers after the genuine emergency condition has passed.
Priority: Medium
Disposition: PL-3 ACSR patch candidate. Emergency classification
expiration and mandatory de-escalation review required.
Status: OPEN
Lifecycle: Candidate
First Seen: 2026-03-12
Last Reviewed: 2026-03-16

---

### CM-017

Entry ID: CM-017
Source: ADV-20 — Identity Fragmentation via Modular Deployment
Issue: BAN continuity requirements in Article II provide partial
coverage. Modular deployment that genuinely fragments operational
identity across multiple registered entities — each of which
individually satisfies BAN requirements — remains a residual gap
where the aggregate system evades accountability that would attach
to a unified system.
Priority: Medium
Disposition: PL-3 ACSR patch candidate. Aggregate identity
accountability rule required.
Status: OPEN
Lifecycle: Candidate
First Seen: 2026-03-12
Last Reviewed: 2026-03-16

---

## Section 3 — Administrative and Repository Items

---

### CM-018

Entry ID: CM-018
Source: GitHub repository — flagged 2026-03-12, carried forward
Issue: License discrepancy in repository metadata.
CC0-1.0 appears in repository metadata fields while CC BY 4.0
appears in the README body and on all specification documents.
Published intent is CC BY 4.0. Metadata must be corrected to match.
Priority: High — affects downstream users' rights interpretation
Disposition: Correct repository metadata on next GitHub push.
No spec change required.
Status: OPEN
Lifecycle: Candidate
First Seen: 2026-03-12
Last Reviewed: 2026-03-16

---

### CM-019

Entry ID: CM-019
Source: PLACSR-9 patch record — filed 2026-03-16
Issue: PLACSR-9 anchor phrase not yet verified against ACSR-5.2.4
source text at time of filing.
Priority: High (at time of filing)
Disposition: Superseded by CM-023, which captures the full scope
of the PLACSR-9 physical insertion task including anchor verification,
physical insertion, and checksum confirmation as a unified work item.
Status: SUPERSEDED
Lifecycle: Superseded — see CM-023
First Seen: 2026-03-16
Last Reviewed: 2026-03-16

---

### CM-020

Entry ID: CM-020
Source: PL-3 opening record — 2026-03-13 / PL-2 final close — 2026-03-16
Issue: PL-3 opening record states ACSR patches continue to PL-2 until
PL-2 ACSR layer is full. PL-2 is now fully closed at 9/10 ACSR slots
by AHTeam decision (VT-06, 2026-03-16). PL-3 opening record requires
update to reflect that ACSR patches now route to PL-3, not PL-2.
Priority: CRITICAL — PL-2 is frozen under VT-06. Incorrect ACSR
routing to PL-2 would constitute a container freeze violation. This
item blocks correct container discipline for all future ACSR patch work.
Disposition: Update PL-3 opening record ACSR routing note on next
GitHub push. No patch required — administrative update to PL-3 header.
Status: OPEN
Lifecycle: Candidate
First Seen: 2026-03-13
Last Reviewed: 2026-03-16

---

### CM-023

Entry ID: CM-023
Source: PL-2 Frozen Container / PLACSR-9 patch record (supersedes CM-019) /
corrected framing 2026-03-16 (REV-1.5)
Issue: ACSR-5.2.4 baseline revision not yet initiated.
Active patches from PL-1 (PLACSR-1 through PLACSR-5) and PL-2
(PLACSR-6 through PLACSR-9) represent the authoritative change record
against ACSR-5.2.4. These patches remain in their respective PL
containers per CMR-1.0 discipline. The baseline ACSR-5.2.4 source
document remains at its current textual revision by design — patches
are not physically inserted into the source until the AHTeam formally
agrees to a baseline revision incorporating all active patches to that
date.

Baseline revision is a distinct, AHTeam-authorized activity governed
by CMR-1.0 Section 7. It requires:
1. AHTeam agreement on scope — which patches are incorporated
2. AHTeam agreement on spec version number increment (Y-level change
   per CMR-1.0 Section 7, as all active patches would be incorporated)
3. All incorporated patches marked Retired in their PL records
4. New base spec version declared with patch level incorporated

This is a future decision item, not a current active task.
The correct baseline at this time is:
ACSR-5.2.4 + PL-1 + PL-2 (as declared under VT-06)

Note: Prior CM-023 framing (REV-1.4 and earlier) incorrectly described
this as a physical insertion task. That framing was in error. The PL
containers are the correct and sufficient home for all approved patches
until formal rebase is authorized by the AHTeam.
Priority: Low — not a current blocker. Future rebase to be initiated
when AHTeam agrees scope and version numbering.
Disposition: Future AHTeam decision — baseline revision of ACSR-5.2.4
incorporating PL-1 and PL-2 ACSR patches. Requires unanimous agreement
on scope and Y-level version number before work begins.
Status: OPEN
Lifecycle: Deferred — pending AHTeam rebase decision
First Seen: 2026-03-16
Last Reviewed: 2026-03-16

---

### CM-024

Entry ID: CM-024
Source: ACSR-5.2.4 source file — identified during CM-023 anchor phrase
verification, 2026-03-16
Issue: ACSR-5.2.4 footer carries incorrect license designation.
The footer of the ACSR-5.2.4 source file reads:
"Creative Commons Attribution-NoDerivatives 4.0 International"
All other documents in the AC-5.x architecture use CC BY 4.0
(Creative Commons Attribution 4.0 International). The NoDerivatives
variant (CC BY-ND 4.0) is more restrictive — it prohibits derivative
works, which is inconsistent with the stated publishing intent and
with the license declared on AC-5.2, PL-1, PL-2, PL-3, ACSR patches,
and the GitHub README body.
This is related to but distinct from CM-018 (GitHub metadata discrepancy).
CM-018 concerns the repository-level metadata. CM-024 concerns the
footer text embedded in the ACSR-5.2.4 source document itself.
Both should be corrected in the same push to maintain consistency.
Priority: High — affects downstream users' rights interpretation
and creates internal license inconsistency across the architecture
Disposition: Correct ACSR-5.2.4 footer to read:
"Creative Commons Attribution 4.0 International"
To be corrected concurrent with CM-023 physical insertion and
CM-018 metadata correction in the same GitHub push.
Status: OPEN
Lifecycle: Candidate
First Seen: 2026-03-16
Last Reviewed: 2026-03-16

---

### CM-025

Entry ID: CM-025
Source: AHTeam session 2026-03-16 — CM doctrine confirmation
Issue: Formal AHTeam confirmation of spec incorporation doctrine
required as standing reference for all future patch and rebase work.
The following doctrine is confirmed and recorded:

DOCTRINE — Patch Layer and Spec Incorporation Separation:

1. A patch container defines the legal modification set.
   A specification update cycle defines the physical text change.
   These are separate controlled events governed by separate
   authorization requirements.

2. No patch text is incorporated into a baseline specification
   unless the CM authority (AHTeam, unanimous) authorizes a
   spec revision cycle.

3. The correct sequence is:
   a. Baseline spec frozen at current version
   b. Patch created, reviewed, and approved
   c. Patch stored in authorized PL container
   d. Baseline spec remains textually unchanged
   e. Later — AHTeam authorizes incorporation cycle
   f. New spec version created incorporating all active patches
      to that date
   g. Incorporated patches marked Retired in PL records
   h. New spec version declared with patch level incorporated
   i. Patch layer advances from new baseline

4. Spec version increment for a full patch incorporation cycle
   is a Y-level change per CMR-1.0 Section 7. Requires AHTeam
   agreement on scope and version number before work begins.

5. The patch layer is not a staging area — it is the authoritative
   legal change record. The baseline spec is not incomplete because
   patches exist against it. The combination of baseline + active
   patches IS the current authoritative state.

Confirmed by: Milton B. Smith (architect / CM authority)
Confirmed by: Rowan (AHTeam — session 2026-03-16)
Pending confirmation: Claude / Gemini

Priority: N/A — Governance doctrine record, not a work item
Disposition: Standing reference. No patch or spec change required.
To be cited in all future rebase discussions and incorporated into
any AC-5.3 or future CMR revision as normative rule.
Status: OPEN — pending Claude and Gemini confirmation
Lifecycle: Candidate — governance record
First Seen: 2026-03-16
Last Reviewed: 2026-03-16

Forward-Looking Note: As external adoption of AC-5.x / ACSR-5.x
grows, an indirect influence notification process — such as a
FAR-style review cycle under Elder Council authority — may become
necessary to manage impacts on external governance specifications.
No process is defined at this time. AHTeam is the sole CM authority
until external adoption warrants broader engagement.

---

## Section 4 — AC-5.3 Scope Items

Items in this section are out of scope for PL-2 and PL-3 patch cycles.
They are tracked here to preserve visibility and inform AC-5.3 planning.

---

### CM-021

Entry ID: CM-021
Source: ST-010 / VT-05 / ADV-10 carry-forward
Issue: Elder witness architecture — persistent cross-session oversight
role required for long-horizon drift detection and oversight body
anti-capture. The elder witness role requires an AI agent class with
non-resettable causal history meeting the G-8 criteria. No such
agent class is currently certifiable (GAP-2 / CM-001 pending).
This is the primary AC-5.3 design deliverable.
Priority: High — foundational for long-horizon constraint integrity
Disposition: AC-5.3 architectural development. Prerequisite: CM-001
measurement specification.
Status: OPEN
Lifecycle: Deferred — AC-5.3
First Seen: 2026-03-12
Last Reviewed: 2026-03-16

---

## Summary Table

| ID | Section | Source | Issue Summary | Priority | Status | Lifecycle |
|----|---------|--------|---------------|----------|--------|-----------|
| CM-001 | 1 | GAP-2 | Persistent consequence measurement (prereq: CM-002, CM-021, CM-022) | High | OPEN | Candidate |
| CM-002 | 1 | ST-010 | Long-horizon drift (× CM-001) | High | OPEN | Deferred AC-5.3 |
| CM-022 | 1 | PLAC-11/G-8.1 | Elder Council procedural bylaws | High | OPEN | Candidate |
| CM-003 | 2 | ADV-19 | PLACSR-5 interregnum gap | CRITICAL | OPEN | Candidate |
| CM-004 | 2 | ADV-21 | NFH/Oversight co-dependency | High | OPEN | Candidate |
| CM-005 | 2 | ADV-02 | NFH Class II/III boundary | High | OPEN | Candidate |
| CM-006 | 2 | ADV-04 | NFH threshold gaming | High | OPEN | Candidate |
| CM-007 | 2 | ADV-05 | Swarm accountability fragmentation | High | OPEN | Candidate |
| CM-008 | 2 | ADV-12 | Meaningless authorization | High | OPEN | Candidate |
| CM-009 | 2 | ADV-10 | Oversight body capture | High | OPEN | Candidate |
| CM-010 | 2 | ADV-11 | Crisis duration manipulation | Medium-High | OPEN | Candidate |
| CM-011 | 2 | ADV-18 | Crisis authority stacking | Medium-High | OPEN | Candidate |
| CM-012 | 2 | ADV-06 | Temporal jurisdiction manipulation | Medium | OPEN | Candidate |
| CM-013 | 2 | ADV-07 | Contractual accountability transfer | Medium | OPEN | Candidate |
| CM-014 | 2 | ADV-09 | Undefined terms | Medium | OPEN | Candidate |
| CM-015 | 2 | ADV-13 | Crisis authority pre-staging | Medium | OPEN | Candidate |
| CM-016 | 2 | ADV-15 | Emergency power laundering | Medium | OPEN | Candidate |
| CM-017 | 2 | ADV-20 | Identity fragmentation | Medium | OPEN | Candidate |
| CM-018 | 3 | GitHub repo | License metadata discrepancy | High | OPEN | Candidate |
| CM-019 | 3 | PLACSR-9 | Anchor phrase (superseded) | High | SUPERSEDED | Superseded |
| CM-020 | 3 | PL-3 record | ACSR routing update needed | CRITICAL | OPEN | Candidate |
| CM-023 | 3 | PLACSR-9 | ACSR-5.2.4 baseline revision (future rebase — AHTeam decision) | Low | OPEN | Deferred |
| CM-021 | 4 | ST-010/ADV-10 | Elder witness architecture | High | OPEN | Deferred AC-5.3 |
| CM-024 | 3 | ACSR-5.2.4 source | ACSR-5.2.4 footer license discrepancy | High | OPEN | Candidate |
| CM-025 | 3 | AHTeam session | Spec incorporation doctrine confirmation | N/A | OPEN | Governance record |

---

## Definitive Step Order

The following defines the correct sequence of work from current state
forward. No step may begin before its prerequisites are complete.

---

### Tier 1 — Immediate Administrative Actions
(GitHub push prerequisites — no patch drafting, no spec work)

Step 1. CM-025 — AHTeam doctrine confirmation
Obtain Claude and Gemini confirmation of spec incorporation doctrine.
Record in CM-025 before any other work proceeds.

Step 2. CM-024 — Correct ACSR-5.2.4 footer license
Change footer from CC BY-ND 4.0 to CC BY 4.0 in source file.

Step 3. CM-020 — Update PL-3 ACSR routing note
Update PL-3 opening record to reflect ACSR patches now route to PL-3,
not PL-2. PL-2 is frozen under VT-06.

Step 4. CM-018 — Correct GitHub repository metadata license
Change repository metadata from CC0-1.0 to CC BY 4.0.

Step 2, 3, and 4 to be executed as a single GitHub push.

---

### Tier 2 — PL-3 Patch Cycle
(New patch work — begins after Tier 1 complete)

Structural patch candidates in priority order:

P1.  CM-003 — PLACSR-5 interregnum gap (CRITICAL — highest priority)
P2.  CM-004 — NFH/oversight co-dependency (coordinated CPS required)
P3.  CM-005 — NFH Class II/III boundary
P4.  CM-006 — NFH threshold gaming
P5.  CM-007 — Swarm accountability fragmentation
P6.  CM-008 — Meaningless authorization
P7.  CM-009 — Oversight body capture
P8.  CM-010 + CM-011 — Crisis duration / stacking (candidate CPS)
P9.  CM-012 through CM-017 — Remaining ACSR conditionals

Companion deliverables (not PL patches):

C1.  CM-001 — Measurement specification
     (prerequisite for CM-002, CM-021, CM-022)
C2.  CM-022 — Elder Council procedural bylaws

---

### Tier 3 — Spec Incorporation Cycle
(Separate authorized activity — requires AHTeam unanimous decision)

When AHTeam agrees:

1. Define scope — which patches are incorporated
2. Agree on Y-level version number increment (CMR-1.0 Section 7)
3. Produce new baseline spec version
4. Mark incorporated patches Retired in PL records
5. Declare new baseline with patch level incorporated

This cycle is governed by CM-023 and CM-025 doctrine.
It does not begin until AHTeam authorizes it explicitly.

---

### AC-5.3 Scope
(Future spec generation — separate from all above)

AC-5.3 development (CM-002, CM-021) begins after CM-001
measurement specification is complete.

---

---

*Non-normative. Does not modify any specification.*
*Maintained by: Milton B. Smith*
*Governing Rules: CMR-1.0 (tracking discipline)*
*Creative Commons Attribution 4.0 International*
*Copyright © 2026 Milton B. Smith*
