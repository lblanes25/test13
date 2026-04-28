# Proposal: Project Tracking Suite in Airtable

**For:** Team review (director + peer)
**Purpose:** Stand up a connected suite of tables in our project Airtable to track structured project data — deliverable status, decisions, sign-offs, working group input, beta feedback, and cross-team handoffs — for the Optro migration.

---

## Why we need this

We're producing a defined set of artifacts per workflow across four workflows, with multi-stakeholder reviews, beta team feedback in real time, and a working group providing input. With three of us working in parallel, we need consolidated visibility into:

- What's the status of every deliverable?
- What decisions are open vs. resolved, and who owns each?
- Who has signed off on what, when, and against which version?
- What's the working group reviewing next?
- What feedback have we received from the beta team and what's been done with it?
- What have we surfaced to other teams (methodology, data migration, IT, training)?

We have markdown documentation of the *narrative content* (workflow narratives, gap analyses, design rationale) that lives in a working ChatGPT project. But the *tracking data* — structured, frequently updated, multi-row — fits Airtable far better than markdown files. This proposal captures everything tracking-related in Airtable, where it can be filtered, grouped, and shared cleanly.

## The split — what lives where

| Lives in Airtable (structured tracking, frequent updates) | Lives in markdown (narrative, periodic updates) |
|---|---|
| Deliverable status across all workflows | Workflow narratives |
| Decisions log | Gap analyses |
| Sign-off log | Design rationale documents |
| Working group log (agenda + meetings) | Mermaid diagrams |
| Beta feedback log | Archer-vs-Optro comparisons |
| Methodology impacts | UAT scenarios |
| Cross-team handoffs (reporting, training, integration) | Catalog files (workpaper types, etc.) |
|  | Field-level crosswalks |
|  | Reference / template files |
|  | Version history (in artifact headers) |
|  | Routine review feedback (informal) |

This is a deliberate division: structured tracking goes where structured tracking is easy; narrative content stays where prose works. Both tools earn their keep.

## Proposed tables

A connected suite of tables in our team's tab area within the project Airtable.

### 1. Deliverable Status

The "what state is everything in" view.

