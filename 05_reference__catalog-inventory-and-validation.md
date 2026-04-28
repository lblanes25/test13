# Catalog Inventory & Validation Checklist

Reusable checklist for building any variant catalog (workpaper types, entity types, issue rating types, audit types, etc.). Run this whenever a workflow has material variation that needs a catalog.

**Why this exists:** A catalog with no validation history is a draft, not a deliverable. Stakeholders sign off on catalogs as if they're complete; if they're missing variants, the gap shows up at go-live. This checklist forces the validation work to happen before the catalog is treated as final.

**How to use:** When starting a new catalog, copy this checklist into the workflow's folder (or into the catalog file itself). Track each item until done. Don't mark the catalog as a deliverable until all five sections are complete or the gap is explicitly accepted.

---

## 1. Source-document inventory

Pull the list of variants from the authoritative current-state document — usually the procedures manual, but could be a templates library, a system configuration export, or another canonical source.

- [ ] Identify the source document(s) for this catalog
- [ ] Extract every variant referenced in the source — do not rely on memory
- [ ] Add any missing variants to the catalog
- [ ] For any catalog entries not referenced in the source: confirm they're still in use, or remove

**Common pitfall:** stopping here. Source documents are often out of date — this is necessary but not sufficient.

---

## 2. Recent-use validation

Validate the catalog against actual recent practice, because procedures and templates lag practice.

- [ ] Identify 3–5 recent uses spanning the variation you expect (e.g., for engagements: span audit types; for issues: span ratings)
- [ ] List the variants actually used in each
- [ ] Reconcile against the catalog
- [ ] For each gap, decide: add to catalog, or treat as a one-off needing a procedural decision

**Common pitfall:** picking only easy/recent examples. Pick deliberately for variety — old ones, edge ones, integrated ones.

---

## 3. Role-based validation

People who do the work see what documents miss. For each major role that uses or produces variants from this catalog, get explicit review.

- [ ] List the roles that interact with the catalog (typically: producers, reviewers, approvers, integrated specialists)
- [ ] For each role, identify a specific person to review (not "the methodology team" — name a person)
- [ ] Have each named reviewer:
  - Flag missing variants
  - Flag merged variants that should be split
  - Flag obsolete variants that should be removed
  - Confirm the variant-specific fields (review criteria, evidence requirements) match what they actually do/expect
- [ ] Capture each reviewer's sign-off in `sign-off-log.md` with their lens noted as "catalog validation"

**Common pitfall:** treating this as optional. It's the most important validation step — documents lie, people don't.

---

## 4. Target-system capability check

For migration projects, validate that the target system can actually support each variant.

- [ ] For each catalog row, confirm whether the target system supports configuring this variant natively
- [ ] For any variant the target can't replicate cleanly, log a `gap-analysis.md` entry
- [ ] If the target doesn't support a catalog/template structure at all, that's itself a gap — flag prominently
- [ ] For any gap that won't be closed before go-live, add to `known-limitations.md`

**Common pitfall:** assuming the target supports what the source does. Always verify per variant, not per workflow.

---

## 5. Methodology / policy cross-check

The variant catalog must be consistent with what methodology says should exist.

- [ ] Compare the catalog to the methodology team's documented variants
- [ ] If methodology lists variants not in current practice, decide: add them (methodology drives) or update methodology (practice drives)
- [ ] If practice has variants methodology doesn't address, that's typically a methodology gap — flag to the methodology team
- [ ] Log any divergence to `methodology-impacts.md`

**Common pitfall:** doing this last. If methodology and practice diverge significantly, you may need to redo earlier validation work after the divergence is resolved.

---

## Sign-off discipline for catalogs

A catalog gets formally signed off the same way any artifact does — but with one extra requirement: the sign-off must explicitly reference the catalog version *and* the validation steps completed at that version. A row in `sign-off-log.md` for a catalog should look something like:

> "[Reviewer] approved workpaper-types.md v1.0 covering 23 variants, after validation steps 1–5 completed on [date]. Conditions: [any]."

Without that, it's not a defensible sign-off — it's just a thumbs-up on a document of unknown completeness.
