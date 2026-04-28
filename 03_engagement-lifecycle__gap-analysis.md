# Gap Analysis — Engagement / Audit Lifecycle

Record of every place where Archer and Optro diverge in a way that requires a decision — not just configuration.

**Gap types:**
- **Capability** — Archer does something Optro cannot do natively
- **Behavioral** — both systems can do it, but the way Optro does it changes how users work
- **Design** — places where we *chose* not to replicate Archer because Optro suggests a better pattern

**What goes here:** Items requiring a decision. Routine configuration mapping does not. If you can't articulate the decision, it's a question — those go in `decisions-log.md` until they're scoped enough to become gaps.

**Status:** Draft. Three gaps identified from initial design work; more expected as workflow design and Optro capability discovery progress.

---

## Gap 1: Two PGA approvals in Kickoff/Planning

**Type:** Design

**Current Archer behavior:** Planning/scope approval routes through to PGA as one approval. Announcement memo separately routes through to PGA as a second approval. PGA touches the engagement twice in the same phase.

**Optro target behavior:** *(Proposed)* Combine the two PGA touchpoints into a single gate where the PGA reviews and approves both the planning record and the announcement memo together.

**The gap:** This is a deliberate design choice rather than a capability constraint. Optro can support either pattern. The question is whether to preserve current Archer behavior (two approvals) or simplify (one combined approval).

**Impact:**
- For users: PGAs spend less time on each engagement during planning. Audit Leaders see faster planning cycle times.
- For workflow integrity: No loss of oversight — PGA still reviews scope, budget, and announcement language. Just consolidated into a single review event.
- For downstream artifacts: RACI becomes cleaner. Methodology may need a language update (see `methodology-impacts.md`).

**Options considered:**
1. Preserve current Archer pattern — two separate PGA approvals.
2. Combine into single PGA gate — one approval covering planning + announcement.
3. Move announcement memo approval to the Audit Leader level (PGA reviews planning only) — reduces PGA workload further but removes their direct visibility into auditee-facing language.

**Recommendation:** Option 2. Preserves PGA oversight of both elements while removing redundancy. Option 3 introduces a meaningful policy change that should be a separate methodology conversation, not a side effect of system migration.

**Decision status:** Proposed
**Confirmed by:** Pending PGA representative review
**Cross-references:** `design-rationale.md` (TBD entry on consolidated planning gate); `methodology-impacts.md` (existing row on planning approval consolidation)

---

## Gap 2: Workpaper review routing relativity

**Type:** Capability *(pending Optro confirmation)*

**Current Archer behavior:** Workpaper review is routed dynamically — the system identifies the last person who worked on or approved the workpaper and routes review to someone one organizational level above them. Routing rule is relative, not role-based.

**Optro target behavior:** *(TBD)* If Optro supports relative-level routing natively, replicate the rule. If not, design a workaround that preserves the policy intent (review must be one level above last actor) within Optro's available routing model.

**The gap:** Optro's standard approval routing patterns are typically role-based (e.g., "Auditor's work routes to Team Leader"). Native support for "one level above whoever last touched this" is unconfirmed.

**Impact:**
- For users: If routing has to be manually assigned, Team Leaders will need to identify reviewers per workpaper instead of the system handling it. Adds friction. If hardcoded role-based routing is used, the system will sometimes route to the wrong person (e.g., when an Audit Leader has worked on a workpaper, it would still route to a Team Leader).
- For workflow integrity: Manual routing creates a small but real risk of self-review or insufficient independence if a Team Leader accidentally routes back to themselves.
- For downstream artifacts: RACI design is harder to make crisp. Methodology may need to describe the rule procedurally rather than as a system-enforced control.

**Options considered:**
1. Confirm Optro supports relative-level routing natively and configure accordingly.
2. Configure role-based routing pairs (Auditor → Team Leader, Team Leader → Audit Leader, Audit Leader → PGA) as fixed routes — system-enforced but loses the "last actor" flexibility.
3. Use Optro's manual reviewer assignment with a procedural rule that the assigner must select someone one level above the last actor — system-suggested, human-enforced.

**Recommendation:** Pending Optro capability confirmation. If option 1 is available, that's clearly preferred. If not, default to option 2 with a procedural exception process for cases where senior staff have worked on the workpaper. Option 3 is a fallback if neither work and is least defensible from an independence perspective.

**Decision status:** Proposed (option 1 vs. option 2 contingent on Optro capability)
**Confirmed by:** Pending — needs (a) Optro capability confirmation from PM/admin, and (b) stakeholder review of fallback option.
**Cross-references:** `design-rationale.md` entry on relative-level routing; `methodology-impacts.md` row on review procedures.

---

## Gap 3: Cross-workflow audit entity update at closeout

**Type:** Behavioral *(pending Optro confirmation)*

**Current Archer behavior:** At engagement closeout, the team manually updates the audit entity record with issue impacts, newly identified risks, and any added or modified controls. The link between the engagement and the audit entity is recorded by manual reference.

**Optro target behavior:** *(TBD)* If Optro supports automated linkage between engagements and audit entities — propagating issue impacts, new risks, and new controls into the entity's risk assessment — this becomes an automated step. If not, manual update remains.

**The gap:** Whether the linkage is automated or manual changes the closeout workflow significantly. Manual linkage creates a real risk of inconsistency (entity record drifts from engagement findings); automated linkage creates a configuration burden but ensures consistency.

**Impact:**
- For users: Manual = closeout takes longer and team must remember to update. Automated = closeout is shorter but team must verify the propagation worked correctly.
- For workflow integrity: Manual carries higher risk of audit entity records becoming stale or inaccurate. Automated reduces that risk but introduces a new validation step.
- For downstream artifacts: Affects audit entities workflow design directly. RACI and methodology language differ depending on which model is chosen.

**Options considered:**
1. Configure Optro for automated propagation of issues, risks, and controls from engagement to audit entity at closeout.
2. Keep manual update step but use Optro's record-linking feature to make the navigation easier.
3. Hybrid — automate issue/risk/control creation in the audit entity but require manual confirmation/approval before the audit entity record is updated.

**Recommendation:** Pending Optro capability confirmation. If option 1 is supported, prefer option 3 — captures the efficiency of automation while preserving a deliberate review step (consistent with current behavior of "the team must look at the entity record and update it"). Option 2 is the fallback if automation isn't supported.

**Decision status:** Proposed
**Confirmed by:** Pending — needs Optro capability confirmation and audit entities workflow design alignment.
**Cross-references:** `methodology-impacts.md` row on audit entity update; will become relevant to audit entities workflow once started.

---

## Pending gaps (questions not yet ready to be gaps)

These are unresolved questions that may become gaps once enough is known to define the decision. Until then, they're tracked in `decisions-log.md`.

- Optro support for engagement-level risk assessment as a distinct activity (decisions-log #2)
- Integrated team participation model in Optro (decisions-log #1)
- Reporting phase sequence (decisions-log #5) — may surface gaps once known
- Fieldwork exit checklist contents (decisions-log #4) — may surface gaps once known
