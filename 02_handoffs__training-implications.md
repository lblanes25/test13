# Training Implications — Handoff (Owner TBD)

Running list of design changes that will require auditor training or change-management effort at go-live.

⚠️ **Training ownership is unconfirmed** (see `/decisions-log.md` #7). Until an owner is named, this file accumulates implications. Treat this as mandatory work, not optional — a well-designed workflow with no training plan is a failed migration.

**Format:** Newest at top. Describe the change, who needs to be trained, and what "fluent" looks like for them.

---

| Date | Source workflow | Change affecting users | Roles needing training | What fluency looks like | Priority | Status |
|---|---|---|---|---|---|---|
| *Example* | engagement-lifecycle | Planning and announcement memo approvals may be consolidated into a single PGA gate | PGAs, Audit Leaders | Know that they review scope + memo together in one approval; understand the new artifact bundle | Medium | 🟡 Pending training owner |
| *Example* | engagement-lifecycle | Workpaper review uses relative-level routing | Auditors, Team Leaders, Audit Leaders | Know how to identify "one level above last actor" in Optro UI; know when to escalate if routing looks wrong | High | 🟡 Pending training owner |

---

## Priority key

- **High** — user cannot function in new workflow without training
- **Medium** — user can function but will make avoidable mistakes without training
- **Low** — nice-to-have context; user will learn by doing

## Status key

- 🟡 Pending training owner — no receiving team yet
- 🟢 Handed off — training owner has accepted the implication
- ✅ Training planned/built — training owner has scoped the work
- ❌ Deferred / not addressed — surface as a known limitation
