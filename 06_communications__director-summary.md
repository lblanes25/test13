# Archer → Optro Workflow Design: Approach Summary

## What I've set up

I've built a structured workspace for our team's workflow design work on the Archer→Optro migration. The framework is not creating documentation from scratch — most of this content already exists across emails, meetings, the procedures manual, our project Airtable, and team members' notes. What this framework does is **organize, standardize, and make that work reviewable and reusable** so we can defend it across stakeholders, hand off cleanly to other teams, and prove what was decided when.

## How the tools fit together

> **Airtable → status, decisions, ownership**
> **SharePoint → final signed-off artifacts**
> **Everything else → disposable**

Airtable is the system of record for tracking. SharePoint is the system of record for final approved artifacts and approval evidence. The drafting workspace where we consolidate scattered content into reviewable form is non-authoritative — what matters is what gets promoted to SharePoint and tracked in Airtable. Every Airtable row links directly to its SharePoint counterpart, so status-to-artifact is one click.

## How the work is structured

**Per workflow** (engagement lifecycle, issues, audit entities, workpaper review):
- A written narrative and visual diagram of the target-state design
- Side-by-side comparison of current Archer to target Optro
- Gap analysis where Optro can't or shouldn't replicate Archer
- RACI matrix making approvals explicit
- UAT scenarios for validation

**Across the project:**
- Decisions log capturing open questions, confirmations, and who confirmed what
- Sign-off log built to a defensibility standard (specific version, named approver, archived evidence)
- Design rationale capturing *why* major choices were made and what alternatives were considered
- Change log tracking material updates and re-approvals

**For other teams:**
- Handoff lists for methodology updates, reporting needs, training implications, integration touchpoints, and data quality issues — surfaced as we encounter them, not at the end

## What this protects us from

- **Methodology gaps post-go-live.** Anything our design implies for the procedures manual is logged for the methodology team as we go, so nothing reaches them by surprise.
- **Approval ambiguity.** Sign-offs are tied to specific artifact versions with archived email evidence. We can show exactly who approved what and when.
- **Decision drift.** Every material design choice has a recorded rationale, including what we considered and rejected. If a decision is questioned later, the answer isn't in someone's memory.
- **Variant blindness.** For workflows like fieldwork that have many variants (different workpaper types), I'm using a structured approach that catalogs variants explicitly and validates them against procedures, recent practice, and role-based review — so we don't approve a fieldwork design that misses, say, IT-specific workpapers.

## Scope clarity

Our team is responsible for **workflow design** — how auditors and their roles interact with Optro. We are not responsible for:
- Data migration or platform-level role provisioning (PM owns)
- Procedures manual / methodology updates (methodology team owns)
- Reporting, dashboards, and KPI design (data migration team, to confirm)
- System integrations (IT integration workstream)
- Training delivery (owner currently unconfirmed — flagging as a project risk)

We *do* surface implications for each of these teams as we encounter them.

## Operating model

- **Recommend-only posture** — we propose; stakeholders approve. We don't decide unilaterally.
- **Multi-reviewer sign-off** — methodology, data & analytics, and reporting review every workflow at minimum, plus domain-specific reviewers (PGAs, audit leaders) per workflow.
- **Disagreements escalated, not arbitrated.** When reviewers conflict, we document both views neutrally and escalate to the project sponsor.
- **SharePoint is canonical.** My working space is for organization; SharePoint holds the authoritative versions, and that's where sign-offs live.

## Where things stand

Engagement lifecycle workflow is in active design. Several open items are tracked, with the highest-priority being:
1. Locating the existing approval matrix (will populate the RACI)
2. Confirming the Reporting phase sequence
3. Defining the Fieldwork exit checklist
4. Identifying the project sponsor and post-go-live change-control committee
5. Confirming training ownership

## What I'd find helpful from you

- Confirmation of our team's decision authority (recommend-only is my working assumption)
- Help identifying the project sponsor / escalation owner
- Direction on training ownership
- Awareness that the documentation framework exists and can be referenced if anyone questions our approach
