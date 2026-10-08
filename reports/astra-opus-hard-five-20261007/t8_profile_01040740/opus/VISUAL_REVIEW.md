# VISUAL_REVIEW — batch p, part t0_p36f0273496

Author's own review of my drawings (not an expert or human grade). Each entry names the draft/revision and the
drawing I read with the image tool.

Part (from the listing): rounded triangle; through holes loop 1 (r 0.59, inside the top-right round), loop 2
(r 0.66, 0.57 from the slanted right wall), loop 3 (r 0.69); region 0 = counterbore annulus round loop 3 (level loop 4,
r 1.24, occupied 0-0.25, lower than base); region 2 = rounded-rectangle BOSS (level loop 5, occupied 0-0.83, higher than
base); base region 1 occupied 0-0.41. No mirror line.

## draft v1 — batchp/out/t0_p36f0273496_draft_v1.png (check PASS, 31 blocks, min sine 0.372)
- Feature isolation: boss has its own O-grid (core + 4) inside the loop and a 0.6 box ring outside; counterbore has a
  6-sector annulus (region 0) and a 6-sector base ring; holes 1 and 2 each have a 4-block ring.
- Ring scale: counterbore ring is fanned to far corners below it (D on the left wall and bL): blocks 23 (21.8 deg
  wedge) and 25 (D:30) are long diagonal fans. Hole 2's enclosure (tR, bR, E, W7) is oversized; the cut to E is a long
  near-vertical fan, block 17 (E:22) and the bottom wedge 16.
- Transitions/symmetry: no mirror line on the part; boss locally symmetric.
- Decision: REVISE (not submitted). The wedges/fans below the counterbore and hole 2 are exactly the "long diagonal
  fans" the guidance warns about.

## draft v2 — batchp/out/t0_p36f0273496_draft_v2.png (check PASS, 36 blocks, min sine 0.417)
- Change: one horizontal line y=5.294 (counterbore box bottom, same 0.61 margin as its right side) carried straight
  from the left wall through the boss (core split in two) to the boss box's right side; counterbore gets a 5-sector
  ring with clean 45-degree diagonals to M and Wl; a single quad below the counterbore and one below hole 2 replace the
  wedges.
- Left side now reads as a proper box round the counterbore at feature scale. Boss gains 3 blocks (8 in region 2)
  only because the line serves both neighbours (rule 7: carried straight).
- Still weak: tR is a 7-way node; hole 2's left block has a 25-degree corner at tR; hole 2's wall block corner at the
  separator end W7 is 31 deg.
- Decision: try moving the separator's wall end (v3) before submitting.

## draft v3 = rev1 — batchp/out/t0_p36f0273496_draft_v3.png (check PASS, 36 blocks, min sine 0.417)
- Change from v2: separator from tR lands on the wall where both holes sit about 45 deg off the wall normal; G (below
  hole 2) moved so hole 2's wall-side block has 41/43-degree corners instead of 38/31.
- Local feature isolation: through holes 1-3 each ringed; counterbore annulus + box; boss O-grid in its own height
  region with a matching box ring; no level-loop crossing.
- Ring scale: counterbore and boss enclosures ~0.6 margin (feature scale). Hole 2's enclosure is still tall on the
  left (tR to Mr = 3.2) — tR is fixed by the boss box corner. Hole 1's ring is fanned to tR and W7 (blocks 19, 24
  share a long tR-W7 cut); acceptable as hole 1 sits in the top-right round (rule 2) but block 19 is a long sector.
- Symmetry: part has none; boss and counterbore locally symmetric.
- Long diagonals: tR-W7 separator (~3.6, needed to part holes 1 and 2), bowl diagonals bL-D and bR-E (45 deg, rule 6).
  The bottom bowl (block 15) is one block with the bottom round as its side (rule 9/10: fewest blocks).
- Remaining tradeoff: tR is a 7-valent node with a 25-degree corner (block 21) and 31 (block 24). I found no layout
  change that removes it without propagating extra lines through the boss/counterbore.
- Decision: SUBMIT as rev1 to get the frozen full-run quality/refinement numbers before further changes.

## rev1 after its full run — batchp/out/t0_p36f0273496_rev1.png (COUNTED True)
- Drawing matches draft v3; title line: 2-D PASS sine 0.4167, 3-D strict True, stable True, SJ 0.4167 / 0.4167
  (nominal / doubled density), block True, occupancy True. Mesh judge captured 36 of 36 sharp edges.
- The worst SJ (0.4167) equals the 2-D minimum corner sine. It sits at tR's 25-degree corner (block 21, hole 2's left ring block).
  Refinement left it unchanged. It is a layout corner, not a CAD-radius realization issue.
- No repair was made after the run (counted on the first revision), so the layout structure is unchanged.
- Result of the visual review: submitted v3 as rev1 and stopped at the first counted pass. Remaining tradeoffs:
  (1) tR is a 7-valent node with 25/31-degree corners; (2) hole 1's lower sector (block 19) and hole 2's top
  sector (block 24) share one long tR-W7 cut; (3) the boss region carries 8 blocks rather than 5, because the
  counterbore-box line is carried straight through it; (4) the bottom round is one bowl block (block 15) whose bottom
  side follows the whole round, which is the fewest-blocks choice.
