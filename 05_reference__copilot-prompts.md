# Copilot Prompts — Mining Outlook for Governance Evidence

Use these prompts in Microsoft Copilot (with Outlook access) to reconstruct governance history from your email archive. Each prompt targets one file in the project and returns structured output you can review and paste in.

## How to use these prompts

1. **Narrow the time window.** Copilot works better with "last 6 months" or "since January 2025" than with "all time."
2. **Run one prompt at a time.** Don't try to fill multiple files in one query.
3. **Review before you paste.** Copilot is good but not authoritative. Open the source emails it cites before treating anything as confirmed.
4. **Apply the defensibility criteria** (from `sign-off-log.md`) to everything you pull — if an entry doesn't meet them, flag it as "candidate" rather than "confirmed."

## Language conventions

Replace the bracketed placeholders with your specifics. Where prompts mention "the project," use the actual project name your organization uses (migration project, Optro rollout, etc.) so Copilot can filter reliably.

---

## Prompt 1 — Sign-off and approval history

Populates: `sign-off-log.md`

```
Search my Outlook for emails from the last [TIME WINDOW, e.g., 12 months] related to the [PROJECT NAME, e.g., "Archer to Optro migration"].

I'm looking for emails where someone approved, signed off on, or explicitly agreed to a workflow design, process document, approval matrix, RACI, or similar governance artifact related to this project.

For each relevant email, return a row in a table with these columns:
- Date (sent date of the approval email)
- Approver name
- Approver role (use generic roles where possible: methodology lead, audit leader, PGA, CAE, etc.)
- Artifact approved (name and version if mentioned)
- Lens they approved from (methodology / data / reporting / domain / other — infer from context if not explicit)
- Exact phrase they used to signal approval (quote the key line, not the whole email)
- Any conditions attached to the approval (e.g., "pending X," "subject to Y")
- Link or subject of the source email so I can verify

Only include emails where there is a clear approval statement. Exclude:
- Emails where someone said they'd "take a look" but didn't confirm
- Meeting invites or calendar items
- Emails forwarded without comment

If a thread contains discussion leading up to an approval, focus on the message that carries the approval itself.
```

### What to do with the output
Paste candidate rows into `sign-off-log.md`. For each, apply the defensibility criteria:
- ✅ Artifact and version referenced → treat as confirmed
- ⚠️ Ambiguous reference (e.g., "the workflow" without version) → mark as candidate and follow up with the approver to confirm which version

---

## Prompt 2 — Decisions made over email

Populates: `decisions-log.md`

```
Search my Outlook for emails from the last [TIME WINDOW] related to the [PROJECT NAME].

I'm looking for emails where a decision was made about how an audit workflow should work in the new system. Examples:
- "We decided that planning approval will route through PGA"
- "Let's consolidate these two approvals"
- "We agreed that reporting team reviews all workflows"

For each decision, return a row in a table with these columns:
- Date the decision was made (or the email confirming it)
- Topic / what was decided (one sentence, neutral framing)
- Who made or confirmed the decision (name + role)
- Other participants in the thread who appeared to agree
- Any dissenting views expressed in the thread
- Current status of the decision (still in effect? superseded? unclear?)
- Source email subject and date so I can verify

Exclude:
- Discussions without a clear resolution
- Tentative suggestions that weren't accepted
- Decisions about logistics (meeting times, document locations) — only process/design decisions

If the same decision appears in multiple threads, consolidate to one row but note all relevant thread references.
```

### What to do with the output
For each decision Copilot surfaces:
- If it matches a resolved item already in `decisions-log.md`, add the email reference as corroborating evidence.
- If it's a decision you didn't have captured, add it to the "Resolved" section of `decisions-log.md` with the email date and approver.
- If the status is unclear or the decision has been superseded, log both versions with a note on which governs now.

---

## Prompt 3 — Review feedback and disagreements

Populates: `review-comments-log.md`

