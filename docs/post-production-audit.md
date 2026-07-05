# Post-Production Audit
*(read in pre-production)*

Adapted and extended from Guadalupe Lareo's "Post-Production Audit (Read in
Pre-Production)". Reorganized into topical sections with a decision-timing
dimension, and extended with technical pipeline, delivery, legal/AI, and
archive coverage — the omissions that become expensive when discovered after
production.

**Timing tags:** [G1] decide before greenlight · [G2] lock before principal
photography · [P] monitor during production · [PL] verify at picture lock.
Dual tags ([G2→PL]) mark items that are planned early and re-verified at lock.

**How to read it:** each phase has one owner and one verb — Gate 1 **decides**
(producer + writer/director), Gate 2 **locks** (line producer + post supervisor),
Phase P **watches** (post supervisor + editor, weekly), Gate PL **verifies**
(post supervisor). Decisions live at the gate where they are cheapest to make.

## 1. Schedule & Delivery Strategy

**Deadlines & schedule integrity**
- [ ] [G1] Is the post schedule built from the actual work, or backward from an untested release date?
- [ ] [G2] Are editing, sound, and VFX on aligned timelines?
- [ ] [G2] Is there a schedule buffer, or does everything have to go perfectly?
- [ ] [G2→PL] Is there enough time after picture lock for music, mix, grade, and QC?

**Versions & international delivery**
- [ ] [G1] Are festival/distributor deliverables defined? (they drive the whole back half of the schedule)
- [ ] [G2→PL] Are all required versions (theatrical, broadcast, international, airline) accounted for?
- [ ] [G2] International deliverables spec'd: textless masters, M&E (music & effects) mix, split/stem audio, dubbing-ready materials?
- [ ] [PL] Textless elements actually captured or generated for every shot carrying titles or graphics?

**Mastering formats & platform specifications**
- [ ] [G1] Is the release strategy known well enough to plan mastering formats — DCP for theatrical, IMF for streaming, broadcast masters — and who makes them?
- [ ] [G1] Are target streaming platforms' technical specs known **before** camera and pipeline choices? (approved camera lists, capture codec minimums, HDR requirements)
- [ ] [G2] IMF/DCP creation budgeted, with vendor or tooling identified and a QC pass included?
- [ ] [G2→PL] Platform QC specs (loudness, photosensitivity, subtitle formats, metadata) built into finishing and QC — not discovered at delivery rejection?

**Accessibility**
- [ ] [G2] Accessibility deliverables scoped explicitly — closed captions, SDH, audio description — with vendor, cost, and lead time, not lumped as "subtitles later"?
- [ ] [G2→PL] Subtitles, dubbing, captions/SDH, and audio description planned per delivery language and territory — not last-minute add-ons?
- [ ] [PL] Caption/SDH/AD production scheduled against the locked cut, with the script/dialogue list it depends on?

**Review cycles**
- [ ] [G2] Is time for studio or financier reviews built into the schedule?

## 2. Technical Pipeline & Media

**Camera tests & color management**
- [ ] [G2] Camera test shot and pushed through the entire real pipeline — dailies, editorial, VFX roundtrip, grade, deliverable — before day one, at the actual format, codec, and frame rate?
- [ ] [G2] Color management defined end-to-end: working color space (e.g., ACES or Resolve color-managed), on-set monitoring LUTs matching dailies and editorial, and the same transforms arriving in finishing?
- [ ] [PL] Verify: the LUTs/looks editorial cut against match what finishing applies — no "it looked different in the offline" surprises?

**Frame rate & mixed formats**
- [ ] [G1] Is the project frame rate chosen against delivery requirements — not the camera default — and known to every department?
- [ ] [G2] Mixed-format sources identified (drones, phones, action cams, archival, screen recordings) with a conversion/retime policy before they hit the timeline?

