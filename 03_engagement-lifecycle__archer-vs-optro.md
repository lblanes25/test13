# Archer vs. Optro — Engagement / Audit Lifecycle

Side-by-side comparison of current-state Archer behavior to target-state Optro behavior, organized by phase.

**Purpose:** Lets a reviewer see exactly what's changing for each part of the workflow without reading two narratives in parallel.

**Format rules:**
- One row per material activity or decision point
- Factual descriptions of behavior, not evaluative language ("clunky," "improved," "modernized" — avoid)
- Activities that disappear in Optro get an explicit row showing them disappearing — never silently omitted
- Activities new in Optro that didn't exist in Archer get their own row
- The "Why" column is grounded in gap analysis, stakeholder decision, or methodology requirement — not personal preference

**Status:** Draft. Most rows pending confirmation. Items marked TBD will be filled in once Optro capabilities and stakeholder decisions are confirmed.

---

## Phase 1 — Kickoff / Planning (blended)

| Activity | Archer (today) | Optro (target) | Change for users | Why |
|---|---|---|---|---|
| Internal brainstorm session | Held informally, outputs captured in personal notes or shared docs outside Archer. | *(TBD — does this remain external, or move into Optro as part of planning template?)* | Pending decision. | Pending. |
| Scope definition | Captured in Archer planning record fields. | Captured in Optro engagement template fields. | Same activity, different field structure (mapping in progress with PM). | Configuration change, not behavioral. |
| Planning memo / audit program | Document drafted in Word, attached to Archer engagement record. | Drafted directly in Optro engagement template; lives with the engagement record. | One source of truth; no separate Word file to version. | Reduces version-control issues; auditee receives the same record that's archived. |
| Budget and staffing | Entered in Archer engagement record. | Entered in Optro engagement template. | Functionally equivalent. | Configuration change. |
| In-system planning approval (scope + budget) | Approval routes Auditor → Team Leader → Audit Leader → PGA. | *(TBD — proposed: combined gate with announcement memo approval. See `gap-analysis.md` Gap 1.)* | One PGA approval instead of two for the planning phase. | Eliminates redundant PGA touchpoint identified in gap analysis; reduces planning cycle time. Pending PGA confirmation. |
| Announcement memo drafting | Drafted in Word, attached to Archer engagement record after PGA approval. | Drafted directly in Optro engagement template. | Memo lives with the engagement record, not in a separate folder. | Reduces version-control issues. |
| Announcement memo approval | Separate approval chain up to PGA. | *(TBD — proposed: combined with planning approval. See Gap 1.)* | See above. | See above. |
| Memo issued to auditee | Sent via email, attachment archived. | *(TBD — does Optro distribute, or is email retained as the channel?)* | Pending decision. | Pending. |
| Entrance / kickoff meeting | Held externally; notes attached to Archer record. | Functionally equivalent — held externally, notes attached to Optro record. | No change. | No change. |
| PBC / evidence request list | Maintained in Archer; updated as evidence is received. | Maintained in Optro; updated as evidence is received. | Functionally equivalent (mapping fields with PM). | Configuration change. |

---

## Phase 2 — Fieldwork