```
Search my Outlook for emails from the last [TIME WINDOW] related to the [PROJECT NAME].

I'm looking for emails where someone gave feedback, raised concerns, asked questions, or disagreed about workflow designs, process documents, or approval models.

For each piece of feedback, return a row in a table with these columns:
- Date
- Reviewer name and role
- Artifact or topic the feedback was about
- Summary of the feedback (paraphrase, 1-2 sentences)
- Type of feedback: question / suggestion / concern / disagreement
- Whether the feedback was resolved in the same thread (yes / no / partially)
- If resolved, what the resolution was
- If not resolved, what the last status was
- Source email subject and date

Pay special attention to threads where two or more people disagreed — these are important for reconstructing governance history.

Exclude:
- Routine status updates without substantive feedback
- Purely logistical comments (schedule, format)
- Thank-you replies without content
```

### What to do with the output
- Paste rows into `review-comments-log.md` under the right status (Resolved, Open, Disagreement, etc.).
- For any unresolved disagreement, also add an entry to the "Escalations" section if it warrants escalation to the project sponsor.
- For resolved feedback that led to a material design change, cross-reference the relevant entry in `design-rationale.md` (and add one if missing).

---

## Prompt 4 — Design rationale from your own sent mail

Populates: `design-rationale.md`

Often the clearest explanations of *why* a design choice was made are in emails you wrote — explaining a recommendation to a stakeholder, defending a position, or summarizing a decision. This prompt mines your sent mail to pull that reasoning out.

```
Search my sent mail in Outlook from the last [TIME WINDOW] for emails I sent related to the [PROJECT NAME].

I'm looking for emails where I explained, recommended, or justified a design decision about an audit workflow. Examples:
- "We should keep this approval at the PGA level because..."
- "I recommend consolidating these two steps because..."
- "The reason we're treating these as a single phase is..."

For each relevant email, return a row in a table with these columns:
- Date
- Recipient(s) and their role(s) — generic where possible
- Topic / what was being decided
- The recommendation or position I took (paraphrase, 1-2 sentences)
- The reasoning I gave (paraphrase, 1-3 sentences)
- Alternatives I mentioned having considered, if any
- Whether the email led to a confirmed decision (yes / no / unclear from context)
- Source email subject and date

Exclude:
- Emails that just forwarded content without my own reasoning
- Logistical emails (scheduling, document locations)
- Emails where I only asked questions without proposing a position
```

### What to do with the output

For each row:
- If the rationale is sound and the decision still stands, paste it into `design-rationale.md` using the standard format. The "alternatives considered" column maps directly to the alternatives section of each entry.
- If a rationale was given but the decision later changed, log the original rationale anyway with a note: "Superseded by [later decision] — rationale retained for audit trail."
- If you find rationale for a decision you forgot you'd made, cross-check `decisions-log.md` and add the decision there if it's missing.

This prompt often turns up the highest-quality entries because *you* wrote them — the reasoning is articulated, not reconstructed. If a single email contains rationale for multiple decisions, split it into multiple rows.

---

## General guidance

### When Copilot over-claims
If Copilot returns something like "this email constitutes approval" when the email actually says "looks reasonable, let's discuss," treat that as a candidate only. Language matters. "Looks reasonable" is feedback, not approval.

### When Copilot misses context
Copilot sees emails but not the surrounding decisions made in meetings, Teams chats, or verbally. If an important decision seems to have no email trail, it was probably made outside email — note the gap in `decisions-log.md` and don't force an email citation that doesn't exist.

### Confidentiality reminder
The project artifacts are at procedures-manual confidentiality tier (see `CLAUDE.md` → Working boundaries). Copilot is an approved M365 tool with proper scope, but you should still avoid pasting Copilot's summaries of approval emails into unapproved channels.

### Building the history isn't one-shot
You may need to run each prompt multiple times with different time windows or keyword emphases as you recall specific threads. Treat it as iterative research, not a single batch pull.
