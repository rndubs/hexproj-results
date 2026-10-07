# Batch p visual review (author self-review, not an expert grade)

## t0_p336d70065d — draft d1 -> rev1 (drawing: batchp/out/t0_p336d70065d_draft_d1.png)

- Feature isolation: H1 is ringed inside R3 (R3 drawn by me; the four ring cuts go to R3's corners). H2 has a
  rectangular reverse O-grid whose east side is the vertical diameter x=2.975 of the left round (so the box is
  wider on that side: 0.90 vs 0.72). H3, close to the top wall and to R0, has no box: a radial cut to J0.1, a cut
  to the round (Wh) and cuts to R0/H2's box. R0 (full-thickness boss, region 0) and R2 (thinner pocket, region 2)
  are drawn with their own O-grids; R2 is split at R3's top line y=4.561, which is carried straight on to the
  right round (rule 7).
- Ring scale: H1 ring fills R3 (fixed by the region). H2 box is near the hole's scale. R0/R2 inner cores are
  about half the region size.
- Symmetry/transitions: R2 and R3 locally symmetric. R0 has 6 loop corners (NW, NE, E, SE, S, SW) because it
  must meet 6.0, 6.1, H3S, Kw and Kb; its core is two irregular quads (113/135 degree corners) - not symmetric.
- Fans/wedges: Kb is a 6-block node with the long diagonal Kb->6.1 (blocks 6/9), and block 4 (r0NE-Ptop-6.0) is a
  36-degree wedge; block 2 (H3 east, 38 deg at h3S) and block 33 (32 deg at Tl) are skewed. These come from H3
  and R0 sitting 0.13 apart diagonally with the 6.0/6.1 corners fixed; I could not find an axis-aligned
  alternative without a T-junction cascade. Block 34/38 hold the right round without a wrap band (the round
  is split by the carried y=4.561 line instead).
- Numerical repairs: none yet. Min sine 0.516, forecast edge ratio 10.9.
- Decision: SUBMIT as rev1 to get a full-run verdict early (45-minute session); revise only if the full run or
  its drawing shows a weak transition worth one correction.

## t0_p336d70065d — rev1 full run (drawing: batchp/out/t0_p336d70065d_rev1.png)

- Full run: COUNTED (2-D pass, min sine 0.516; 3-D strict and stable; scaled Jacobian 0.365, 0.374 at double
  density; volume error -0.27%). The drawing matches the draft exactly; no numerical repair was applied.
- Re-read against the five points: features are all isolated (H1/H2 rings, R0/R2 O-grids, H3 ringed by
  four blocks, unequal in size). The remaining weak spots are the ones noted for d1: the 6-block node at Kb with the long
  Kb->6.1 diagonal, the thin wedge at Ptop (block 4), the skewed H3-east block 2, and the unwrapped right
  round. None is a sliver strip carried across the part.
- Decision: STOP. The brief says stop revising once counted. The full-run quality is acceptable (sj 0.36),
  so it does not justify spending another run on a cosmetic change.