**Dailies, metadata & naming**
- [ ] [G2] Is there a confirmed finishing pipeline (online edit, color grade, deliverables)?
- [ ] [G2] Dailies workflow defined: who processes, proxy specs, turnaround, who receives what?
- [ ] [G2] Naming, timecode, and audio sync standards agreed across camera, sound, editorial, VFX?
- [ ] [G2] Metadata plan: camera metadata, scene/take/slate, and sound reports flowing into editorial and staying searchable through finishing?

**Backup & storage**
- [ ] [G2] Backup policy locked: 3-2-1 copies, checksum verification, a named data owner?
- [ ] [G2] Storage projected from the expected shoot ratio, with headroom?
- [ ] [P] Are backups verified and dailies keeping pace with the shoot — or is a backlog building?

**Cloud collaboration & remote editorial**
- [ ] [G2] If editorial is remote or distributed: collaboration platform chosen, proxy streaming/sync workflow tested, and project sharing (e.g., Resolve collaborative projects / cloud libraries) proven with real media before the shoot?
- [ ] [G2] Review-and-approval tooling defined — frame-accurate notes tied to timecode, not screen recordings over chat?

**Security & watermarking**
- [ ] [G2] Content security requirements known (studio/TPN obligations, NDAs) and access control defined for media, project files, and review links?
- [ ] [P] Screeners and review links watermarked and access-logged — leaked-cut risk actively managed, not assumed away?

**Version control**
- [ ] [G2] Version discipline defined before the first cut: one naming scheme for timeline/cut versions, VFX shot versions, and grade versions that every department uses?
- [ ] [P] Change lists produced for every cut-to-cut revision, so sound, VFX, and color are always conforming to the same reference?

**Picture lock & conform**
- [ ] [P] Is footage conforming cleanly as it arrives (spot-check a real scene through finishing) rather than waiting for lock to find out?
- [ ] [PL] Conform/roundtrip validated: locked sequence travels NLE → finishing (AAF/XML/EDL, agreed handles) and relinks frame-accurately?
- [ ] [PL] All media in the locked cut online at source resolution — no offline clips, proxies, or temp media in the timeline?
- [ ] [PL] Turnover packages accepted by each downstream department (sound, music, VFX, color), including a change-list procedure for post-lock revisions?

**Archive & LTO**
- [ ] [G2] Archive plan budgeted from the start: what gets archived (camera originals, project files, graded masters, deliverables), on what medium (LTO, cloud), retained how long, owned by whom?
- [ ] [PL] Archive execution scheduled as a deliverable after final delivery — not left to whoever still has the drives?

## 3. VFX Planning

**Shot count**
- [ ] [G1] How many VFX shots are there, and have they actually been counted?
- [ ] [P] Is the shot count holding, or creeping past the greenlight number?

**Invisible VFX**
- [ ] [G1] Does the script require invisible VFX for period, futuristic, or world-building elements?
- [ ] [G2] Are locations requiring heavy clean-up or set extension identified and planned?

**Practical vs digital**
- [ ] [G1] Are any hero shots driving unnecessary cost?
- [ ] [G1] Could production design or in-camera practical effects solve problems currently assigned to VFX?
- [ ] [G1] Are there scenes with digital doubles, de-aging, or face replacement?

**Pipeline**
- [ ] [G2] VFX turnover workflow defined: how plates get pulled and delivered, and the color pipeline (LUTs/CDLs, color space) vendors must work in?

**Supervision**
- [ ] [G2] Are green screen or volume scenes properly budgeted for on-set VFX supervision?

## 4. Sound Strategy

**Recording specifications**
- [ ] [G2] Audio recording specs locked: sample rate and bit depth, track layout and iso tracks, timecode sync between recorder and cameras, and sound report format editorial can actually use?

**Difficult locations**
- [ ] [G2] How many scenes are in locations with uncontrollable background noise?
- [ ] [G2] Any scenes in moving vehicles, near water, or outdoors in wind?

**Dialogue**
- [ ] [G2] Scenes where actors are masked, turned away, or obscured?
- [ ] [G2] Overlapping dialogue that will be difficult to isolate and clean?

