# 5. Budget Impact Tables

What each failure mode costs when discovered late, versus what preventing it
costs at the right gate. All figures are industry rules of thumb
`[CALIBRATE: replace with Argonautas actuals as productions close — the risk
register's closed items (4.3.5) are the data source]`.

Multipliers reference the gate table in chapter 1.

| Failure mode | Cheap fix (gate) | Late discovery (gate) | Typical late cost | Audit item |
|---|---|---|---|---|
| Uncounted VFX shots | Breakdown + count (G1) | Shots surface in the edit (PL) | 10–50× the breakdown cost; budget line loses meaning | §3 shot count |
| Mixed frame rates / rogue formats | Conversion policy + pipeline test (G2) | Manual retime/reconform in online (PL) | Online budget can double — see case 6.3 | §2 frame rate & mixed formats |
| No/poor metadata | Naming + metadata plan (G2) | Search and relink by eye (P/PL) | Weeks of AE time; conform risk — see case 6.2 | §2 dailies, metadata & naming |
| Noisy-location dialogue | Sound scout + staging (G2) | ADR sessions + actor availability (PL) | ADR day per affected scene; performance loss | §4 difficult locations |
| Missing insert/coverage | Editor input on shot list (G2); pickup while dressed (P) | VFX patch or ADR restructure (PL) | 10× the pickup cost — see case 6.1 | §5 coverage |
| Titles baked in, no textless | Textless in turnover spec (G2) | Rebuild titles for international (after PL) | Re-online of every titled shot — see case 6.4 | §1 versions & international |
| Subtitles/accessibility ignored | Scoped with vendor + lead time (G2) | Rush against festival/platform date (after PL) | Rush fees; missed festival window — see case 6.4 | §1 accessibility |
| Platform spec unread | Spec check before camera choice (G1) | Master rejected at delivery QC | Re-grade/re-master cycle; release slip | §1 mastering & platform specs |
| Unlicensed temp music survives to lock | Temp-media log (P) | Re-cut or emergency license (after PL) | License premium or picture change post-lock | §5 contingency / §4 music |
| Uncleared artwork/trademark in frame | Clearance procedure (G2) | Legal flag at delivery; blur/replace in VFX | VFX cleanup per shot + legal review cycle | §6 legal review |
| Conform won't relink | Camera test + spot-check conform (G2/P) | Discovered at lock (PL) | Days-to-weeks of finishing time at facility rates | §2 picture lock & conform |
| No archive plan | Budgeted deliverable (G2) | Drives scattered after wrap | Restoration cost, or the material is simply gone | §2 archive & LTO |
| AI use undisclosed | Policy + disclosure check (G1/G2) | Platform declaration form at delivery | Deliverable rejected pending legal review | §6 AI usage policy |

## Reading the table

- **The prevention column is always a G1/G2 line item** — small, predictable,
  and budgetable. The late column is unbounded because it includes schedule
  damage, not just invoices.
- When pricing a mitigation in the risk register, quote both columns: what it
  costs now, what it costs at the late gate. That is the argument that wins
  the budget conversation.
- After each production closes, add a row (or update a figure) from the
  closed risk register. Figures with a production behind them lose the
  `[CALIBRATE]` mark.
