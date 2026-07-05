# CLAUDE.md

Operational DaVinci Resolve scripts for Argonautas — only approved, in-use scripts
belong in this repo ("scripts que rodam aprovados em uso").

## Working with Sergio

- Terse directives ("analisar", "fold those in") are complete instructions: carry the
  conversation context forward and deliver the full work product without clarifying
  questions; he redirects if needed.
- Mirror the language of his most recent message — Portuguese or English, turn by
  turn. Post-production vocabulary (picture lock, conform, AAF/XML/EDL, turnover)
  stays in English either way.
- He owns document structure. Propose improvements once; when he supplies his own
  structure, adopt it as the primary axis and fold prior value in as a secondary
  dimension rather than defending the earlier version.
- Frame answers through the producer/line-producer lens: decision timing
  (before greenlight → lock before shooting → monitor during production → verify at
  picture lock), a named owner and a single verb per phase.
- Don't commit artifacts preemptively — offer once; files land in the repo only when
  he asks.

## Key documents

- `docs/argo-lab-procedures/` — the Argo Lab Procedures manual: workflow
  standards, department audits, 5×5 risk method, budget impact tables, case
  studies, templates, and one-page role checklists. The audit asks questions;
  the manual gives Argonautas' standard answers. `[DECIDE]` marks unset house
  standards; `[CALIBRATE]` marks rule-of-thumb figures awaiting real data.
- `docs/post-production-audit.md` — the intake audit, operationalized by the
  `post-production-audit` skill.
- Scripts in this repo automate procedures in the manual; each script's
  documentation must name the procedure it serves.

## Session lessons

Detailed reflections are stored in `docs/lessons/` (one file per session).
See `docs/lessons/2026-07-05-post-production-audit-session.md` for post-production
planning principles, checklist design lessons, and Resolve automation candidates
(conform/relink validation, offline-media detection, temp-media flagging, backup
checksum verification).
