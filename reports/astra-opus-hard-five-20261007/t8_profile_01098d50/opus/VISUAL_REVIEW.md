# VISUAL_REVIEW — batch p, t0_p2dd63146ab (author's own review, not an expert grade)

## draft d1 → submitted as rev1 — drawing `batchp/out/t0_p2dd63146ab_draft_d1.png`

Regions read from the listing: R1/R2/R3 are counterbore annuli (higher-floor material between a through hole and its
level loop), not voids; holes 1-5 are through. Each annulus is drawn by me with radial cuts matching the box-ring corners.

- **Feature isolation:** every through hole and every level loop has its own ring. R1, R3, R2: concentric hole→level-loop
  annulus (5 radial blocks) inside a reverse O-grid box. H4 boxed (left side on the outline, 4 ring blocks). Slot boxed with
  its top ring block along the top edge (3.9 gap) and left/right ring blocks split at the slot mid-height.
- **Ring scale:** R1 box margin about 2.5 to 4 beyond the level loop, R3 about 2.7 / bottom on the outline, H4 about 3.4 to
  4.5. R2 is the weak one: its box runs to the outline on the right and bottom (P2 on the bottom-right round, R2TR on the
  right edge), so ring block 22 is about 13 thick and block 24 has a 31° corner at R2TR. Accepted for now because a
  separate wrap of the bottom-right round adds a column of blocks; flagged as the first thing to revisit.
- **Symmetry/transitions:** slot ring symmetric about its mid-height; R1/R3 rings share the x=65.2 line and y=29.8 line
  (R1 bottom ring split at R3TL). Rounds: top-left round wrapped by blocks 40/42, top-right by 44/45, bottom-left by 50.
- **Diagonals/wedges:** R1TR→R2TL diagonal at about -24° (blocks 52/53) is a shallow slant (rule 6 tension) needed to
  give both box corners a conforming exit; R1TR→Fp at 45°. Left band 47/48 follows the angled left edge (cuts N–U
  perpendicular to it). Sharpest corners: o3 34°, o1 35°, A 36° (ring-to-outline corners), all above the 20.5° limit.
- **Subdivisions:** 56 blocks (41 base + 3×5 annulus); the extra ring splits (R1 bottom, R2 left, R3 left, slot sides) each
  carry a cut that conforms a neighbouring box corner; none is decorative.

Decision: submit as rev1. The check passes cleanly with no marks; the R2 ring-to-outline corners are a known tradeoff to
inspect after the full run's quality numbers rather than chase now.

## rev1 full-run drawing — `batchp/out/t0_p2dd63146ab_rev1.png`

Same structure as d1 (read after the run). The full run refused it only on element aspect (21.1 > 20): the part has
a 0.313-thick layer between the R2 floor (5.795) and the R3 floor (6.108). Every element in that layer needs an in-plane
edge under about 6.26, which is below nominal size. The bad element sits on the top-left round (block 40, arc side
A–Qa, 26.2 chord in 4 cells). That is a sizing problem, not a feature-isolation one, so the repair should move corners
and keep the structure.

## draft d3 → submitted as rev2 — drawing `batchp/out/t0_p2dd63146ab_draft_d3.png`

- Repairs: no blocks added or removed (still 56). Corners moved so that each chain of opposite sides divides
  under about 6.1 by my own estimate: Qa 120°→126° on the top-left round, Ra 55°→60° on the top-right round, H4
  box right side 22→22.8 (margin to the hole 4.3; the box is still near the hole's scale), R2 box top 45.5→47.2 (top margin
  5.1 against left 3.1). M is moved to (25,80) so block 42 stays well shaped (d2 had a 149° corner at M).
- Isolation, rings and symmetry are unchanged from rev1. The top-left wrap blocks 40/42 now split the round more evenly.
- Effect of the repair on the structure: there is none visible. The R1TR→R2TL diagonal becomes slightly shallower (about
  -21°) because R2's box top rose. That rule-6 tradeoff remains and is accepted.
- Remaining weak transitions: R2 ring to the outline (R2TR 35°, block 22 thick); H4 ring corner A 36°.

Decision: submit. The structure is coherent and the change targets the measured failure without new partitions.

## rev2 full-run drawing — `batchp/out/t0_p2dd63146ab_rev2.png`

Read after the run. The structure is the same as d3. The refusal again came from element size in the 0.313 layer
(21.4): this time on the top edge beside Hp (block 44), where moving Ra from 55° to 60° left only 30° of the top-right
round on that chain of blocks. The run's cell counts show that the outline-round sweep sets the count there: 5 cells in
rev2 against 6 in rev1, so the cells grew to about 6.7. rev1's hotspot (block 40) did not reappear.

## draft d4 → submitted as rev3 — drawing `batchp/out/t0_p2dd63146ab_draft_d4.png`

