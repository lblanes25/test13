# Beta Team Feedback Log

Tracks feedback from the beta audit team using Optro for live audits, including how each piece of feedback is dispositioned and how the loop is closed back with the team that gave it.

**Why this exists:** Beta users are giving free signal about what works in practice. Their feedback is high-value but degrades fast: if they don't see their input being used, they stop giving useful feedback. This log forces disposition + closing-the-loop on every item.

**Important principle:** Beta feedback can override prior design decisions. If the beta team finds something confusing in practice that we'd previously aligned on, that's a real signal — not a training problem to wave away. The disposition process below explicitly allows this and routes it through proper governance (re-version, re-approve).

---

## Feedback intake

Capture every piece of feedback received. Don't filter at intake — filter at disposition. A piece of feedback that turns out to be out of scope is still worth recording so we can show the beta team it was considered.

| ID | Date received | From (name + role) | Workflow / artifact | Type | Feedback summary | Source (verbal / email / meeting / form) |
|---|---|---|---|---|---|---|
| BF-001 | *(date)* | *(name, role)* | *(e.g., engagement lifecycle, control test workpaper)* | *(Defect / Design Q / Training Gap / Preference / Out of Scope)* | *(1-2 sentences, paraphrased)* | *(where it came from)* |

### Feedback type definitions

- **Defect** — the workflow as configured is not behaving as designed (system bug or misconfiguration)
- **Design Question** — the workflow is behaving as designed but the design itself isn't working in practice
- **Training Gap** — design is sound and behaving correctly; user didn't know how to use it (likely needs training material)
- **Preference** — user would prefer a different approach but the current design is functional and intentional
- **Out of Scope** — feedback is about something our team doesn't own (refer to PM, IT, methodology, etc.)

---

## Disposition

For each piece of feedback, decide what to do. Update as decisions are made.

| ID | Disposition | Rationale | Action owner | Re-version triggered? | Status |
|---|---|---|---|---|---|
| BF-001 | *(Action / Decline / Defer / Escalate / Refer)* | *(brief why)* | *(name)* | *(yes/no — if yes, link the change-log entry)* | *(Open / In Progress / Done / Closed-No-Action)* |

### Disposition options

- **Action** — change something (workflow design, training material, configuration). If a workflow change, this triggers `change-log.md` entry and likely re-approval.
- **Decline** — feedback acknowledged but no change will be made. Always requires a clear rationale because this is what beta users will see.
- **Defer** — change makes sense but not now (e.g., post-go-live). Logged in `known-limitations.md` if relevant.
- **Escalate** — disagreement on how to disposition or feedback exceeds team's authority. Goes to project sponsor per the standard escalation path.
- **Refer** — feedback is real but belongs to another team (PM, IT, methodology). Routes to the appropriate handoff file.

---

## Closing the loop

Beta users need to see that their feedback went somewhere. Every piece of feedback gets a closing-the-loop entry — even Decline outcomes (especially Decline outcomes, because those are where trust is lost).

| ID | Date loop closed | How (email / meeting / message in shared channel) | What was communicated back | Confirmation from feedback giver |
|---|---|---|---|---|
| BF-001 | *(date)* | *(channel)* | *(brief summary of what we told them)* | *(yes / no / partial)* |

### Templates for common closing-the-loop messages

**Action taken:**
> Thanks for the feedback on [topic]. We've changed [specific change] in [artifact] (now at version [X]). The change rolls out [when]. We appreciated this one — it caught [what it caught].

**Declined:**
> Thanks for raising [topic]. We considered it carefully and decided not to change the design because [specific rationale]. We know this isn't the answer you might have hoped for; the reason is [the tradeoff]. If you continue to find this an issue in practice, please raise it again — we may revisit if patterns emerge.

**Deferred:**
> Thanks for [topic]. We agree it makes sense but we're holding it for [post-go-live / phase 2 / when X is decided] because [reason]. It's logged at [reference] so it doesn't get lost.

**Referred:**
> Thanks for [topic]. This is actually owned by [team] — we've passed it along to [name] and they'll follow up. Cc'ing here for visibility.

---

## Patterns and trends

Periodically review the feedback log for patterns. A single piece of feedback is signal; multiple pieces on the same topic is loud signal. Update this section monthly or after each beta cohort.

| Pattern | Items | Implication | Action |
|---|---|---|---|
| *(populate as patterns emerge)* | *(BF-IDs)* | *(what the pattern suggests)* | *(what we're doing about it)* |

---

## Beta team trust check

Quick periodic gut-check on whether the beta team is still engaged. If feedback volume drops or the items being raised feel low-value, the team may have stopped trusting that feedback gets used. This is a leading indicator and worth noticing.

| Period | Feedback volume | Average days to disposition | Average days to close the loop | Notes / concerns |
|---|---|---|---|---|
| *(populate periodically)* | | | | |
