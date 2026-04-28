# Extraction Prompts — Procedures Manual → Workflow Artifacts

Use these prompts in ChatGPT (or any LLM) to extract structured facts from your procedures manual without sharing verbatim content. Paste the prompt, then paste the relevant section.

## Before you start — redaction checklist

Before pasting any manual section into an LLM, strip or replace:

- Company name and any subsidiary/brand names
- Proprietary system names (Archer, specific internal tools) — replace with "the current GRC system"
- Specific employee names — replace with role titles
- Department codes, cost center IDs, org unit labels
- Policy numbers, manual section numbers, document IDs
- Any content your company classifies as confidential beyond what LLM use is approved for

Role titles (Auditor, Team Leader, Audit Leader, PGA, CAE) are already generic and safe.

---

## Prompt 1 — Extract activities for a phase

Use for: filling in the activity list of a phase (e.g., complete Kickoff/Planning, confirm Fieldwork, etc.)

```
You are helping me extract a structured activity list from an audit procedures manual.
I will paste a section below.

Please produce:
1. A bulleted list of discrete activities (verb + object, max 10 words each)
2. For each activity, the role that performs it — use ONLY generic role titles:
   auditor, team leader, audit leader, PGA, CAE, auditee management, process owner
3. Any approval or review step listed separately as a "gate" with its approver

Strict rules:
- Do NOT include company names, proprietary system names, or person names
- Do NOT reproduce any phrase longer than 8 words verbatim from the source
- Paraphrase everything

Return in this format:
## Activities
- [verb] [object] — role: [generic]
## Gates
- [gate name]: [what is approved] — approver: [generic role]

Section to extract from:
[paste your redacted section]
```

---

## Prompt 2 — Extract a checklist

Use for: the Fieldwork admin checklist, closeout checklist, any procedural checklist.

```
You are helping me extract a structured checklist from an audit procedures manual.
I will paste a section below.

Please produce a plain numbered list of checklist items. Each item should:
- Be one sentence, imperative form (e.g., "Archive workpapers")
- Be 10 words or fewer
- Be paraphrased, not copied

Do NOT include company names, proprietary system names, person names, or any verbatim phrase longer than 8 words.

Section to extract from:
[paste your redacted section]
```

---

## Prompt 3 — Extract approval authority rules

Use for: populating the RACI from your approval matrix.

```
You are helping me extract approval authority rules from an audit document.
I will paste a section below.

Please produce a table with these columns:
- Decision or Document (what is being approved)
- Approver (generic role only: auditor, team leader, audit leader, PGA, CAE)
- Trigger (when this approval is needed in the process)
- Conditions (escalation rules, risk-rating thresholds, etc., if any)

Strict rules:
- Generic role titles only
- No company names, system names, or person names
- Paraphrase; no verbatim phrase longer than 8 words

Section to extract from:
[paste your redacted section]
```

---

## Prompt 4 — Extract sequence / order of operations

Use for: confirming the Reporting phase sequence (or any process with ambiguous order).

```
You are helping me extract the order of operations in a process from an audit procedures manual.
I will paste a section below.

Please produce:
1. A numbered list of steps in the order they occur
2. For each step, note whether it is sequential (must happen after the prior step) or parallel (can happen concurrently)
3. Flag conditional branches (e.g., "if X then do Y")

Each step: 10 words or fewer, paraphrased. No verbatim phrases over 8 words. No company or system names.

Section to extract from:
[paste your redacted section]
```

---

## Prompt 5 — Cross-reference what we already have

Use for: checking our current draft narrative against the manual without exposing manual content.

```
I will paste two things:
(A) A draft workflow narrative I wrote
(B) A section from an audit procedures manual

Your job:
1. Tell me what activities, approvals, or roles in (B) are MISSING from (A)
2. Tell me what's in (A) that CONTRADICTS (B)
3. Tell me what's in (A) that (B) does not cover (neither confirms nor contradicts)

Rules for your output:
- Describe findings in generic terms only
- No verbatim quotes longer than 8 words from (B)
- No company names or system names

(A) Draft narrative:
[paste narrative.md content]

(B) Manual section:
[paste your redacted section]
```

---

## Bringing results back

After ChatGPT returns structured output:

1. **Skim it** — make sure it hasn't leaked a verbatim phrase or identifier despite the prompt rules.
2. **Paste the structured result** into the relevant artifact (narrative.md, decisions-log.md, raci.md).
3. **Note the source generically** in the decisions log (e.g., "Confirmed from procedures manual, Session 2") without revealing section references.

If ChatGPT does surface something surprising or contradictory, log it as an open question for verification rather than accepting blindly.
