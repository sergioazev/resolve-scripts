---
name: post-production-audit
description: Run the post-production audit on a project in pre-production. Use when starting pre-production on a new project, when asked to audit a script/schedule/budget for post-production risks, or when asked what must be decided before greenlight, locked before shooting, monitored during production, or verified at picture lock.
---

# Post-Production Audit

Operationalizes the checklist in `docs/post-production-audit.md` (read it first —
it is the source of truth for the items, their section grouping, and their
timing tags). Do not paraphrase items from memory; quote them from the document.

## Timing model

Every item carries a tag for when it fires:

- **[G1]** decide before greenlight — owner: producer + writer/director, verb: DECIDE
- **[G2]** lock before principal photography — owner: line producer + post supervisor, verb: LOCK
- **[P]** monitor during production — owner: post supervisor + editor, weekly, verb: WATCH
- **[PL]** verify at picture lock — owner: post supervisor, verb: VERIFY
- **[G2→PL]** planned at G2, re-verified at PL — both gates, explicitly

## Procedure

1. **Establish the project's phase.** Ask (or infer from the material provided)
   where the project stands: pre-greenlight, prepping to shoot, in production,
   or approaching picture lock. The phase decides which tags are actionable now,
   which are already overdue, and which are premature.

2. **Ingest whatever material exists** — script, schedule, budget, shot list,
   deliverables spec. For each checklist item, answer it from the material where
   possible; only ask the user for what can't be inferred. Batch questions by
   section, don't drip them one at a time.

3. **Walk the audit sections** (Schedule & Delivery Strategy; Technical
   Pipeline & Media; VFX Planning; Sound Strategy; Editorial Risk Assessment;
   Legal, Rights & AI) marking each item: OK, AT RISK, UNANSWERED, or N/A —
   with a one-line justification anchored in the material, never a bare
   checkbox.

4. **On a phase-filtered request** ("what must be locked before shooting?",
   "o que precisa estar travado antes de filmar?"), return exactly the items
   with that tag, grouped by section, with their current status.

5. **Always finish with the Final Green-Light Review** (the document's last
   section). This is the deliverable: four written answers, not checkboxes:
   - What can be solved now instead of in post? (the [G1] items flagged AT RISK)
   - Biggest schedule risks? (schedule, delivery, accessibility/mastering lead times)
   - Biggest budget risks? (VFX, ADR, rights/clearances, mastering, archive)
   - What absolutely must be locked before shooting? (the [G2] list with status)

6. **Flag Resolve automation candidates.** When [P] or [PL] items are AT RISK or
   UNANSWERED, note which are scriptable in DaVinci Resolve and could live in
   this repo: conform/relink validation, offline/proxy media detection in a
   locked timeline, temp-media flagging (temp VFX, unlicensed temp music),
   dailies/backup checksum verification.

## Output conventions

- Mirror the user's language (Portuguese or English); keep domain terms
  (picture lock, conform, AAF/XML/EDL, turnover, walla) in English either way.
- Organize output by decision timing and ownership, not by department taxonomy.
- Overdue items (tag earlier than the project's current phase) go first,
  labeled as such — those are the findings that matter most.
