# 2. Workflow Design

Six pipelines, camera to archive. Each section states the flow, the house
standards (`[DECIDE]` where not yet set), the handoffs, and the verification
points. The audit items in `docs/post-production-audit.md` section 2 map onto
these pipelines; the templates in chapter 7 are their paperwork.

## 2.1 Camera pipeline

**Flow:** camera → cards → DIT offload (checksum) → 3-2-1 backup → dailies
(proxy + LUT) → editorial ingest.

**Standards:**
- Approved cameras and capture codecs: `[DECIDE: list per project tier; check
  target platform approved-camera lists first — see 5.x]`
- Project frame rate chosen against delivery requirements, never camera
  default. Mixed-format sources (drones, phones, archival) require a
  conversion/retime policy **before** they hit a timeline.
- Offload with checksum verification (xxHash/MD5), two independent copies on
  set plus one off-site: `[DECIDE: tooling — e.g., Silverstack, YoYotta — and
  who owns the data]`
- Proxy spec: `[DECIDE: codec/resolution — e.g., DNxHR LB or H.264 proxy —
  and whether Resolve generates them]`
- Naming and metadata per the Camera Metadata Sheet (template 7.8); scene/
  take/slate and camera metadata must survive into editorial and finishing.

**Verification:** camera test through the entire real pipeline (dailies →
editorial → VFX roundtrip → grade → deliverable) before day one. No exceptions.

## 2.2 Audio pipeline

**Flow:** recorder (iso tracks + mix) → sound reports → timecode sync with
camera → editorial → turnover to sound post → ADR/design/mix → M&E and stems.

**Standards:**
- Recording spec: `[DECIDE: sample rate/bit depth — typically 48 kHz/24-bit —
  track layout, iso track policy]`
- Timecode sync method between recorder and cameras locked at G2 and tested
  in the camera test.
- Sound reports in a format editorial can use directly: `[DECIDE: format]`
- ADR exposure tracked from dailies using the ADR Forecast (template 7.4).
- Every delivery needs M&E; the mix is built with M&E in mind from the start,
  not reverse-engineered after.

## 2.3 Editorial pipeline

**Flow:** proxy ingest → sync/organization → assembly → cuts (versioned) →
picture lock → turnover (AAF/XML/EDL with agreed handles) → conform.

**Standards:**
- NLE and project organization: `[DECIDE: Resolve-native or external NLE +
  Resolve finishing; bin structure; collaborative project settings]`
- Version discipline: one naming scheme for cuts, VFX shot versions, and
  grade versions, used by every department: `[DECIDE: scheme, e.g.,
  PROJ_EP_CUT_v###_YYYYMMDD]`
- Change lists for every cut-to-cut revision; sound, VFX, and color always
  conform to the same reference.
- Temp media (temp VFX, unlicensed temp music) logged from the first
  assembly so nothing untracked survives to lock.
- Remote/distributed editorial: `[DECIDE: collaboration platform, proxy
  streaming, review tooling with frame-accurate notes]`

**Verification:** spot-check conform on a real scene during production; full
roundtrip validation at picture lock (Picture Lock Report, template 7.1).

## 2.4 VFX pipeline

**Flow:** shot count (G1) → breakdown → plate pulls (with color pipeline) →
vendor → shot versions → final delivery → conform back into finishing.

**Standards:**
- Shots counted before greenlight; count re-checked weekly against drift.
- Turnover spec: how plates are pulled, delivered format, handles, and the
  color pipeline vendors must work in (LUTs/CDLs, color space).
- Shot tracking via the VFX Shot Log (template 7.2); every shot has a status
  and a version, and finals are checksummed on receipt.
- On-set VFX supervision budgeted for green screen / volume days.

## 2.5 Color pipeline

**Flow:** on-set monitoring LUTs → dailies color → editorial (same looks) →
conform → grade → deliverables per master format.

**Standards:**
- Color management end-to-end: `[DECIDE: ACES version or Resolve Color
  Managed; working/timeline color space; output transforms per deliverable]`
- The LUTs editorial cuts against must be the same transforms finishing
  applies — documented in the Color Pipeline Sheet (template 7.7).
- HDR requirements checked against platform specs before the pipeline is
  locked, not at mastering.

**Verification:** at PL, confirm offline looks match finishing math — no
"it looked different in the offline."

## 2.6 Archive pipeline

**Flow:** final delivery accepted → collect (camera originals, project files,
graded masters, deliverables) → archive media → verification → catalog.

**Standards:**
- What is archived, on what medium, retained how long, owned by whom:
  `[DECIDE: LTO generation and/or cloud tier; retention policy; owner]`
- Archive is a budgeted deliverable scheduled at G2 — never left to whoever
  still has the drives.
- Every archive verified by checksum and logged in the Archive Verification
  Sheet (template 7.10) before working storage is released.