| Field | Type | Purpose |
|---|---|---|
| Workflow | Linked record (to PM's workflow records if available) | Which workflow this deliverable belongs to |
| Workflow status | Single select (workflow-level) | Not started / Design in progress / Design signed off / Being configured in Optro / UAT in progress / Ready for go-live |
| Deliverable | Single line text | Artifact name (Narrative, Diagram, Gap Analysis, RACI, UAT, etc.) |
| State | Single select | Per-deliverable state: Not Started / Draft / Internal Review / External Review / Signed Off / Blocked / Deferred |
| Lead | Single select (or linked record) | Which of the three of us is leading |
| Reviewers | Multi-select | Stakeholders who need to review |
| Last updated | Last modified time | Auto-populated |
| Next action | Single line text | What unblocks this next? |
| Blocking decisions | Linked records (to Decisions table) | Open items that need to resolve before progress |
| External reference | URL | Link to artifact in SharePoint when promoted |
| Notes | Long text | Anything else |

**Note on workflow status vs. deliverable state:** Workflow status is workflow-level (the whole workflow has one status). State is per-deliverable (the narrative might be Signed Off while UAT is still Draft). The two work together: a workflow reaches "Design signed off" when all required deliverables for that gate have State = Signed Off.

### 2. Decisions

Open questions, design questions, resolved decisions.

| Field | Type | Purpose |
|---|---|---|
| ID | Auto-number | Stable reference (D-001, etc.) |
| Title | Single line text | Short name |
| Type | Single select | Open Question / Design Question / Resolved |
| Context | Long text | Why this is a question and what's at stake |
| Why it matters | Long text | Impact if unresolved |
| Owner | Single select (or linked record) | Who's responsible for resolving |
| Workflow | Linked record | Which workflow (or "cross-cutting") |
| Related deliverables | Linked records (to Deliverable Status) | What can't progress until this resolves |
| Status | Single select | Open / In Progress / Resolved / Deferred |
| Resolution | Long text | What was decided |
| Confirmed by | Single line text | Name + role |
| Confirmed date | Date | When |
| Source | Single line text | Email, meeting, etc. |

### 3. Sign-Offs

Per-artifact approval records with defensibility criteria.

| Field | Type | Purpose |
|---|---|---|
| Artifact + version | Single line text | What was approved, what version |
| Workflow | Linked record | Which workflow |
| Approver name | Single line text | Who approved |
| Approver role | Single select | Methodology lead, audit leader, PGA, CAE, data & analytics, reporting, etc. |
| Lens | Single select | Methodology / Data / Reporting / Domain / Catalog Validation |
| Date approved | Date | When |
| Evidence location | URL or text | SharePoint location of approval email |
| Conditions | Long text | Any conditions |
| Status | Single select | Active / Withdrawn |
| Defensibility check | Checkbox | All four criteria met? |

### 4. Working Group Items

Agenda backlog + meeting log + items aligned + concerns raised.

| Field | Type | Purpose |
|---|---|---|
| Topic | Single line text | Item title |
| Type | Single select | Backlog / Discussed / Aligned / Concern raised |
| Why working group input needed | Long text | What we're asking them |
| Framing | Long text | Context, question, options, recommendation, what's not in scope |
| Priority | Single select | High / Medium / Low |
| Date scheduled | Date | When on agenda |
| Date discussed | Date | When discussion happened |
| Outcome | Long text | What was decided / deferred / re-framed |
| Owner of follow-up | Single line text | Who acts on outcome |
| Related deliverables | Linked records | What this affects |
| Related decisions | Linked records | What this resolves or creates |

### 5. Beta Feedback

Intake + disposition + closing-the-loop.

| Field | Type | Purpose |
|---|---|---|
| ID | Auto-number | Stable reference (BF-001, etc.) |
| Date received | Date | When |
| From | Single line text | Name + role |
| Workflow / artifact | Linked record (or text) | What it relates to |
| Type | Single select | Defect / Design Question / Training Gap / Preference / Out of Scope |
| Feedback summary | Long text | Paraphrased |
| Source | Single select | Verbal / Email / Meeting / Form |
| Disposition | Single select | Action / Decline / Defer / Escalate / Refer |
| Disposition rationale | Long text | Why this disposition |
| Action owner | Single select | Who acts on it |
| Re-version triggered | Checkbox | Did this cause an artifact re-version? |
| Loop closed date | Date | When we communicated back |
| Loop closed how | Long text | What we said back |
| Status | Single select | Open / In Progress / Done / Closed-No-Action |

### 6. Methodology Impacts

Handoff list for the methodology team.

| Field | Type | Purpose |
|---|---|---|
| Date identified | Date | When |
| Source workflow | Linked record | Where the impact came from |
| Change | Long text | What's changing |
| Methodology area affected | Single line text | Which section of procedures |
| Notes for methodology team | Long text | Context, confirming stakeholder, status |
| Status | Single select | Pending / Acknowledged / Accepted into methodology |
| Date accepted | Date | When methodology team confirmed |

### 7. Cross-Team Handoffs

Single table covering all four receiving teams (data migration, reporting, training, IT integration), with a Receiving Team field to filter views. Simpler than four separate tables.

| Field | Type | Purpose |
|---|---|---|
| Date identified | Date | When |
| Receiving team | Single select | Reporting / Training / IT Integration |
| Source workflow | Linked record | Where it came from |
| Item / issue / need / touchpoint | Long text | What we're surfacing |
| Impact on workflow | Long text | Why it matters to us |
| Receiving team contact | Single line text | Who on their side |
| Status | Single select | Flagged / Acknowledged / Actioned / Out of Scope |
| Resolution / action taken | Long text | What happened |
| Date resolved | Date | When |

### 8. Versioning and review feedback — handled lightly, not as separate tables

Two things we deliberately do *not* track in dedicated Airtable tables:

**Version history** — captured in a short header at the top of each markdown artifact (e.g., "v0.3 — added Reporting sequence on [date]") rather than a separate Change Log table. Material version changes generate Sign-Off rows when re-approved, so the audit trail of meaningful changes lives in the Sign-Offs table.

**Routine review feedback** — handled informally between team members (chat, doc comments, sync discussion). Feedback that rises above informal goes to the table that fits it: working group input → Working Group Items, individual reviewer disagreements that need escalation → Decisions (flagged for escalation), beta team feedback → Beta Feedback. We don't need a separate "review comments" table because every meaningful piece of feedback already has a home.

## Suggested views (across multiple tables)

Useful cross-cutting views to set up from day one:

- **Everything blocked** — Deliverable Status where State = Blocked, with Blocking Decisions visible
- **My open work** — Deliverable Status where Lead = me AND State ≠ Signed Off
- **This week's working group prep** — Working Group Items where Date Scheduled = this week
- **Open decisions awaiting me** — Decisions where Owner = me AND Status = Open
- **Beta feedback awaiting disposition** — Beta Feedback where Status = Open
- **Beta feedback awaiting loop closure** — Beta Feedback where Disposition is set AND Loop Closed Date is empty
- **Recent sign-offs** — Sign-Offs sorted by Date Approved descending, last 30 days
- **Cross-team handoffs awaiting acknowledgment** — Cross-Team Handoffs where Status = Flagged, age > 14 days

## Update cadence

- **As-it-happens** — each of us updates relevant tables when something changes
- **At every team sync (weekly)** — walk the cross-cutting views together
- **At every working group session** — update Working Group Items
- **At every external review event or sign-off** — update Sign-Offs and Deliverable Status
- **At end of every working session** — capture any new decisions or beta feedback that came up

## What this is NOT

- **Not the PM's project tracker** — that's their separate table; we link to it but don't replicate
- **Not the narrative content** — workflow narratives, gap analyses, design rationale, diagrams, catalogs, crosswalks all live in our markdown working space, not Airtable
- **Not the audit trail of approval emails themselves** — the actual emails are archived in SharePoint; Airtable holds the metadata pointing to them
- **Not a replacement for the procedures manual or methodology documents** — those are the methodology team's

## Risk to be aware of

These tables become critical project history. If the Airtable goes away (vendor change, permissions issue, base restructured), we lose institutional memory of decisions, sign-offs, and feedback. Mitigation: schedule monthly CSV exports to SharePoint, especially before any major project milestones.

## Decisions needed from the team

To stand this up:

1. **Workflow leads** — who leads each of the four workflows
2. **Single-source reviewer list** — names + roles of stakeholders we'll add as Reviewers
3. **State definitions** — exact controlled values (especially Internal Review vs. External Review boundary)
4. **Whether to link to PM's existing workflow records** — needs PM's input
5. **Who owns building it out** — one of us, or shared

## Initial population

Once tables are built:

- **Deliverable Status:** ~10-12 rows per workflow. ~40-50 rows once all four workflows are in flight.
- **Decisions:** Migrate the 22 items currently in our markdown decisions log
- **Sign-Offs:** Empty initially; populate as approvals come in (Copilot can backfill from email if we want history)
- **Working Group Items:** Empty initially; populate as we prepare for sessions
- **Beta Feedback:** Empty initially; populate as feedback comes in (or backfill if there's existing feedback)
- **Methodology Impacts:** Migrate the 4 items currently in our markdown methodology-impacts file
- **Cross-Team Handoffs:** Empty initially; populate as we surface items

## Estimated build effort

About a half-day of focused setup work for one person to build the tables, set up linked records, create initial views, and migrate existing markdown content.

---

*Prepared by [name], [date].*
