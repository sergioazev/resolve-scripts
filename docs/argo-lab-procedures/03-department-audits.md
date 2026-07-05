# 3. Department Audits

Six departments, each audited through the same six lenses: objectives,
responsibilities, warning signs, common mistakes, decision tree, real-world
example. The warning signs feed the weekly [P] review; the decision trees are
what the post supervisor actually walks when a sign fires.

## 3.1 Camera & DIT

**Objectives:** every frame shot arrives in editorial intact, named, backed
up, and looking the way the DP intended.

**Responsibilities:** offload with checksums; 3-2-1 backup; apply/record
monitoring LUTs; generate dailies to spec; camera reports and metadata sheets;
flag format deviations same-day.

**Warning signs:** offload backlog growing; checksum step "skipped to save
time"; a new camera/format appears on the truck; card reuse before backup
verification; LUTs changing mid-shoot without documentation.

**Common mistakes:** trusting a copy without verification; letting drone/
phone footage bypass the DIT cart; naming by hand instead of by convention;
one backup instead of three.

**Decision tree — unplanned format arrives on set:**
1. Can it be shot on an approved format instead? → do that.
2. No → run it through the pipeline test *today* (proxy, conform, grade).
3. Test fails → escalate to post supervisor before the material is depended on.
4. Test passes → document conversion policy, add to Camera Metadata Sheet.

**Example:** see case study 6.3 — mixed frame rates that doubled an online
budget because nobody ran step 2.

## 3.2 Sound

**Objectives:** dialogue usable without ADR wherever possible; everything
recorded to spec, synced, and reported; ADR exposure known weekly, not
discovered in the mix.

**Responsibilities:** recording spec compliance; iso tracks; timecode sync;
sound reports editorial can use; flag unusable-location risk before the
schedule locks; maintain the ADR Forecast.

**Warning signs:** locations added near water/traffic/HVAC without a sound
scout; costumes/masks covering mouths approved without sound consulted;
overlapping-dialogue scenes staged without isolation; sound reports arriving
late or not at all.

**Common mistakes:** assuming "we'll fix it in the mix"; not recording room
tone; treating walla as free; scheduling the mix before the ADR list exists.

**Decision tree — location flagged as sound-hostile:**
1. Can the scene move or the schedule shift to a quiet window? → do that.
2. No → can staging isolate the dialogue (blocking, lav strategy)? → plan it.
3. No → book ADR *now*: add actors' availability to the ADR Forecast, price it.
4. Performance is ADR-hostile (children, non-actors, emotional peak) →
   escalate: this scene's sound is a production problem, not a post problem.

**Example:** see case study 6.1 — the missing insert that forced ADR.

## 3.3 Editorial

**Objectives:** the cut is always conformable; every version is named and
change-listed; risks visible in dailies (coverage, performance, sync) are
reported while reshooting is still cheap.

**Responsibilities:** ingest/sync to convention; verify metadata arrived;
version discipline and change lists; temp-media log; coverage feedback to set;
turnover packages to spec.

**Warning signs:** editor cutting from files outside the project structure;
versions named "final_v2_REAL"; temp music multiplying with no log; a scene
that "doesn't cut" but nobody has told production while coverage is still
gettable.

**Common mistakes:** silent fixes that hide coverage problems until lock;
turnover without handles agreed; relying on the editor's memory as the change
list; letting picture lock drift ("locked except reel 3").

**Decision tree — scene doesn't cut:**
1. Is coverage still obtainable (location/actors available)? → request insert/
   pickup now, with a shot-specific list.
2. No → can restructure solve it (reorder, steal a reaction from another
   take)? → prototype in a branch version, show the director.
3. No → does it need VFX (split screen, morph) or ADR to bridge? → price both,
   add to risk register.
4. Nothing works → contingency plan: can the film live without the scene?
   Answer before lock, in writing.

## 3.4 VFX

**Objectives:** shot count matches greenlight; every shot has a version,
status, and a plate pulled to the correct color pipeline; finals conform
frame-accurately.

**Responsibilities:** breakdown and count; turnover spec compliance; vendor
tracking via VFX Shot Log; version control on shots; final QC on receipt.

**Warning signs:** "small" shots being added in dailies review without
entering the log; plates pulled from the offline instead of source; vendor
working in an unverified color space; count at week 4 exceeding count at
greenlight.

**Common mistakes:** VFX absorbing problems that production design or a
reshoot would solve cheaper; no handles on plates; approving shots on a
laptop screen; treating temp comps as final in the schedule.

**Decision tree — new shot requested after greenlight:**
1. Could set/practical/production design solve it before the company wraps
   the location? → cheaper, do that.
2. No → enter it in the log with cost estimate *before* approving. No shadow
   shots.
3. Cumulative drift > `[DECIDE: threshold, e.g., 10%]` of greenlight count →
   producer sign-off required, budget line revised.

## 3.5 Color & Finishing

**Objectives:** the locked cut conforms frame-accurately; the grade starts
from the same math the offline looked at; every deliverable comes out of one
managed pipeline.

**Responsibilities:** color management setup; conform and relink validation;
grade; deliverable renders per Delivery Matrix; QC pass per QC Report.

**Warning signs:** offline media in the conform; "we'll relink later"; LUTs
of unknown origin in the editorial project; deliverable specs arriving after
the grade started; QC scheduled with zero fix days.

**Common mistakes:** grading before conform is verified; one deliverable
cloned into another spec without re-QC; trusting the timeline instead of the
change list after a post-lock revision.

**Decision tree — conform doesn't relink:**
1. Isolate: media problem (offline/missing) or metadata problem (timecode/
   reel/name)? Run the relink validation script `[when it exists in this repo]`.
2. Media → pull from archive/backup; if the source never made it to storage,
   escalate immediately — that is a camera-pipeline failure, not a finishing
   task.
3. Metadata → repair against the Camera Metadata Sheet; document the mismatch
   cause so the next show doesn't repeat it.
4. More than `[DECIDE: e.g., 1%]` of events fail → stop, audit the whole
   timeline before touching the grade.

**Example:** see case study 6.2 — the documentary with no metadata.

## 3.6 Delivery & QC

**Objectives:** every contracted deliverable (versions, masters, accessibility,
paperwork) leaves on time and passes the recipient's QC the first time.

**Responsibilities:** Delivery Matrix ownership; platform/festival spec
compliance; textless and M&E existence; captions/SDH/AD production; QC and
fix cycle; archive handoff.

**Warning signs:** deliverable list still "being confirmed" during the grade;
titles baked into picture with no textless; no dialogue list for subtitling;
loudness/photosensitivity specs unread; delivery date and QC date the same day.

**Common mistakes:** treating accessibility as a subtitle export; assuming a
theatrical master converts to IMF for free; discovering platform camera
requirements after the shoot (see case 6.4 for the festival variant).

**Decision tree — new delivery target added late:**
1. Get the written spec first. No spec, no commitment.
2. Diff against existing masters: what already complies, what needs re-render,
   what needs re-grade or re-mix?
3. Anything requiring source we don't have (textless, stems, HDR) → price and
   schedule *before* accepting the date.
4. Update Delivery Matrix and risk register; nothing is delivered from memory.