| Activity | Archer (today) | Optro (target) | Change for users | Why |
|---|---|---|---|---|
| Walkthroughs | Documented in Archer workpaper templates. | Documented in Optro workpaper templates (per `workpaper-types.md` catalog). | Mapping per workpaper type still in progress. | Configuration change; depends on catalog finalization. |
| Control testing (design, operating effectiveness) | Per workpaper templates in Archer. | Per templates in Optro, mapped via `workpaper-types.md`. | Per type, see catalog. | See catalog. |
| Sample selection | Manual; documented in workpapers. | *(TBD — does Optro provide sampling tools, or is this still manual? Confirm with data & analytics team.)* | Pending. | Pending. |
| Workpaper creation | In Archer, by Auditor. | In Optro, by Auditor, using mapped templates. | Templates may have different field structures (catalog-driven). | Configuration change. |
| Workpaper review | Routed dynamically — one organizational level above the last person who worked on or approved the workpaper. | *(TBD — see `gap-analysis.md` Gap 2 on relative-level routing.)* | Depends on Optro capability. If supported natively: no change. If not: routing rule moves from system-enforced to procedurally-enforced. | Capability gap; recommendation pending Optro confirmation. |
| Integrated team execution (e.g., IT Audit) | Integrated team members work in parallel within the same engagement record. | *(TBD — confirm Optro participation model. See `decisions-log.md` #1.)* | Pending integrated team participation model. | Pending. |
| Status meetings | Held externally, notes attached to Archer record. | Functionally equivalent. | No change. | No change. |
| Draft issue identification | Issues drafted in Archer engagement record by Team Leader. | Issues drafted in Optro engagement record by Team Leader. | Functionally equivalent. | Configuration change. |
| Hours and budget tracking | Tracked in Archer. | Tracked in Optro. | Functionally equivalent (mapping fields with PM). | Configuration change. |
| Fieldwork exit checklist | *(TBD — current checklist contents not yet known. See `decisions-log.md` #4.)* | TBD | TBD | TBD |

---

## Phase 3 — Reporting

| Activity | Archer (today) | Optro (target) | Change for users | Why |
|---|---|---|---|---|
| Finalize issues | Issues refined from drafts in Archer. | Issues refined from drafts in Optro. | Functionally equivalent. | Configuration change. |
| Exit / closing meeting | Held externally, notes attached. | Functionally equivalent. | No change. | No change. |
| Management response collection | Collected (channel TBD — likely email or in-system); attached to Archer record. | *(TBD — does Optro support in-system management response, and if so, is auditee management given access?)* | Pending decision. | Pending — affects auditee user provisioning, in scope of PM. |
| Draft report creation | Drafted in Word from Archer data. | *(TBD — does Optro generate draft report from engagement data, or is it still drafted externally?)* | Pending. | Pending. |
| Internal draft report review | Routed Team Leader → Audit Leader → PGA → CAE. | Same chain expected. | Functionally equivalent (assuming Optro supports the chain natively). | No change. |
| Report rating / opinion assignment | Assigned in Archer. | Assigned in Optro. | Functionally equivalent. | Configuration change. |
| Final report approval | Per existing approval matrix (to be retrieved). | Per same approval matrix. | No change. | No change in policy; system change only. |
| Report distribution | Distributed externally (channel TBD). | Distributed externally; record retained in Optro. | Pending whether Optro distributes or just archives. | Pending. |
| Audit committee reporting | If applicable — handled externally with materials drawn from Archer record. | Functionally equivalent. | No change. | No change. |

*(Sequence within this phase is TBD — see `decisions-log.md` #5)*

---

## Phase 4 — Closeout

| Activity | Archer (today) | Optro (target) | Change for users | Why |
|---|---|---|---|---|
| Final workpaper archive / lockdown | Archer locks the engagement record at closure. | Optro locks the engagement record at closure. | Functionally equivalent. | Configuration change. |
| Hours and budget reconciliation | In Archer. | In Optro. | Functionally equivalent. | Configuration change. |
| Lessons learned / retrospective | Held externally; notes attached. | Functionally equivalent. | No change. | No change. |
| Audit entity update (issue impacts, new risks/controls) | Manual update by team to the audit entity record after closure. | *(TBD — does Optro automate this linkage, or is it still manual? See `gap-analysis.md` Gap 3.)* | Depends on Optro capability. | Cross-workflow dependency; affects audit entities workflow. |
| Issue handoff to issues workflow | Issues remain in Archer record; remediation tracked separately. | Issues handed off to Optro issues workflow at closure. | Functionally equivalent (clean handoff at the same point). | No change in policy. |
| Auditee satisfaction survey | Sent externally. | Sent externally. | No change. | No change. |
| Formal engagement close in system | Status change in Archer. | Status change in Optro. | Functionally equivalent. | Configuration change. |

---

## Activities going away (not replicated in Optro)

*(Populate as we identify activities the team currently performs in Archer that won't be replicated in Optro by deliberate design choice.)*

| Activity | Why removed | Confirmed by |
|---|---|---|
| *(none identified yet)* | | |

---

## Activities new in Optro

*(Populate as we identify Optro activities that weren't part of the Archer workflow.)*

| Activity | Why added | Confirmed by |
|---|---|---|
| *(none identified yet)* | | |
