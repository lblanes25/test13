# Engagement / Audit Lifecycle — Workflow Narrative

**Status:** Draft, Session 1. Several items pending confirmation — see `decisions-log.md`.

---

## Scope

Covers an individual audit engagement from **kickoff through closeout**. The annual audit plan and engagement selection are handled by a separate workflow.

## Roles

| Role | Abbr. | Responsibility |
|---|---|---|
| Staff / Senior Auditor | — | Performs fieldwork; drafts workpapers |
| Team Leader | Director | Runs the engagement at the workpaper level; drafts issues |
| Audit Leader | VP | Runs the audit at the engagement level |
| Portfolio General Auditor | PGA (SVP) | Owns a portfolio of audit entities (~30 across org); approves key engagement gates within portfolio |
| Chief Audit Executive | CAE | Final approval authority |
| Auditee management | — | Leadership of the department/function being audited |
| Process / Control Owners | — | SMEs providing evidence |
| Integrated teams (e.g., IT Audit) | — | Specialized teams participating in the engagement; *participation model TBD* |

## Phases

### Phase 1 — Kickoff / Planning *(blended)*

**Activities**
- Internal brainstorm session
- Scope definition (objectives, criteria, in/out of scope)
- Planning memo / audit program development
- Budget and staffing (hours, assignments, integrated team needs)
- Announcement / engagement letter to auditee (one memo, internal approval first)
- Entrance / kickoff meeting with auditee
- Evidence request list (PBC list)
- *Engagement-level risk assessment — TBD (may be embedded in planning or absent)*

**Approval gates**
1. **In-system planning approval** — scope + budget approved up through Team Leader → Audit Leader → PGA
2. **Announcement memo approval** — same chain, up to PGA; memo then issued to auditee

> ⚠️ Design question for gap analysis: two separate PGA gates in the same phase. Explore consolidation in Optro.

**Exit:** Both approvals complete; memo issued; entrance meeting held.

---

### Phase 2 — Fieldwork

**Activities**
- Walkthroughs / process understanding
- Control testing (design and operating effectiveness)
- Sample selection and evidence gathering
- Workpaper creation and documentation
- Workpaper review *(see rule below)*
- Integrated team execution (IT Audit, etc.)
- Status meetings with auditee
- Draft issue identification (first versions of findings)
- Hours / budget tracking

**Workpaper review rule**
Two-tier. The reviewer must be **one organizational level above** whoever last worked on or approved the workpaper. Relative, not fixed-role.

> ⚠️ Design question for gap analysis: verify Optro supports relative-level approval routing.

**Exit:** Fieldwork admin checklist complete — *checklist contents TBD.*

---

### Phase 3 — Reporting

**Activities**
- Finalize issues (refine from draft versions)
- Exit meeting / closing conference with auditee
- Management response collection on issues
- Draft report creation
- Internal draft report review (Team Leader → Audit Leader → PGA → CAE)
- Report rating / opinion assignment
- Final report approval
- Report distribution to auditee / stakeholders
- Audit committee reporting (if applicable)

**Sequence:** *TBD — come back to confirm order of operations.*

**Approval:** Existing approval matrix governs this phase (at minimum the final report). *Document to be retrieved and incorporated into the RACI.*

---

### Phase 4 — Closeout

**Activities**
- Final workpaper archive / lockdown
- Hours and budget reconciliation
- Lessons learned / retrospective
- **Audit entity update** — document issue impacts in the audit entity's risk assessment; add any newly identified risks, controls, or other elements
- Issue handoff to the Issues workflow for ongoing remediation tracking
- Auditee satisfaction survey
- Formal engagement close in the system (status change)

> ⚠️ Cross-workflow dependency: Closeout feeds the **Audit Entities** workflow (risk assessment refresh, new risks/controls added). Design for clean linkage in Optro without manual re-entry.

---

## Open items

See `decisions-log.md` for the full list. Highest-priority items to resolve:

1. Retrieve the existing approval matrix — will unlock the RACI.
2. Confirm Reporting sequence.
3. Define the Fieldwork admin checklist contents.
4. Clarify integrated team participation model.
