# Archer → Optro Workflow Design

Project workspace for designing target-state audit workflows in Optro (fka Auditboard), migrating from Archer.

## How the tools fit together

> **Airtable → status, decisions, ownership**
> **SharePoint → final signed-off artifacts**
> **Everything else → disposable**

- **Airtable** is the system of record for tracking — deliverable status, decisions, sign-offs, ownership, working group items, beta feedback, methodology impacts, cross-team handoffs.
- **SharePoint** is the system of record for final, approved artifacts and approval evidence.
- **This ChatGPT project** is a drafting and working space — non-authoritative, recreatable. Content here is consolidated into a reviewable form, then promoted to SharePoint as final and tracked in Airtable as a deliverable.
- **One-click rule:** every Airtable row links to its SharePoint counterpart. Status → artifact in one click.

This framework is not creating documentation from scratch. Most of the content already exists across emails, meetings, the procedures manual, the project Airtable, and team members' notes. The framework's job is to organize, standardize, and make that work reviewable and reusable.

## Project scope

**In scope:** Workflow design for audit entities, engagements/workpapers, issues/findings. Approval logic within workflows.

**Out of scope:** Data migration (PM owns), role/permission provisioning, methodology updates, reporting/dashboard design, integrations, training delivery.

**Cross-team flagging:** In scope — we surface implications for methodology, reporting, training, and integrations to the right owners. Data observations from workflow design land directly in field-level crosswalks rather than a separate handoff file.

## Workflows

Detailed deliverable status (per-artifact state, leads, blockers, next actions) is tracked in our team's tab in the project Airtable. The table below is a brief overview only.

| Workflow | Lead | Status | Location | Last updated |
|---|---|---|---|---|
| Engagement / audit lifecycle | *(TBD)* | Design in progress | `/workflows/engagement-lifecycle/` | Session 1 |
| Issues / findings lifecycle | *(TBD)* | Not started | — | — |
| Audit entities (risk/control library) | *(TBD)* | Not started | — | — |
| Workpaper review & approval | *(TBD)* | Not started | — | — |

**Status values:** Not started · Design in progress · Design signed off · Being configured in Optro · UAT in progress · Ready for go-live

## Project-level artifacts

| File | Purpose |
|---|---|
| `CLAUDE.md` | Agent definition, scope, working principles, deliverable model. |
| `decisions-log.md` | Open questions, confirmations, resolved decisions. |
| `methodology-impacts.md` | Handoff list for the methodology team. |
| `extraction-prompts.md` | Prompts for sanitized extracts from the procedures manual via ChatGPT. |
| `/handoffs/reporting-needs.md` | Reporting/dashboard needs — for reporting team (likely data migration team; to confirm). |
| `/handoffs/training-implications.md` | Training/change-management implications — owner TBD. |
| `/handoffs/integration-touchpoints.md` | System integration needs — for IT integration workstream. |

## Quick status

**Confirmed so far (Session 1):**
- Engagement lifecycle phases: Kickoff+Planning (blended) → Fieldwork → Reporting → Closeout
- Roles: Auditor, Team Leader (Dir), Audit Leader (VP), PGA (SVP, ~30 across org), CAE, plus auditee mgmt, process owners, integrated teams
- Workpaper review rule: one level above the last person who worked or approved (relative, not fixed-role)
- Closeout triggers audit entity update (cross-workflow dependency)
- Sign-off model: multi-party by lens (methodology + data + reporting minimum) plus domain stakeholders
- Sign-off mechanics: email, with defensibility criteria

**Top open items to unblock progress:**
1. Locate the existing approval matrix — will populate RACI.
2. Confirm Reporting phase sequence.
3. Define Fieldwork exit checklist contents.
4. Identify the project sponsor / escalation owner and change-control committee.
5. Confirm training ownership.
6. Assign workflow leads across the three-person team.
7. Confirm with PM that legacy data access, concurrent engagements during cutover, and audit trail/immutability requirements are owned somewhere.

See `decisions-log.md` for the full list of 22 tracked items.
