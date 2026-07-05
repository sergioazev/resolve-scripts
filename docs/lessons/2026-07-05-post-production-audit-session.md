# Session Reflection — Post-Production Audit Checklist (2026-07-05)

Reflection on the working session that evolved Guadalupe Lareo's department-organized
"Post-Production Audit (Read in Pre-Production)" checklist (36 questions) into a
48-item, dual-axis operational document: five topical sections (Schedule & Delivery
Strategy, VFX Planning, Sound Strategy, Editorial Risk Assessment, Final Green-Light
Review) with decision-timing tags on every item ([G1] decide before greenlight,
[G2] lock before shooting, [P] monitor during production, [PL] verify at picture lock).

---

## Part 1 — Post-production planning knowledge

### 1. Post-production overruns are born in pre-production; place each decision where it is cheapest.
The biggest post costs (VFX scope, ADR volume, structural re-edits) are set on the page
and on the shooting plan, not in the edit suite. The restructure operationalized this:
every question sits at the earliest gate where answering it is still cheap — expensive
work scoped before greenlight, pipeline and risk mitigation locked before day one,
drift merely watched during production, everything re-verified before picture lock
(the most expensive commitment in post).

### 2. Media management and conform are the blind spots of department-oriented audits — and the ones that matter most in a Resolve-based finishing workflow.
The original 36 questions covered schedule, VFX, sound, and editorial but had zero
coverage of the technical spine: codec/format/frame-rate pipeline testing end-to-end,
dailies workflow and proxy specs, 3-2-1 backup with checksums and a named data owner,
naming/timecode/sync standards across departments, storage projected from shoot ratio,
and VFX turnover + color pipeline (LUTs/CDLs). Rationale for all 12 added items:
pipeline mistakes are cheap in a test, brutal mid-shoot; a conform failure discovered
after lock costs weeks instead of hours.

### 3. Picture lock is a verification gate with pass criteria, not just a milestone.
Concrete checks: frame-accurate roundtrip validation (AAF/XML/EDL with agreed handles);
all media online at source resolution with no offline, proxy, or temp clips in the
locked timeline; turnover packages accepted by each downstream department, including
an agreed change-list procedure for post-lock revisions. The supporting practice during
production is logging all temp media (temp VFX, unlicensed temp music) so nothing
untracked survives to lock.

### 4. Planning items and verification items are the same items at two different times.
Finishing pipeline, delivery versions, clearances, and schedule buffer are legitimately
locked early (G2) and re-verified at picture lock (PL). Making this explicit as
plan-then-verify ([G2→PL]) is more honest than picking one home per question — treating
plan and verify as one checkbox is how locked decisions silently drift during a shoot.

## Part 2 — Operational-document design principles

### 5. Structure a working checklist along the axis the user acts on, not the axis the content is categorized by.
Department grouping (Timeline / VFX / Sound / Editorial) is how the knowledge is
organized; decision timing (greenlight → pre-shoot lock → production → picture lock)
is how a producer actually works. When both axes carry real information, keep the
topical sections as the primary structure and preserve timing as tags on every item —
a dual-axis document instead of a forced choice.

### 6. Every phase needs one owner and one verb.
Each gate has a named accountable role (producer + writer/director; line producer +
post supervisor; post supervisor + editor, weekly; post supervisor) and a single
operative verb (DECIDE, LOCK, WATCH, VERIFY). This converts a list of questions into
an accountability structure: who runs the meeting, what "done" means at that phase,
and which items are continuous monitoring rather than one-time gates.

### 7. End with a synthesis section that forces written answers, not checkboxes.
Sections 1–4 are analysis; the Final Green-Light Review forces synthesis — free-text
answers to roll-up questions ("What can be solved now instead of in post? Biggest
schedule/budget risks? What must be locked before shooting?"), each drawing
mechanically on the tagged items (e.g., "what must be locked" is the [G2] list
verbatim). This is what turns the audit from reference material into a document that
cannot be completed by ticking boxes.

## Part 3 — Collaboration lessons (how these sessions work)

### 8. Terse directives are full instructions; execute, don't interrogate.
Sergio drives with minimal commands — "analisar" on an uploaded photo, "fold those in"
referencing gaps named two turns earlier — and expects the context to be carried
forward and acted on completely. Produce the full work product and let him redirect.

### 9. Substantive additions are welcome, but he owns the structure — propose, then yield.
He accepted the gap analysis and the first restructure, then proposed his own 5-section
layout and expected it adopted as the primary axis. The winning move is synthesis, not
defense: keep his structure on top and preserve prior value as a secondary dimension
(the timing tags) rather than arguing for the previous version.

### 10. Structure and workflow-fit matter more than content volume.
His only pushback across four exchanges was structural ("forces the reader to jump
between departments"); he never disputed a single question's content across 48 items.
Organize outputs by when a decision is made, who owns it, and what verb applies —
not by topic taxonomy alone.

### 11. Mirror his language turn-by-turn.
He opens in Portuguese and switches to English for detailed technical work. Match the
language of his most recent message rather than fixing one language per session;
domain vocabulary (picture lock, conform, AAF/XML/EDL, turnover) stays in English.

### 12. Artifacts land in the repo only when he says so.
The commit offer for the checklist was made twice and ignored twice while iteration
continued; the repo's own description ("scripts que rodam aprovados em uso") signals
only vetted material belongs here. Iterate in-conversation; one offer to store is
enough.

## Follow-up candidates

- The Gate 4 / Phase 3 items are natural candidates for Resolve automation scripts in
  this repo: conform/relink validation, offline-and-proxy media detection in a locked
  timeline, temp-media (temp VFX / unlicensed music) flagging, dailies/backup checksum
  verification.
- The finished checklist itself (48 items, 5 sections, timing tags) has not been
  committed; it lives in the session transcript and can be stored as
  `docs/post-production-audit.md` on request.
