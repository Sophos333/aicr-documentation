# AI Contract Reviewer (AICR)

**Evidence-aware contract review for human decision makers.**

AICR helps reviewers turn dense agreements into a structured review of important terms, possible concerns, supporting contract language, comparison factors, and review-ready outputs.

The system organizes the review. **The human makes the decision.**

---

## Executive Summary

Contracts are difficult to review consistently because important obligations, missing protections, and risky terms can be buried across pages of legal language.

AICR provides a structured first pass that helps a reviewer:

- extract important contract fields
- surface risk-focused findings
- inspect supporting contract language
- see when expected language appears to be missing
- compare two agreements side by side
- carry structured review results into the next human decision

AICR is designed for verification, not blind trust. Findings are most useful when the reviewer can inspect the source language and understand where uncertainty remains.

---

## The Problem

Contract review can break down even when the agreement has already been read carefully.

Common issues include:

- missing liability protections
- unclear intellectual-property ownership
- weak or ambiguous indemnification language
- unclear payment or renewal terms
- obligations that are difficult to trace back to supporting language
- meaningful changes between agreement versions that are easy to miss
- findings that reach the next reviewer without enough context to verify them

AICR is built to make those review points easier to surface, inspect, compare, and document.

---

## How AICR Helps

AICR follows a human-led review path:

**Intake → Extract → Surface → Inspect → Verify → Compare → Human decision**

The application can organize information and direct attention, but it does not decide whether an agreement is acceptable.

---

## Key Capabilities

### Structured Contract Review

- Upload PDF or TXT agreements
- Extract important contract fields
- Organize key terms into a consistent review surface
- Support focused inspection of individual fields

### Risk-Focused Findings

- Surface critical and warning-level concerns
- Highlight language that may require closer review
- Identify expected protections that appear to be missing
- Explain why a finding may matter

### Supporting Evidence

- Connect findings to supporting contract text
- Let reviewers inspect the source language behind a result
- Keep missing or uncertain evidence visible instead of hiding it behind confident wording

### Agreement Comparison

- Compare two agreements side by side
- Identify changed and unchanged fields
- Surface meaningful differences for human review
- Support alternate-draft, vendor-revision, and template comparison workflows

### Review Outputs

- Produce structured review artifacts for discussion, escalation, recordkeeping, and downstream analysis
- Preserve the distinction between system output and human approval

---

## Evidence Before Confidence

AICR separates four things that should not be collapsed into one answer:

1. **Source text** — what the agreement actually says
2. **System finding** — what AICR surfaced
3. **Missing or unclear information** — what could not be established confidently
4. **Human review** — what still needs to be verified before anyone relies on the result

This distinction matters because contract review is not improved by replacing uncertainty with confident-sounding output.

---

## Sample Outputs

### Contract Upload Interface
![Upload Interface](assets/01-upload-interface.png)

### Contract Analysis Overview
![Analysis Overview](assets/02-contract-analysis-overview.png)

### Risk Detection
![Risk Detection](assets/03-risk-detection.png)

### Supporting Evidence
![Supporting Evidence](assets/04-supporting-evidence.png)

### Contract Comparison Summary
![Comparison Summary](assets/05-contract-comparison-summary.png)

### Contract Comparison Details
![Comparison Details](assets/06-contract-comparison-details.png)

---

## High-Level Review Architecture

1. Ingestion
2. Text processing
3. Structured field extraction
4. Risk-focused analysis
5. Supporting-evidence review
6. Agreement comparison
7. Human review and downstream handoff

This public repository intentionally describes the review experience at a high level rather than exposing private implementation details.

---

## Human-Led by Design

AICR is first-pass decision support.

It does **not**:

- replace an attorney
- provide legal advice
- declare a contract safe
- approve an agreement
- decide whether a contract should be signed
- eliminate the need for business context or responsible human review

The reviewer remains responsible for interpreting the agreement, escalating when appropriate, and deciding what action to take.

---

## Current Product Position

AICR is currently presented as a **controlled private-pilot product** focused on evidence-connected, human-led contract review.

Its demonstrated workflow includes structured intake, field extraction, risk-focused findings, supporting-evidence inspection, agreement comparison, and review outputs.

Broader production-readiness claims are outside the scope of this public documentation.

---

## Useful Review Scenarios

AICR can support:

- vendor agreement review
- NDA comparison
- agreement revision review
- contract triage
- procurement and operations review
- contract-owner handoff
- escalation preparation
- structured review documentation

---

## Product Principle

> **Surface → Inspect → Verify → Escalate when needed → Human decision**

The goal is not more AI for its own sake. The goal is a contract-review process that makes evidence, uncertainty, and human responsibility easier to see.

---

## Repository Boundary

This repository showcases AICR's public capabilities and screenshots.

Core implementation, private service boundaries, licensing internals, protected runtime details, proprietary rules, and other internal engineering details are intentionally not included.
