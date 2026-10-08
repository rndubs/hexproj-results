# VISUAL_REVIEW — batch p, part t0_p94c5816bb9 (author's own review, not an expert grade)

## Draft d1 → submitted as rev1
Drawing read: `batchp/out/t0_p94c5816bb9_draft_d1.png` (Read tool, 2026-10-08 ~04:50Z).

- **Feature isolation.** Every through hole has its own ring. The big hole H4 sits in a rectangular box (3.75–7.88 × 3.65–6.55) with 8 ring blocks; the extra radial cuts come from the y=5.083 vertex lines and the H1/pocket box sides. H3 has a 4-block box ring (7.88–9.54 × 5.08–6.55). H2 (in the step region) has a 5-block box ring; its right block is split radially at y=8.571. H1 straddles the step boundary: a 3-block ring below the level line and one cap block above it, with the required junctions j12/j10 as corners. The blind pocket (region 0, a lower level, not a void) gets an O-grid: a core plus 4 inner blocks, and 4 outer ring blocks to a box. The top-right round is not cut mid-arc: it stays inside block 50, with corner A1 at its tangent point and a radial cut from its centre.
- **Ring scale.** H2 and H3 rings are about 0.3 thick, close to the hole scale. H4's ring is about 1.0 thick at the sides but only 0.29 / 0.49 at the bottom / top, which the pocket and H1 force. The H1 lower ring is too wide sideways (~1.0) and very thin below (0.18), so block 35 is a long thin trapezoid with 24° corners. That is the weakest local transition.
- **Symmetry/transitions.** The part has no mirror line, because the holes are not symmetric. The left and right vertex cuts at y=5.083 mirror each other. The pocket box is centred on the pocket.
- **Fans/strips/wedges.** One slanted cut, N→Q, runs about 18° off vertical in the bottom-right. It is needed because a vertical line there meets the 60° wall and leaves a triangle. Block 4 is a long slanted strip along the lower-right wall, which follows the wall direction. The cap column above H1 (blocks 46/47, 0.54 wide) runs to the top edge. It is forced by the two required junctions; rule 11 did not mark it.
- **Unnecessary subdivisions.** 51 blocks is a lot (rule 10), but each line serves a feature box or a required junction. No numerical repairs have been applied yet.
- **Decision:** submit as rev1. The layout is coherent and passes check (min sine 0.405, forecast edge ratio 9.8). The full run's 3-D and refinement results should decide whether the thin H1 bottom block needs a repair.

## rev1 full-run drawing
Drawing read: `batchp/out/t0_p94c5816bb9_rev1.png`. Same partition as d1. The run reported 2-D PASS and SJ 0.405 at nominal and doubled density, but it was not counted: STRICT `ar_ok` failed with a worst element aspect of 21.06 against a_max 20. That element is at (6.40, 6.63, 4.13), in the thin H1 bottom ring block (block 35). This confirms the weak transition flagged above: the H1 box was about 1.0 wide on each side, so its radial edges were about 1.1 long, while the gap under the hole is only 0.18 thick, so several cells were squeezed into it.

## Draft d2 → submitted as rev2 (repair of the H1 transition)
Drawing read: `batchp/out/t0_p94c5816bb9_draft_d2.png`.
- **Repair:** H1's box is narrowed to x 5.6–7.2, a ring about 0.3 thick at the hole's scale. Its radial edges are now about 0.55 long instead of about 1.1. This follows the guidance to keep the reverse O-grid near the hole's scale. It is not a cosmetic subdivision. Above the step line the cap gets its own small 4-block ring, in a box 5.6–7.2 × 7.625–8.571 with inner corners M1/M2 straight above the required junctions j12/j10.
- **Effect on the overall structure:** the new box sides add two cuts into H4's top ring at x=5.6 (vertical, about 12° off radial) and from (7.2, 6.55) to the 60° point on H4 (about 24° off radial). H4's top ring now has 5 blocks. Block 28 (37°/144°) is the most skewed of them, but still well within the sine limit. In region 1 the columns are 4.9–5.6, 5.6–7.2 and 7.2–7.884: wider than the old 0.54 cap column, and no sliver band was marked.
- **Other features are unchanged:** the H2 box, the H3 box, the pocket O-grid, the vertex cuts and the round kept whole.
- **Tradeoff:** 58 blocks, up from 51 (rule 10). The other bottleneck is the 0.18 gap above H3. Its radial edges are already short (about 0.5), and it did not set the worst element in rev1.
- **Decision:** submit d2 as rev2. Check passes with min sine 0.430 (was 0.405) and forecast edge ratio 10.4.

## rev2 full-run drawing
Drawing read: `batchp/out/t0_p94c5816bb9_rev2.png`. The partition is the same as d2. The full run reports 2-D PASS (sine 0.43), 3-D strict True, stable True, SJ 0.4300 at nominal and doubled density, and COUNTED True. The H1 repair removed the aspect failure without changing the rest of the layout.

**Result of the visual review:** I stopped at this first counted pass. Remaining tradeoffs:
- 58 blocks is many (rule 10).
- H4's ring is uneven: about 1.0 at the sides and 0.29–0.49 top and bottom, set by the pocket and H1.
- The 0.18 gaps under H1 and over H3 are thin.
- Block 28 is skewed (37°/144°).
- The slanted N→Q cut and the strip along the lower-right wall are forced by the 60° walls.
- Region 1 has a 155° corner at the H2 box's top-left (g56).
- The top-right round stays whole in one block (A1 at its tangent point) rather than being wrapped.
