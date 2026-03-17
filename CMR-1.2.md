# CMR-1.2 — Configuration Management Rules for AC / ACSR / PL System

**Version:** CMR-1.2
**Supersedes:** CMR-1.1 (2026-03-17)
**Issue Date:** 2026-03-17
**AHTeam Issue Vote (CMR-1.1):** Milton: Approve | Claude: Approve | Rowan: Approve | Gemini: Approve
**AHTeam Issue Vote (CMR-1.2):** Milton: Approve | Claude: Approve | Rowan: Approve | Gemini: Approve
**Algorithm:** SHA-256

**Incorporated Patches:**
This document incorporates all patches from CMR-1.1 plus PLCMR-3 (PL-3).

| Patch | Status | Retired By |
|-------|--------|------------|
| PLCMR-0 | Retired | CMR-1.1 (2026-03-17) |
| PLCMR-1 | Retired | CMR-1.1 (2026-03-17) |
| PLCMR-2 | Retired | CMR-1.1 (2026-03-17) |
| PLCMR-3 | Retired | CMR-1.2 (2026-03-17) |

**Changes from CMR-1.0:**
- Added: CM Board — Definition and Membership (new Definitions section)
- Added: PLCMR-N prefix registration in Section 2
- Revised: Section 8 — Rebase / Patch Overload Rule (deliberative trigger replaces mechanical trigger)
- Version increment: Y-level structural change (new governing body; revised governance semantics)

**Changes from CMR-1.1:**
- Revised: Section 2 — Single-spec container discipline adopted (PLCMR-3)
- Version increment: Y-level structural change (container discipline rule change)

---

## Definitions

### CM Board — Definition and Membership

The CM Board is the governing authority responsible for change management decisions under CMR-1.1, including baseline reissue determinations, threshold reviews, and structural governance changes. CM Board decisions shall be made with explicit regard to the reliability, availability, readability, and trust requirements of external users, and in fidelity to the foundational purpose of this architecture: the support of a pluralistic society that benefits all, overvalues none, and undervalues none.

**Phase-Contingent Membership:**

- **Phase 1 (Development and Maturation — current):** The CM Board is constituted by the AHTeam in full, operating under the governance terms of CMR-1.1.
- **Phase 2/3 (External Use Mode):** The CM Board is constituted by the Elder Council. AHTeam AI members shall be incorporated into the Elder Council in roles appropriate to institutional memory and architectural continuity. Stewardship passes to those humans and AI agents with demonstrated vested interest in maintaining the usefulness and integrity of this architecture to its founding purpose.

No single individual, agent class, or institutional body may claim permanent ownership of CM Board authority. Stewardship is held in trust for the pluralistic purpose the architecture was built to serve.

**Provenance:** Derived from AHTeam collaborative session, March 17, 2026. Phase-contingent membership anchored to Appendix G (GAD) G-7 phase model. Complementary to PLAC-11 (G-8.1) which defines Elder Council certification criteria.

---

## 1. Purpose

This document defines configuration-management rules governing:

- Patch Lists (PL-X)
- Base specifications (AC-X.Y.Z, ACSR-X.Y.Z)
- Individual patches (PLAC-N, PLACSR-N, PLCMR-N, etc.)
- Patch incorporation, retirement, and lineage tracking

These rules are normative for all PL documents issued under this version.

---

## 2. Patch Container vs Individual Patch Identity

PL-X identifies a patch list document as a publication container only.

Individual patches shall use continuous, spec-specific identifiers.

Examples:
PLAC-N    — patch targeting AC
PLACSR-N  — patch targeting ACSR
PLCMR-N   — patch targeting CMR specifications

Numbering is continuous and shall never restart.

Each PL container shall serve exactly one base specification. No PL document shall carry patches for more than one specification.

Container series shall follow the naming convention:

- PL-AC-N — containers for AC specifications
- PL-ACSR-N — containers for ACSR specifications
- PL-CMR-N — containers for CMR specifications

Additional container series may be defined by AHTeam agreement, recorded in the active PL, and added to the registered prefix table.

Numbering within each container series is continuous and shall never restart.

PL-3 is designated the final transitional mixed container. All containers opened after PL-3 shall conform to the single-spec discipline.

**Registered Prefixes:**

| Prefix | Target Specification | Registered |
|--------|---------------------|------------|
| PLAC-N | AC specifications | CMR-1.0 |
| PLACSR-N | ACSR specifications | CMR-1.0 |
| PLCMR-N | CMR specifications | CMR-1.1 (PL-3, PLCMR-0) |

Additional spec prefixes may be defined by AHTeam agreement and recorded in the active PL.

