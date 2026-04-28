# Design Rationale — Engagement / Audit Lifecycle

Captures the *why* behind material design choices. Each entry is a short, standalone paragraph: the decision, the alternatives considered, and why this option was chosen.

**Purpose:** Protects the team if a design is questioned later. "Why did you design it this way?" should have an answer in this file, not in someone's memory.

**Update discipline:** Add an entry every time a material design decision is made. Not at the end of the project — while the reasoning is fresh.

---

## Format

Each entry uses this structure:

```
### [Date] — [Short decision title]

**Decision:** What was decided.

**Alternatives considered:** What else was on the table.

**Why this option:** The reasoning. Include any stakeholder input, constraints, and tradeoffs.

**Confirmed by:** Name, role, date (if applicable). If not yet confirmed, state "proposed — pending confirmation."

**Related artifacts:** Links to narrative sections, gap-analysis entries, or decisions-log items.
```

---

## Entries

### [Session 1] — Blended Kickoff and Planning phase

**Decision:** Treat Kickoff and Planning as a single blended phase in the workflow design, rather than two separate phases.

**Alternatives considered:**
1. Standard 5-phase model (Kickoff → Planning → Fieldwork → Reporting → Closeout).
2. Fully separate Kickoff as its own gated phase.
3. Blended phase (chosen).

**Why this option:** The user's team operates Kickoff and Planning as overlapping activities in practice. Forcing a separation would create artificial phase gates that don't match how work actually happens. The blended model preserves the distinct activities without imposing a false sequence.

**Confirmed by:** Proposed — pending methodology review. Methodology may describe these as separate; if so, either methodology updates or the workflow adjusts to match (see `methodology-impacts.md`).

**Related artifacts:** `narrative.md` Phase 1; `methodology-impacts.md` (row on blended phase language).

---

### [Session 1] — Relative-level workpaper review routing

**Decision:** Workpaper reviewer must be one organizational level above the last person who worked on or approved the workpaper, rather than a fixed role (e.g., "Team Leader reviews all workpapers").

**Alternatives considered:**
1. Fixed-role review (e.g., Team Leader always reviews Auditor work; Audit Leader always reviews Team Leader work).
2. Relative-level review based on last actor (chosen).
3. Risk-tiered review (high-risk workpapers get higher-level review; low-risk gets single-tier).

**Why this option:** The user's team already operates on the relative-level rule. It scales across different engagement sizes and team compositions without needing workflow branches per scenario. It also ensures review independence without requiring fixed role assignments that can break when staffing varies.

**Tradeoff flagged:** Requires Optro to support relative-level routing natively. If Optro cannot, the alternative would require either (a) hardcoded role pairs per workpaper type, or (b) manual reviewer assignment with a policy rule. See `gap-analysis.md` design question B.

**Confirmed by:** Proposed — pending Optro capability confirmation and stakeholder review.

**Related artifacts:** `narrative.md` Phase 2; `gap-analysis.md` design question B.

---

### [Session 1] — Engagement workflow owns draft issues and management responses

**Decision:** The engagement lifecycle workflow includes finding identification, draft issue creation, and management response collection. The separate issues workflow picks up at final remediation tracking only.

**Alternatives considered:**
1. Engagement workflow ends at final report; issues workflow owns everything from first finding onward.
2. Engagement workflow owns drafts + responses; issues workflow owns remediation (chosen).
3. Both workflows run in parallel during fieldwork and reporting.

**Why this option:** Finding identification and management response happen in the flow of the engagement and belong in that context. Separating them would force artificial handoffs mid-engagement. Remediation tracking, by contrast, continues long after engagement closeout and genuinely belongs in its own workflow.

**Confirmed by:** Proposed — pending stakeholder review.

**Related artifacts:** `narrative.md` Phase 3; cross-workflow handoff noted in Phase 4 Closeout.

---

*(add further entries here as design decisions accumulate)*
