# Project File Index

ChatGPT projects don't support folders, so files in this project use a numeric-prefix + double-underscore naming convention to convey logical structure. Read this index first to understand how files relate.

**Naming convention:**
- `NN_` = top-level grouping (sorts alphabetically in the file list)
- `__` (double underscore) = subfolder separator
- Hyphens within a section = standard word separators

So `03_engagement-lifecycle__narrative.md` should be read as: *engagement-lifecycle folder, narrative file*.

---

## How to navigate this project

When the assistant needs to find a specific file:

- Project front page → `00_README.md`
- This index → `00_INDEX.md`
- Cross-cutting living documents → `01_*.md` (decisions log, methodology impacts, working group log, beta feedback log)
- Cross-team handoff lists → `02_handoffs__*.md`
- Engagement lifecycle workflow artifacts → `03_engagement-lifecycle__*.md`
- Fieldwork workflow artifacts → `04_fieldwork__*.md`
- Reference / template files → `05_reference__*.md`
- Communication tools (director one-pager, Airtable proposal) → `06_communications__*.md`

---

## Full file list with purpose

### 00 — Front page

| File | Purpose |
|---|---|
| `00_README.md` | Project front page: scope, workflow status, three-tool model, top open items |
| `00_INDEX.md` | This file — how to navigate the project |

### 01 — Cross-cutting living documents

These would normally live at project root.

| File | Purpose |
|---|---|
| `01_decisions-log.md` | Open questions, design questions, resolved decisions (22 items currently). **Migration source for Airtable Decisions table.** |
| `01_methodology-impacts.md` | Handoff list for the methodology team. **Migration source for Airtable Methodology Impacts table.** |
| `01_working-group-log.md` | Working group agenda backlog, meetings, alignments, concerns. **Migration source for Airtable Working Group Items table.** |
| `01_beta-feedback-log.md` | Beta team feedback intake, disposition, closing-the-loop. **Migration source for Airtable Beta Feedback table.** |

### 02 — Cross-team handoffs

These would normally live in a `/handoffs/` folder.

| File | Purpose |
|---|---|
| `02_handoffs__reporting-needs.md` | Reporting/dashboard/KPI needs for the reporting team |
| `02_handoffs__training-implications.md` | Training implications for whoever owns training (TBD) |
| `02_handoffs__integration-touchpoints.md` | System integration needs for IT integration workstream |

### 03 — Engagement lifecycle workflow

These would normally live in `/workflows/engagement-lifecycle/`.

| File | Purpose |
|---|---|
| `03_engagement-lifecycle__narrative.md` | Process narrative across 4 phases (Kickoff/Planning, Fieldwork, Reporting, Closeout) |
| `03_engagement-lifecycle__diagram.md` | Mermaid flowchart of all 4 phases |
| `03_engagement-lifecycle__archer-vs-optro.md` | Side-by-side comparison, target column mostly TBD until Optro specifics confirmed |
| `03_engagement-lifecycle__gap-analysis.md` | 3 gaps detailed (PGA approval consolidation, relative-level routing, audit entity update) |
| `03_engagement-lifecycle__uat.md` | UAT scenarios across happy path, rejection paths, variants, boundary cases, cross-workflow handoffs |
| `03_engagement-lifecycle__design-rationale.md` | Why major design choices were made; 3 entries seeded |

### 04 — Fieldwork workflow

These would normally live in `/workflows/fieldwork/` (and `/workflows/fieldwork/crosswalks/`).

| File | Purpose |
|---|---|
| `04_fieldwork__workpaper-types.md` | Catalog of workpaper variants — populate from procedures and existing crosswalk doc |
| `04_fieldwork__crosswalks__control-test.md` | Field-level Archer→Optro mapping for control testing workpapers |

### 05 — Reference / templates

Read-when-needed, not actively maintained.

| File | Purpose |
|---|---|
| `05_reference__extraction-prompts.md` | Prompts for sanitizing manual content (less central now that ChatGPT is approved for the manual directly; retained for reference) |
| `05_reference__copilot-prompts.md` | Prompts for mining Outlook via Copilot to backfill sign-offs, decisions, review feedback, and design rationale |
| `05_reference__catalog-inventory-and-validation.md` | Reusable 5-section checklist for building any variant catalog |

### 06 — Communication tools

For sharing with director and team — not for daily work.

| File | Purpose |
|---|---|
| `06_communications__director-summary.md` | One-pager for briefing the director |
| `06_communications__airtable-tracker-proposal.md` | Proposal for the team to set up the seven-table Airtable tracking suite |

---

## Tool model reminder

> **Airtable → status, decisions, ownership**
> **SharePoint → final signed-off artifacts**
> **Everything else → disposable**

The files in this project are drafting/working content. They are non-authoritative. Final approved versions live in SharePoint; tracking lives in Airtable. Several `01_*.md` files are migration sources for Airtable — once those tables are populated, the markdown copies are no longer maintained.

---

## What's NOT in this project

The following files were generated during framework design but are not part of the active project:

- `change-log.md`, `sign-off-log.md`, `review-comments-log.md` — superseded by Airtable tables and version-history-in-headers
- `handoffs-data-quality-flags.md` — superseded by field-level crosswalks
- `CLAUDE.md` — legacy from earlier in the design process
- `import-inventory.md` — setup roadmap, not part of the live project

If you see references to these in older artifacts, they're historical context and can be ignored.
