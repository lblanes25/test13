# Workpaper Types Catalog — Fieldwork

Catalog of workpaper variants that plug into the fieldwork spine workflow.

**Relationship to the spine:** The fieldwork narrative describes the lifecycle every workpaper goes through (plan → execute → document → review → resolve → finalize). This catalog captures *what changes* between workpaper types — templates, evidence requirements, review criteria, special roles, and approval rules.

**Status:** Draft. Inventory and validation activities tracked below — catalog is not a deliverable until they're complete.

---

## Catalog

| Type ID | Workpaper type | Current Archer template | Evidence requirements | Review criteria (what makes it "good") | Roles involved | Approval rules | Optro target template | Notes |
|---|---|---|---|---|---|---|---|---|
| WP-01 | *(e.g., Process walkthrough)* | *(template name in Archer)* | *(what evidence must be attached)* | *(criteria reviewer applies)* | *(any roles beyond the standard fieldwork team)* | *(any rules beyond the standard "one level above" review)* | *(target Optro template, once designed)* | *(any quirks, exceptions, recent issues)* |
| WP-02 | *(e.g., Control design test)* | | | | | | | |
| WP-03 | *(e.g., Operating effectiveness test)* | | | | | | | |
| WP-04 | *(e.g., IT general controls test)* | | | | IT Audit integrated team | | | |
| WP-05 | *(e.g., Sampling memo)* | | | | | | | |
| WP-06 | *(e.g., Data analysis workpaper)* | | | | Data & analytics team consultation | | | |
| WP-07 | *(e.g., Third-party / SOC 1 reliance)* | | | | | | | |

*(extend as variants are identified)*

---

## Inventory and validation activities

These activities must be completed before this catalog is treated as a deliverable. Track each item's status in `decisions-log.md` for the fieldwork workflow.

### 1. Procedures manual inventory
- [ ] Pull the list of workpaper types referenced in the procedures
- [ ] Cross-check against the catalog — every type from the procedures should appear here
- [ ] For any type in the procedures missing from the catalog: add it
- [ ] For any type in the catalog not referenced in the procedures: confirm it's still in use, or remove

### 2. Recent-engagement validation
- [ ] Identify 3–5 recent engagements that span different audit types (operational, financial, IT, integrated)
- [ ] For each, list the workpaper types actually used
- [ ] Reconcile against the catalog — note any types used in practice that aren't in the catalog
- [ ] For each reconciliation gap, decide: add to catalog, or treat as a one-off needing a procedural decision

### 3. Role-based validation
- [ ] Have a Senior Auditor or Team Leader review the catalog and flag any missing types they regularly produce
- [ ] Have an IT Audit lead review specifically for IT-specific workpaper types
- [ ] Have a Data & Analytics representative review for analytics-related workpapers
- [ ] Have an Audit Leader review the review criteria column — these are what *they* will use to assess quality

### 4. Optro capability check
- [ ] For each catalog row, confirm whether Optro supports configuring this template natively
- [ ] For any type Optro can't replicate cleanly, log a `gap-analysis.md` entry
- [ ] If Optro doesn't natively support a workpaper-type catalog at all, that's itself a gap — flag prominently

### 5. Methodology cross-check
- [ ] Compare the catalog to the methodology team's view of what workpaper types should exist
- [ ] If methodology lists types not in current practice, decide whether they should be added (methodology drives) or removed from methodology (practice drives)
- [ ] Log any divergence to `methodology-impacts.md`

---

## Catalog evolution

This catalog is a living document. Track changes here as they're made.

| Date | Change | Why | Source / who confirmed |
|---|---|---|---|
| *(populate as catalog is updated)* | | | |