**ADR risks**
- [ ] [G2] Performances that would be difficult to recreate in ADR?
- [ ] [P] Is location sound coming in clean, or is the ADR list silently growing?

**Music**
- [ ] [G1] Is original music/score required and budgeted — or assumed to be library?
- [ ] [G2] Music clearances started early? (a picture-lock blocker if they start late)
- [ ] [P] Are clearances progressing, or stalled?
- [ ] [PL] Clearances resolved — nothing in the cut that can't be licensed?

**Sound design**
- [ ] [G1] Does any scene rely on a sound effect needing custom design rather than library pulls?
- [ ] [G2] Crowd scenes / walla that will need to be built entirely in post?
- [ ] [G2] Sequences where silence is doing dramatic work? (protect the location sound plan)

## 5. Editorial Risk Assessment

**Coverage**
- [ ] [G2] Is the editor attached early enough to give input on what coverage is actually needed on set?
- [ ] [P] How many planned cuts depend on a specific piece of coverage that hasn't been shot yet?
- [ ] [P] Are scenes where the script relies on the edit for heavy emotional lifting actually getting the coverage the editor needs?

**Structural risks**
- [ ] [G1] Are any scenes so long they'll almost certainly need cutting down?
- [ ] [G1] Could parallel storylines be simplified to reduce assembly complexity?

**Exposition**
- [ ] [G1] Are there scenes that exist only to set up information the audience could receive another way?
- [ ] [PL] Is any act so front-loaded with exposition that the edit struggles to hold pace? (last cheap moment to fix it)

**Flashbacks**
- [ ] [G1] Could flashbacks or non-linear sequences be straightened out without losing narrative impact?

**Contingency plans**
- [ ] [PL] Is there a contingency plan if a key scene doesn't work in the cut?
- [ ] [P] Is temp material in the cut (temp VFX, temp/unlicensed music) being logged, so nothing untracked survives to picture lock?

## 6. Legal, Rights & AI

**Legal review & clearances**
- [ ] [G1] Is the rights budget realistic for everything the film needs: music, archival footage, artwork, trademarks and brands appearing on screen?
- [ ] [G2] Clearance procedure defined for what the camera will see — artwork, posters, logos, products, storefronts — and E&O insurance requirements known?
- [ ] [P] Clearance log maintained as scenes are shot, so nothing unlicensed accumulates silently in the cut?
- [ ] [PL] Legal review of the locked cut complete: every music cue, piece of artwork, and trademark cleared, replaced, or cleared for fair use in writing?

**AI usage policy**
- [ ] [G1] AI usage policy set before anyone uses a tool: what's allowed (transcription, upscaling, cleanup, temp voice), what requires disclosure, what's prohibited?
- [ ] [G2] Union/guild and platform AI disclosure requirements checked — several deliverable specs now require declaring AI use?
- [ ] [G2] Data policy for AI tools: is footage or audio permitted to leave controlled storage into third-party cloud AI services, and under what terms?

## 7. Final Green-Light Review
*Answered in one sitting, drawing on sections 1–6. These require written answers, not checkboxes.*

- **What can be solved now instead of in post?** — pull every [G1] item answered "yes" in sections 3–6: script fixes, practical-for-digital swaps, structural simplifications, rights problems avoidable on the page.
- **What are the biggest schedule risks?** — from sections 1–2: untested release date, missing buffer, late clearances, accessibility and mastering lead times, unplanned review cycles.
- **What are the biggest budget risks?** — from sections 1, 3, 4, 6: uncounted VFX shots, hero shots, ADR exposure, custom sound/score assumed to be cheap, rights and clearances, IMF/DCP mastering, archive left unbudgeted.
- **What absolutely must be locked before shooting?** — the [G2] list, verbatim: camera/pipeline tests, color management, media workflow, sound specs and mitigation plan, VFX supervision, editor attachment, security and version discipline, AI and clearance policy.