- Single change from rev2: Ra back to 55° on the top-right round, so the top-right wrap blocks 44/45 split the round
  as they did in rev1. The rev2 repairs on the top-left (Qa 126°, E/X 22.8, M) and R2 box top 47.2 are kept.
- Feature isolation, ring scale and symmetry are unchanged. No new partition was added. The blocks 44/45 split of the
  round is close to its midpoint, which also reads better than rev2's 60°.
- Remaining tradeoffs are the same as before: R2 ring corners at the outline (R2TR 35°, P2), the shallow R1TR→R2TL diagonal,
  and the H4 corner A at 36°.

Decision: submit. Each part of this revision has already been through a full run in rev1 or rev2 without being the worst element.
I can't model the mesher's cell counts exactly, so this is the evidence-based repair, not a guess at a new partition.

## rev3 full-run drawing — `batchp/out/t0_p2dd63146ab_rev3.png`

Read after the run: same as d4. Aspect is down to 20.49 (from 21.44). The rev2 top-right hotspot is gone. The worst
element is now in the slot's top ring block 37, the 41.5 × 3.9 strip between the slot and the top edge (cells about
6.42 along the top). That block has been identical in every revision. It surfaced only because the larger hotspots
were removed.

## draft d5 → submitted as rev4 — drawing `batchp/out/t0_p2dd63146ab_draft_d5.png`

- Change: one cut sT–Hm on the slot's own mirror line (x = 54.79), from the slot's top straight to the top edge. It is
  3.9 long and perpendicular to both walls (rule 3). The slot ring becomes 7 blocks and is mirror-symmetric about that
  line (rule 12 / local symmetry). Both ends sit on boundaries, so nothing propagates into the rest of the layout.
- Why this is not just chasing a number: the top ring block was a long thin strip whose cells along the top were the
  largest left in the thin layer. Splitting it where the slot is symmetric isolates each rounded slot end with its own top
  block, the way rule 9 asks rounds to be treated. This is one local partition and no global restructuring.
- Everything else is unchanged from rev3; the same remaining tradeoffs (R2 ring-to-outline corners, R1TR→R2TL slant,
  H4 corner A) apply.

Decision: submit.

## rev4 full-run drawing — `batchp/out/t0_p2dd63146ab_rev4.png`

Read after the run: same as d5. Aspect is 20.52, and the worst cell is the one beside Hm (about 6.43). The element count
is identical to rev3, so the split did not change the cell count along the top. Each half's slot side mixes a 45° arc with
a straight run, so cells bunch over the arc and spread over the straight run. The mirror cut is still sound for symmetry,
but by itself it did not fix the size.

## draft d6 → submitted as rev5 — drawing `batchp/out/t0_p2dd63146ab_draft_d6.png`

- Change: vertical cuts from slot junctions 5.1 and 5.2 (where the rounded slot ends meet the straight top) up to the top
  edge, perpendicular to both walls. The top band is now: a rounded-end block at each side (blocks 40, 37: slot arc
  against a 10.8 straight top), and two 9.98 × 3.93 rectangles over the straight run, split on the mirror line.
- Feature isolation: each rounded slot end now has its own top block. The straight run is plain rectangles (rules
  5, 9). The slot ring has 9 blocks and is mirror-symmetric about x = 54.79.
- Tradeoff: four small blocks along a 3.9 gap is more partitioning than the expert's fewest-blocks preference would pick
  (rule 10). The band stays local to the slot (no strip carried across the part, rule 11 unmarked). The reason is the
  0.313 layer's size limit, documented above, not appearance.
- No other block changed. The remaining tradeoffs are as before.

Decision: submit. If this still fails, one revision remains.

## rev5 full-run drawing — `batchp/out/t0_p2dd63146ab_rev5.png` (COUNTED)

Read after the run; identical to d6. Every through hole (H4, slot, R1/R2/R3 holes) and every counterbore level loop has
its own ring. The three annuli are cut radially and their corners match the reverse O-grid boxes outside. The four outline
rounds each sit in wrap blocks with their corners on the outline. The top band over the slot is now four short blocks.

Result of my visual review (author's own, not an expert grade): coherent feature-aligned layout. The remaining tradeoffs are:
1. R2's ring runs to the outline at P2 and R2TR (bottom-right round and right edge). Block 22 is thick, with a 35° corner at R2TR.
2. The R1TR→R2TL diagonal is about -21°: a shallow slant (rule 6), needed so both box corners exit conformally.
3. H4 ring corner A on the top-left round is 36°.
4. The slot's top band has 4 small blocks (rule 10 tension), forced by the 0.313 layer's size limit, not by appearance.
5. The 59 blocks sit within the block-count limits (base 44 vs 3×39).
