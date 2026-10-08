# VISUAL_REVIEW — batch p, part t0_p2a5e5dd8fc

Author's own review (never an expert/human grade). Drawings were read with the image-read tool.

## Draft d1 — drawing `batchp/out/t0_p2a5e5dd8fc_draft_d1.png` (check: 2-D PASS, 49 blocks)

- Local feature isolation: region 0 (pocket, occupied 0–0.388, the runner's level loop 7) has an inner
  O-grid and a reverse O-grid box [0,2.54]x[0,2.671] in region 3. The box corners land on the outline,
  so no line spreads beyond region 3. Hole 2 sits inside the region-2 round: there is a radial cut at
  135 deg to the round and a 45-deg box (T2/K2/L2) on its open sides. Slot 1 and slot 3 each have a box ring.
  Slot 1's ring is split at y=3.937, the notch-top line, on both sides, which is also its own mid-height.
  Slot 3's left ring is split where the notch lines y=2.671 and y=3.937 arrive. Every level-loop corner
  is matched on both sides.
- Ring scale: slot 1's box has margins of 0.20–0.28, near the slot's 0.23 corner radius (good). Slot 3's
  box is wider: 0.76 left, 0.60 right (the wall), 0.80 top and 1.25 bottom. The **circle (loop 4) has no
  near-scale ring**. Its 6 radial cuts fan 1.5–2.4 units out to the cell nodes (blocks 20, 24, 25).
  That is the "small hole alone with long fans" pattern from rule 4, so it is oversized.
- Symmetry and transitions: the hole-in-round ring is symmetric about the 135-deg diagonal, and the
  pocket box is symmetric about the pocket. The circle and slot 1 overlap in x, so no vertical line
  can separate them. The circle therefore sits in the cell [3.537,6.74]x[0,2.671], and its ring
  connects to that cell's corners.
- Diagonal fans and wedges: circle blocks 24 and 25 (toward the notch corner and n0) are long fans.
  Slot-3 block 42 has a 28-deg corner at g1, and block 46 has a 33-deg corner at f1. Both come from
  the slot-3 box bottom sitting on the circle-centre line y=1.166.
- Unnecessary subdivisions: the strips at x 3.177–3.537 are forced. The base is wider than regions 2/3
  by 0.36 there, and the notch corners need cuts at block corners. Column x 6.74–7.6 carries slot-3's
  box side.
- Decision: **revise before submitting** — add a near-scale ring around the circle (draft d2).

## Draft d2 = rev1 — drawing `batchp/out/t0_p2a5e5dd8fc_draft_d2.png` (check: 2-D PASS, 57 blocks)

- Change: 7 blocks of ring around the circle out to an offset polygon at radius 0.85 (thickness 0.39,
  about the hole radius). One more radial goes straight down to the wall (cb). Every radial continues
  on one straight line to its cell node (rule 7). The outer blocks now act as the background
  transition, and their worst forecast element is unchanged (0.54).
- Isolation: the circle now has "its own ring of blocks about its own size, then larger blocks
  outward" (rule 4). The other features are as in d1.
- Remaining tradeoffs: the heptagon is irregular because its radials follow the cell nodes. The
  outer blocks still slant toward the notch corner (nc) and n0. The 28-deg corner at g1 and the 33-deg
  corners at n0 and f1 remain (min sine 0.475; edge-ratio forecast 6.2 against a limit of 50).
- Decision: **submit as rev1**. The layout is coherent and feature-aligned, and the remaining slants
  follow from the circle and slot-1 overlap. If the full run refuses, the reasons decide the next step.

## rev1 after the full run — drawing `batchp/out/t0_p2a5e5dd8fc_rev1.png`

- The run reproduced the d2 drawing exactly: 57 drawn blocks, 0 filled. The title line reads 2-D PASS
  sine 0.4754 | 3-D strict True stable True | SJ 0.4754/0.4754 | block True | occupancy True | COUNTED True.
- No numerical repair was applied, and the drawing shows no change in structure. The minimum SJ
  (0.4754) equals the 2-D min sine. That points to the 28-deg corner at g1 (slot-3 right ring block)
  as the limiting element. A gentler corner there would require moving the slot-3 box bottom off the
  circle-centre line y=1.166, which would break the circle's symmetric radial split.
- Decision: **stop** at this first counted pass, as the brief directs. The remaining tradeoffs are
  recorded in FINAL_REPORT.md.
