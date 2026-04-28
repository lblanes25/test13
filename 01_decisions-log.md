# Decisions Log — Engagement/Audit Lifecycle Workflow

Running log of open questions, pending confirmations, and decisions made. Updated every session.

---

## 🔴 Open — Needs Your Confirmation

### 1. Integrated team participation model
**Context:** Integrated teams like IT Audit participate in engagements. Unclear whether they embed as members of the engagement team, run parallel sub-engagements that roll up, or both depending on scope.
**Why it matters:** Determines how Optro models team assignments, workpaper ownership, and review routing.
**Owner:** You

### 2. Engagement-level risk assessment
**Context:** Not selected as a Kickoff/Planning activity. May be embedded in planning memo, done informally during brainstorm, or not performed at the engagement level.
**Why it matters:** Optro has dedicated engagement risk assessment functionality — decide whether to adopt or skip.
**Owner:** You

### 3. Complete Kickoff/Planning activity list
**Context:** You noted "may be more things but I don't have access currently."
**Why it matters:** Narrative and RACI incomplete until full activity set confirmed.
**Owner:** You (pull from Archer or current team documentation)

### 4. Fieldwork exit gate / admin checklist
**Context:** There's a fieldwork admin checklist that must be completed to close fieldwork. Your team defines it. Specific contents unknown.
**Why it matters:** Gate between Fieldwork and Reporting — can't finalize phase boundary or RACI without it.
**Owner:** You (locate current checklist)

### 5. Reporting phase sequence
**Context:** Order of operations within Reporting (finalize issues → mgmt response → draft report → exit meeting → internal review → final report) is not confirmed.
**Why it matters:** Workflow diagram and RACI need correct sequencing; multiple valid patterns exist.
**Owner:** You

### 6. Existing approval matrix retrieval
**Context:** You have a formal approval matrix document covering engagement-level approvals (at least final report, likely more). Content unknown.
**Why it matters:** Will directly populate the RACI artifact and resolve several open approval questions.
**Owner:** You (locate and share the matrix)

### 7. Training ownership
**Context:** Unclear who owns training auditors on the new Optro workflows (our team, L&D, methodology, or shared).
**Why it matters:** Until confirmed, training-relevant implications pile up in `/handoffs/training-implications.md` without a receiving owner. Risk of the list being ignored at go-live.
**Owner:** You / project leadership

### 8. Reporting ownership confirmation
**Context:** Reporting, dashboard, and KPI design appears to sit with the data migration team. Not formally confirmed.
**Why it matters:** Need confirmed owner to route `/handoffs/reporting-needs.md` items to. If assumption is wrong, reporting could fall through the cracks.
**Owner:** You (confirm with PM)

### 9. Decision authority confirmation
**Context:** Operating assumption is "recommend-only" — team proposes, stakeholders approve. Not formally confirmed.
**Why it matters:** Shapes how every deliverable is framed and how sign-off is treated. If team actually has more decision authority than assumed, the process is heavier than needed. If less, protections are stronger than stated.
**Owner:** You (confirm with project sponsor / PM)

### 10. Escalation sponsor identity
**Context:** Disagreements between reviewers escalate to "whoever sponsors the project." Specific person / committee not yet named in our documentation.
**Why it matters:** Need a named escalation path or the process breaks on first real conflict.
**Owner:** You

### 11. SharePoint sync policy
**Context:** Working default is "promote when ready for review and at phase boundaries," but not formally confirmed. You indicated you'll figure it out as you go.
**Why it matters:** Without a policy, formal artifacts could live only in the working space without making it to the canonical repo. If a governance gap appears later, it's hard to prove what was when.
**Owner:** You (confirm when comfortable)

### 12. Post-go-live ownership of workflow docs
**Context:** Unknown who will own the workflow artifacts after migration (our team retained, methodology, new BAU owner, or shared).
**Why it matters:** Ownership gap at go-live means docs could go stale or be mishandled. Also affects how we design for handover.
**Owner:** You / project leadership

### 13. Post-go-live change control committee
**Context:** Future workflow changes: routine handled by methodology, major go through a committee. Committee not yet named.
**Why it matters:** "Major changes go to a committee" doesn't work if there's no committee. Needs to exist before go-live so day-one changes have a path.
**Owner:** You / project leadership

### 14. Workflow lead assignments
**Context:** Three-person team (you, one peer, director). Each major workflow needs a designated lead who drafts, runs working group framings, and stewards artifacts. Not yet assigned.
**Why it matters:** Without lead ownership, three people working in parallel produce inconsistent narratives across workflows. Director likely takes the most politically sensitive workflow; non-director members take the others.
**Owner:** Team conversation

### 15. Working group cadence and membership
**Context:** Working group is referenced as a recurring forum but cadence (weekly? biweekly?) and named members not yet captured in our documentation.
**Why it matters:** Cadence drives how much can be brought forward; membership clarifies which lenses are represented in the group vs. needing separate review.
**Owner:** You (confirm with project leadership)

### 16. Beta feedback intake owner
**Context:** Beta team feedback can come into anyone's email or Teams. Without one designated intake owner, feedback can be inconsistently captured or lost.
**Why it matters:** Beta users stop providing useful feedback if it isn't seen to be used. Single intake owner protects the loop.
**Owner:** Team conversation (one of the three)

