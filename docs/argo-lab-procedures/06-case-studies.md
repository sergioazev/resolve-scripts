# 6. Case Studies

Instructive failures, each traced to the audit item that would have caught it
and the procedure that now exists because of it. The four below are
anonymized/composite industry cases; replace or augment them with Argonautas
productions as the closed risk registers accumulate (4.3.5).

Format: situation → what happened → root cause → cost → the item that catches
it now.

## 6.1 The missing insert that forced ADR

**Situation.** A dialogue scene hinged on a practical detail — a hand
palming a key — that everyone assumed was covered. The shot list had no
insert; the editor wasn't attached yet during the shoot.

**What happened.** In the cut, the scene didn't read without the insert. The
location was struck. The workaround restructured the scene around a take
where the critical line fell off-camera — which meant replacing the line, and
the surrounding dialogue, in ADR to make the new geography work. One missing
5-minute insert became an ADR session with two actors, plus a day of editorial
restructuring.

**Root cause.** No editorial input on the shot list; no same-week assembly
feedback to set while a pickup cost nothing.

**Costs.** `[CALIBRATE]` — pickup at the time: trivial. Actual: ADR day,
actor availability negotiation, performance loss on an emotional scene.

**Caught now by:** audit §5 coverage — "editor attached early enough to give
input on coverage" [G2] and "cuts depending on coverage not yet shot" [P];
chapter 3.3 decision tree, step 1.

## 6.2 The documentary with no metadata

**Situation.** Three hundred hours of observational footage across two years,
multiple cameras and operators, offloaded by whoever was nearest a laptop.
No naming convention, no logs, no synced sound reports.

**What happened.** The edit stalled for months: material could only be found
by scrubbing. Transcription had to be bought for the entire corpus just to
locate scenes. At finishing, the conform failed repeatedly — duplicate clip
names across cards relinked to the wrong sources, and every failure had to be
eye-matched.

**Root cause.** No G2 media plan because "it's just a documentary" — the
exact projects with the highest shooting ratios are the ones that need the
metadata discipline most.

**Costs.** `[CALIBRATE]` — months of AE time, full-corpus transcription,
finishing overruns, and shots the film wanted but could not find.

**Caught now by:** audit §2 dailies, metadata & naming [G2]; storage
projected from shoot ratio [G2]; chapter 3.5 decision tree, step 3.

## 6.3 The feature that doubled its online budget over mixed frame rates

**Situation.** Principal photography at 24 fps on approved cameras. Along the
way: drone unit shooting 30 fps, a phone-shot flashback sequence at variable
frame rate, and archival at 25 fps and 29.97. All of it cut seamlessly into
the offline, because NLEs are forgiving.

**What happened.** The conform was not forgiving. Every non-24 clip needed a
retime decision — optical flow here, frame-blend there, nearest-frame for the
archival — made shot by shot, reviewed shot by shot, because the offline's
automatic conversions didn't match finishing's. The online, bid as days,
took weeks. Budget roughly doubled.

**Root cause.** No conversion/retime policy before rogue formats hit the
timeline; drone and phone material bypassed the DIT cart, so nobody ran the
pipeline test on them.

**Costs.** `[CALIBRATE]` — ~2× the online budget; grade start delayed.

**Caught now by:** audit §2 frame rate & mixed formats [G1]/[G2]; chapter 3.1
decision tree ("unplanned format arrives on set"); the camera test standard
in 2.1.

## 6.4 The festival version that subtitles made impossible

**Situation.** A festival premiere abroad, confirmed late. Subtitling was on
the deliverables list as one line: "subtitles — TBD."

**What happened.** Three discoveries in the same week: the titles and two
text-heavy graphics sequences were baked into the graded master with no
textless; there was no dialogue list, so the subtitler had to transcribe from
the mix; and the festival's DCP spec wanted burned-in subs positioned clear of
the baked-in lower-third graphics — which nobody could move. The version
missed the festival's technical deadline. The premiere slot survived only
because the festival granted an exception screening from a compromised master.

**Root cause.** Subtitles treated as an export, not a deliverable with
dependencies (textless, dialogue list, spec, lead time) that must exist
*before* picture lock.

**Costs.** `[CALIBRATE]` — emergency re-online of titled shots, rush
subtitling and transcription fees, a near-missed premiere.

**Caught now by:** audit §1 versions & international ("textless captured for
every titled shot" [PL]), accessibility scoped with vendor and lead time
[G2]; chapter 3.6 warning signs; Delivery Matrix (template 7.5) which has no
"TBD" state — every row has a spec, a source, and a date.
