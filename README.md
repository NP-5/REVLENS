# REVLENS

### Manager-Focused Conversation Intelligence & Routing

REVLENS transforms sales calls and meetings into structured, evidence-backed workflows for managers. It reduces the effort required to review large amounts of conversation data by identifying useful signals and routing conversations into actionable categories.

---

## Overview

REVLENS follows a simple workflow:

**Calls & Meetings → Normalize → Validate → Analyze → Route → Manager Action**

Instead of treating every conversation the same, REVLENS identifies the type of managerial attention a conversation may require.

### Routing Categories

* **Sales Coaching** — objections, competitor mentions, budget concerns, and coaching opportunities.
* **Deal Next Steps** — buyer commitments, follow-ups, meetings, or purchasing-process signals.
* **Customer Follow-up** — customer issues, delays, dissatisfaction, or operational concerns.
* **Internal / Vendor Note** — vendor, partner, referral, or internal coordination topics.
* **Needs Review** — insufficient evidence, missing transcript content, or cases requiring human judgment.

A conversation can receive multiple routes when multiple signals are supported by the available evidence.

---

## Key Features

* Conversation and meeting data ingestion
* Data normalization and validation
* Duplicate and revision handling
* Evidence-based conversation routing
* Manager-focused dashboard
* Route and person-based organization
* Conversation detail and evidence views
* Manual route correction
* Audit-friendly routing history
* Structured exports
* Manifest-based source of truth
* Needs-review workflow
* Manager briefing and summary outputs

---

## Evidence-Based Routing

REVLENS is designed around the principle:

> **Evidence over assumption.**

The system uses available conversation text and defined analytical signals to determine routing.

Example:

```text
Buyer discusses scheduling the next meeting
            |
            v
Buyer next-step signal detected
            |
            v
Deal Next Steps
```

If there is not enough evidence to make a reliable routing decision, REVLENS can send the record to **Needs Review** instead of making an unsupported conclusion.

---

## Manager Workflow

REVLENS is designed around four simple actions:

**Scan → Filter → Inspect → Act**

Managers can:

1. Review key metrics.
2. Filter conversations by type, person, or route.
3. Open individual conversations.
4. Review the evidence behind routing.
5. Correct routes when necessary.
6. Export structured results.

---

## Output Structure

REVLENS organizes generated outputs into structured folders:

```text
exports/
└── <run>/
    ├── by_route/
    ├── by_person/
    ├── manager_brief/
    ├── manifest.json
    └── manifest.csv
```

The manifest acts as the source of truth for exported records.

Route-based organization supports manager workflows, while person-based organization improves findability.

---

## Data Quality and Auditability

REVLENS does not assume that every source field represents confirmed truth.

For example:

* Missing transcripts are not treated as evidence.
* Meeting organizers are not automatically assumed to be attendees.
* An organizer is not automatically assumed to be the selling representative.
* Source-reported connection status is not treated as transcript verification.
* Unsupported conclusions are routed for human review.

Revision handling ensures that newer versions of records can supersede stale versions without silently losing the underlying history.

---

## Human-in-the-Loop

REVLENS is designed to support managers rather than replace managerial judgment.

Managers can manually correct routing when necessary while preserving the automated routing history.

The workflow is:

**Automation provides scale → Evidence provides transparency → Managers provide judgment**

---

## AI Usage

AI tools may be used during development for coding assistance, documentation, analysis, debugging, and presentation preparation.

The implemented REVLENS routing logic is primarily based on defined, inspectable rules and evidence signals rather than presenting an opaque AI prediction as fact.

This approach prioritizes explainability and auditability.

---

## Known Limitations

* Rule-based detection may miss nuanced language.
* Missing transcripts limit analytical conclusions.
* Meeting organizer data does not prove attendance or selling role.
* Source-reported connection status does not independently verify a conversation.
* The supplied dataset may not represent complete real-world team activity.
* Routing indicates evidence-supported workflow categories, not guaranteed deal outcomes.
* Conversations without matching signals may require manual review.

---

## Future Improvements

Potential future improvements include:

* Semantic conversation understanding
* Improved speaker and participant identification
* Transparent confidence scoring
* Better detection of contradictory signals
* Manager feedback loops
* Historical trend analysis
* Larger evaluation datasets
* Precision and recall measurement for routing
* More advanced analytics while preserving auditability

---

## Project Goal

The goal of REVLENS is not to replace managerial decision-making.

It is to reduce the amount of time managers spend searching through conversations and help them focus attention where it matters.

**REVLENS turns conversation data into evidence-backed managerial workflows.**

---

## Technology

The project is built using the technologies and implementation included in this repository.

Refer to the project files and configuration for the exact runtime, dependencies, and setup instructions.

---

## Project Status

REVLENS is a project implementation focused on demonstrating conversation analysis, evidence-based routing, manager workflows, data quality, and explainable decision support.

Future iterations can extend the analytical capabilities while maintaining the core principles of evidence, auditability, and human control.