### 17. Legacy data access for our team
**Context:** Migration team owns *what data moves* to Optro. Our workflows often need to reference past engagements — will auditors be able to look up a 2024 engagement in three years, in Archer (read-only) or Optro? If migrated, the structure may differ from native records.
**Why it matters:** Workflow design needs to address how historical work is referenced. This may not be our responsibility, but if it's nobody's, it surfaces post-go-live as a complaint.
**Owner:** You (confirm with PM that someone owns this)

### 18. Audit trail and immutability requirements
**Context:** Audit functions typically have strict requirements about audit trails — who did what when, with no retroactive alteration. Our workflow design has not yet explicitly addressed what's immutable, what's editable, and who can see edit history in Optro.
**Why it matters:** Often surfaces in regulator review. Embarrassing if missed. Likely shared between us and the PM, but worth being explicit.
**Owner:** You / PM

### 19. Concurrent engagements during migration cutover
**Context:** Engagements in-flight during the cutover need a path — finish in Archer? Move mid-stream to Optro? A specific transitional workflow may be needed, separate from target-state workflows.
**Why it matters:** Common gap in migrations. If the PM hasn't addressed it, it's worth raising. If they have, our workflow design needs to align.
**Owner:** You (confirm with PM)

### 20. Records retention model in Optro
**Context:** How long engagements are retained, in what form, and where. Optro likely has its own retention model that may or may not match policy.
**Why it matters:** Usually a methodology + legal question but workflow design touches it. May be in scope for methodology team rather than us.
**Owner:** You (raise with methodology / legal if not already addressed)

### 21. Disaster / system unavailability fallback
**Context:** Current Archer workflows may have implicit assumptions about system availability. Optro may have different SLAs or recovery characteristics. No manual fallback documented for fieldwork during system downtime.
**Why it matters:** Workflow design that assumes constant system availability isn't realistic. May be low priority but worth a deliberate decision (accept the risk vs. design a fallback).
**Owner:** You (raise with PM and IT integration team)

### 22. Accessibility and accommodations in Optro
**Context:** Team members may need screen readers, color-vision accommodations, or other accessibility support. Optro's support for these needs has not been verified.
**Why it matters:** Often missed in design and surfaces painfully at training. Easier to address now than to retrofit.
**Owner:** You (verify with PM whether accessibility was part of vendor evaluation)

---

## 🟡 Design Questions (for Gap Analysis)

### A. Two PGA approvals in Kickoff/Planning
Both in-system planning approval (scope + budget) and announcement memo approval route up to PGA. Consider combining into a single PGA gate in Optro.

### B. Dynamic workpaper review routing
Review must be one level above whoever last worked on or approved the workpaper — a relative rule, not fixed role. Verify Optro natively supports relative-level approval routing; if not, design workaround.

### C. Cross-workflow feedback loop
Closeout triggers updates to the Audit Entities workflow (issue impacts added to entity risk assessment, new risks/controls added). Ensure Optro supports this linkage cleanly without manual re-entry.

---

## ✅ Resolved / Confirmed

| Date | Item | Decision |
|---|---|---|
| Session 1 | Workflow boundaries | Engagement kickoff → closeout. Annual planning is a separate workflow. |
| Session 1 | Phases | Kickoff + Planning (blended) → Fieldwork → Reporting → Closeout. |
| Session 1 | Issue workflow handoff | Engagement workflow owns draft issues + management response; issues workflow picks up at final remediation tracking. |
| Session 1 | Roles | Auditor, Team Leader (Dir), Audit Leader (VP), PGA (SVP), CAE, auditee management, process/control owners, integrated teams. |
| Session 1 | PGA definition | Portfolio General Auditor (~30 org-wide, each owns a portfolio of audit entities). |
| Session 1 | Planning approval chain | Both in-system scope/budget approval and announcement memo approved up through to PGA. |
| Session 1 | Workpaper review rule | Two-tier, relative: reviewer must be one level above the last person who worked on or approved the workpaper. |
| Session 1 | Closeout activities | Archive, reconciliation, lessons learned, issue handoff, satisfaction survey, system close, **plus audit entity update** (issue impacts + newly identified risks/controls fed back). |
| Session 1 | Scope: integrations | Not our team — separate IT integration workstream. We flag touchpoints to `/handoffs/integration-touchpoints.md`. |
| Session 1 | Scope: data cleanup | Data migration team owns the decisions. Data observations surfaced during workflow design are captured in the field-level crosswalks (their dispositions are the handoff to data migration), not in a separate file. |
| Session 1 | Scope: methodology | Methodology team owns updates. We flag implications to `/methodology-impacts.md` but do not rewrite methodology. |
| Session 1 | Sign-off model | Multi-party by area. Every workflow is reviewed by methodology, data & analytics, and reporting teams at minimum, plus domain-specific stakeholders (PGAs, audit leaders, etc.). Each reviewer's lens is recorded explicitly. |
| Session 1 | Disagreement handling | We document both views neutrally and escalate to the project sponsor. We do not arbitrate. |
| Session 1 | Confidentiality tier | Workflow artifacts are at the same tier as the procedures manual — highly confidential, limited distribution. |
| Session 1 | Source of truth | SharePoint (approved internal repo) is canonical. Claude Code is personal planning space. |
| Session 1 | Sign-off mechanics | Email approval. Defensibility requires: references artifact version, archived in SharePoint, approver role/lens clear, logged in sign-off-log.md. |
| Session 1 | Post-go-live change control model | Lighter-touch: methodology handles routine changes, a committee handles major changes. Committee not yet named (open item). |