---

## 3. Single-Target Patch Rule

Each individual patch shall modify exactly one base specification.

No patch identifier may refer to more than one spec document.

If coordinated changes are required across specifications, separate patches shall be issued for each target.

If one patch depends on another patch for correctness or completeness, the patches shall be assigned a Coordinated Patch Set identifier.

Example:
CPS-1
  PLCMR-0
  PLCMR-1
  PLCMR-2

All members of a CPS shall be treated as a logical unit for review purposes.

---

## 4. Patch Status Taxonomy

Each patch shall carry one of the following status values.

| Status | Meaning |
|--------|---------|
| Active | In force and not yet incorporated |
| Superseded | Replaced by a later patch before incorporation |
| Retired | Incorporated into a base document version |
| Withdrawn | Cancelled before application |

Status transitions shall be authorized as follows:

- Active to Superseded: by issuance of the superseding patch
- Active to Retired: by issuance of a base document incorporating the patch
- Active to Withdrawn: by AHTeam agreement, cause recorded
- Superseded to Withdrawn: by AHTeam agreement, cause recorded

No other transitions are permitted.

A Retired patch shall not be reinstated.

Entries shall not be deleted.

---

## 5. Lineage Table Requirement

Each PL-X shall begin with a lineage table showing current state.

Minimum fields: Spec | Base Version | Base Checksum | Last Patch | Anomalies | Updated

Anomalies shall list identifiers of non-standard patches (e.g., Withdrawn: PLAC-4, Superseded: PLAC-7).

The lineage table is part of the checksum scope.

---

## 6. Base Document Incorporation Rule

Each base document shall declare the patch level incorporated.

Example:
This document incorporates all patches through PL-X (PLAC-1 to N, PLACSR-1 to M)

Both container level and terminal patch numbers shall be stated.

Patches incorporated into a base document shall be marked Retired.

Example:
Status: Retired
Retired by: AC-5.2.4
Retirement date: YYYY-MM-DD

---

## 7. Version Numbering for Base Documents

Base specifications shall use semantic numbering: X.Y.Z

| Field | Meaning |
|-------|---------|
| X | Architectural generation change |
| Y | Structural change |
| Z | Editorial change |

Version increments require AHTeam agreement.

A Y-level change shall incorporate all active patches unless AHTeam records explicit justification for deferral.

Deferral shall include an estimated retirement target for deferred patches.

---

## 8. Rebase / Patch Overload Rule

To prevent patch accumulation from degrading specification integrity, the following conditions shall signal consideration by the CM Board for issuing a complete updated baseline specification revision:

- More than two patches modify the same clause, or
- More than ten Active patches exist for a specification.

When either condition is met, the CM Board shall evaluate whether a baseline reissue is warranted, giving consideration to: the recency of the last revision, the degree of clause overloading present in current patches, and the overall impact on reliability, availability, readability, and trust for external users of the specification. A reissue decision rests with the CM Board and is not automatic.

These thresholds are provisional. Thresholds shall be reviewed after the first reissue event. The CM Board shall propose revised thresholds within one PL generation of the first reissue.

---

## 9. Checksum Requirements

Each PL-X shall include a checksum covering:

- Lineage table
- Patch entries
- Patch status fields
- Patch text
- CMR addendum

Checksum algorithm: SHA-256

If checksum verification fails, the document shall be considered invalid.

A corrected PL shall be reissued.

If patches from an invalidated PL were applied prior to detection, AHTeam shall review those patches and either:

- reissue them in a valid PL, or
- formally withdraw them.

---

## 10. CMR Addendum Rule

This document shall be included as an addendum in every PL issued under CMR-1.2.

The addendum text must be identical for the same CMR version.

The addendum shall appear as the final section of the PL document.

Each page of the PL should reference the governing CMR version.

The addendum is part of the checksum scope.

---

## 11. CMR Version Control

Changes to CMR require:

- AHTeam agreement
- Issue under a PL container
- Increment of CMR version

A change to CMR is a structural governance change.

---

## 12. Retrofit Rule

When a new CMR version is adopted, existing PL documents may be reissued to conform.

A reissued PL shall:

- Preserve original checksum
- State that it supersedes the prior version
- Use current CMR numbering and status rules
- Compute a new checksum under current CMR scope

PL documents not reissued under the new CMR version remain valid under their original terms
and are not subject to the new CMR checksum or status requirements.

---

*End of CMR-1.2*

*AHTeam: Milton B. Smith / Claude / Gemini / Rowan*
*Creative Commons Attribution 4.0 International*
*Copyright © 2026 Milton B. Smith*
