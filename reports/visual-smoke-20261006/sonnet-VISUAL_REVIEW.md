# VISUAL_REVIEW.md — batch p, part t0_p336d70065d

## Draft d4 -> rev1 (drawing: out/t0_p336d70065d_draft_d4.png)
Earlier drafts d1-d3 failed `check` (d1: slot caps with 0-degree corners, wedge in boss ring; d2: B ring and one slot block folded; d3: fill refused asymmetric slot corners). d4 passes `check`.
- Feature isolation: holes A, B, C each have a 4-block ring; boss (region 0) has a 4-block outer ring plus the fill's own ring/core; slot (region 2) left to fill with 4 corners at 15/165/195/345 deg; pocket (region 3) drawn as 5 ring blocks round hole C. Level boundaries respected, no block crosses a loop.
- Ring scale: A ring is about 1.2 wide vs hole diameter 0.75 (a bit large on the right side, because its NE corner is shared with the boss ring). B ring is tight (0.07-0.1 clearance) because B sits 0.24 from the top wall and 0.4 from the boss; bottom layer of B ring is thin. Pocket ring for C spans the whole pocket (pocket is only 1.4x1.9), so it is scaled to the pocket, not the hole; corner angles 36 deg there.
- Symmetry: slot cuts mirror left/right except the lower-left cut goes to pocket corner/mR; boss ring and A ring are symmetric about their own centres except A's right side. No overall mirror line in the part.
- Long fans / wedges: blocks a_se-P2-D1-pkBL, the wedge below the pocket, and the large band along the lug arc (Qsw..P2) are broad and skewed. They hold no feature; they follow the outline's own 45-degree diagonal and the lug round. Kept rather than adding subdivisions that would only chase a number.
- Subdivisions: 40 drawn + 10 fill = 50 blocks, high. Cap on the right round has 4 blocks (needed: parity of the vertical line N0/N3 corners). Numerical repairs so far were geometric (moving corners), none added blocks solely for a metric.
- Decision: submit as rev1. Remaining weak spots: thin B bottom layer, 29-deg pocket corner, thin wedge block near Dp/N3.

## rev1 full run (drawing out/t0_p336d70065d_rev1.png) — read before repairing
Not counted: 2-D judge PASS, but mesh judge max element aspect 30.1 > 20 at (7.20,3.45), region 2 block 47 = the fill's bottom slot-cap block (10 cells along a 150-degree arc, one cell across 0.69). min SJ 0.375 passes. Everything else (rings, rest of base) was fine in the picture; the defect is local to the slot caps.

## Draft d5 -> rev2 (drawing: out/t0_p336d70065d_draft_d5.png)
Only change: slot drawn by hand (8 blocks) instead of the fixed fill; radial centre cuts Wm-T90 and B270-Dd split each cap into two ~75-degree blocks, caps made shallower (~0.33). The new cuts are radial/perpendicular to the slot arc and to the wall, so they are justified by rules 8/9, not by chasing a number. Check ar3d went 20.8 -> 10.5.
- Isolation: slot now has its own ring (6 loop corners) + 2-block core; holes/boss/pocket unchanged from rev1.
- Costs: +5 blocks (55 total); small wedge blocks near Dr/Dp remain thin; B ring bottom layer still thin; broad skewed blocks along the lug arc/diagonal unchanged (no features there).
- Decision: submit as rev2.

## rev2 full run (drawing out/t0_p336d70065d_rev2.png) — read before repairing
Not counted: max element aspect 20.27 > 20 at (2.58,2.49,z .5745), block 3 = right block of the A ring. Cause: the base region has a 0.023-thick layer (between the region-2 and region-3 top levels), so any in-plane edge over ~0.46 fails; the slot caps are fixed (worst went 30.1 -> 20.3). Slot drawing looks coherent: radial centre cuts, shallow caps.

## Draft d6 -> rev3 (drawing: out/t0_p336d70065d_draft_d6.png)
Only change: A-ring box right side moved x 2.8 -> 2.7 (a_ne, a_se), shortening the ring's radial edge from ~0.51 to ~0.42. No block added. Cost: judge min sine 0.40 -> 0.36 (still > 0.35) in the boss ring's bottom-left corner at a_ne; A ring is now slightly more symmetric about the hole (right margin 0.26 vs left 0.10). The drawing shows no other change. Decision: submit as rev3.

## rev3 full run (drawing out/t0_p336d70065d_rev3.png) — read before repairing
Not counted: aspect 20.22 > 20 at (9.01,3.32) in the lower cap block of the right round (outline side of 1.86 length gets 4 cells of 0.465; limit in the 0.023-thick base layer is ~0.46). The A-ring edge is fixed. Side effect: boss-ring bottom-left corner at a_ne now 21 deg, min SJ 0.293 (was 0.375).

## Draft d7 -> rev4 (drawing: out/t0_p336d70065d_draft_d7.png)
Two small moves, no new block: M2c on the right round from -30 to -20 deg (lower cap's outline side becomes ~2.1 long, so it gets 5 cells ~0.42) and A box right side x 2.7 -> 2.75 (less skew at a_ne; judge min sine 0.36 -> 0.39). Picture shows the same topology; cap still four blocks, lower cap block a little taller. Decision: submit as rev4.

## rev4 full run (drawing out/t0_p336d70065d_rev4.png) — read before repairing
Not counted: aspect 20.20 > 20 at (2.86,0.67), bottom of the lug, in the large block between the A box and the lug arc (S block, arc side 3.95 long, corners 155/132 deg). Previous offenders (A ring, right cap) are fixed; min SJ 0.339. The layout keeps the same structure; the remaining defect is skew in one broad lug block. (A vertical cut d8-first-try made a 180-degree corner and was discarded at `check`.)

## Draft d8 -> rev5 (drawing: out/t0_p336d70065d_draft_d8.png)
Only change: the a_sw cut to the lug arc now leaves 30 deg off vertical (Qsw at 219.4 deg), so the two lug blocks have corners 120/150 instead of 155/115 and the arc side of the S block drops 3.95 -> 3.3. No block added. Judge min sine unchanged 0.386. Decision: submit as rev5.

## rev5 full run (drawing out/t0_p336d70065d_rev5.png) — final
COUNTED (strict True, stable True, min SJ 0.339 / 0.336 at 2x, 32/32 sharp edges captured). Read of the drawing: holes A, B, C each ringed; boss ringed (outer 4 blocks + fill ring/core); slot has its own ring and two-block core with radial centre cuts; pocket drawn as a ring to its four corners. Final review stays as submitted, no further repair.
Remaining tradeoffs: 55 blocks is high; hole B's ring is thin on the bottom (0.07) because the boss and top wall crowd it; the pocket ring for hole C is scaled to the pocket (corners 36 deg), not to the hole; broad skewed blocks along the lug arc and the lower diagonal hold no feature and follow the outline; corner a_ne in the boss ring's bottom-left is 23 deg; thin wedge blocks near Dr/Dp; slot and right-hand cap use extra blocks for parity with neighbours, not for appearance. The split CAD radius on the slot (junction 5.3) did not cause a failure.
