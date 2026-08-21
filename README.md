# Nb₃Sn Cavity Paper

Cavity-only manuscript, split out of `Nb3Sn_Cu_Paper`. Covers the RF cavity development
arc; coupon-scale film development stays in the companion papers.

**Framing:** Nb first, then Nb₃Sn, on roughly matched geometry. Nb is the easy film —
sputter and stop. It establishes what the copper body, the seam, the surface prep, and
the deposition system permit. Nb₃Sn is the hard film and the only one whose $H_{c2}$
clears 9 T. The gap between them localises the problem.

## Build

```
latexmk -pdf main.tex     # biber backend, biblatex
```

`\TODO{...}` renders in **red**. Nothing with red on the page is submittable.

## Cavity sequence

| § | Cavity | Coating | Status | Headline |
|---|--------|---------|--------|----------|
| `results_8piece.tex` | 8-piece hexagon | 1 wall Nb₃Sn (Nb-first) | measured | $R_s$ = 8 mΩ vs 11 mΩ Cu; SC lost at 8 T |
| `results_2piece_nb3sn.tex` | 2-piece hexagon | full Nb₃Sn (Nb-first) | measured | $Q_L$ = 77,000 @ 50 mK; corrected $Q_0$ ≈ 1.4×10⁵ |
| `results_2piece_tanb.tex` | 2-piece hexagon | Ta/Nb only | measured | $Q_0$ = 1.4×10⁶ @ 2 K; 13,000 @ 9 K |
| `results_cyl_cu.tex` | cylinder = **Tom Braine's cavity** | bare Cu, electropolished | **not run** | — |
| `results_cyl_nb3sn.tex` | same cylinder | Nb₃Sn (hot bronze) | **not run** | — |

**Three bodies total:** 8-piece hexagon, 2-piece hexagon, Braine's cylinder.

Cylinder from here on: hand polishing and electropolishing both reach a cylindrical
surface uniformly, and the hexagon's acute inner corners do not. Accepts the ~27 % seam
penalty to get a properly finished surface. Geometry is Braine's unmodified — pull
dimensions from his thesis, don't re-derive.

### Ta/Nb result, as measured

- Body: the 2-piece hexagon. Its own bare-Cu baseline is 55,000 max → **25× improvement**
- 500 nm Ta @ 60 W, 10 mTorr · 750 nm Nb @ 250 W, 8 mTorr · both DC, 200 °C substrate
- $Q_0$ = 1.4×10⁶ at 2 K, PPMS, zero field. $R_s$ = 250 µΩ for $G$ = 350 Ω
- $Q$ = 13,000 at 9 K — *below* bare Cu, because normal-state Nb is more resistive than
  annealed Cu and the 750 nm film exceeds its normal-state skin depth. 108× swing across
  the transition, and the 9 K break confirms clean Nb + a working Ta barrier
- No $Q$ vs $B$ (Nb is mixed-state below 0.4 T — not worth the magnet time)

### EP recipe (cylinder)

3:2 phosphoric acid : butanol, 45 °C, held at the current plateau 10–15 min,
~500 rpm agitation.

## Open items

### Ta/Nb cavity — two details left
- [ ] Surface prep history for that body (hand polish only, or etch + anneal too?
      55,000 matches the fully etched+annealed state)
- [ ] Substrate rotation during Ta/Nb; were the endcaps masked?

### Photos — stubs are in place, drop files in and swap the `\TODO`
- [ ] All three bodies side by side, same scale (`fig:threebodies`, `methods.tex`)
- [ ] Ta/Nb cavity interior, endcaps especially (`fig:tanbCavity`)
- [ ] Electropolished cylinder, assembled + open (`fig:cylCu`)
- [ ] EP cell in operation (`fig:epsetup`) — only process step with no visual record
- [ ] Cylinder after hot-bronze coating (`fig:cylNb3Sn`)

### Cylindrical cavities — not yet run
- [ ] Braine's dimensions transcribed from his thesis
- [ ] EP cathode, plateau voltage/current density, resulting roughness + how measured
- [ ] Hot-bronze cavity recipe (Cu-Sn thickness/composition, substrate temp, post-react?, mask?)
- [ ] Coupon witness carried through the cavity run, SQUID $T_c$
- [ ] $Q(B)$ to 9 T — the measurement the 8-piece cavity failed

### Cross-cutting
- [ ] Companion paper citations (Cu-substrate, Nb-substrate, SLAC mushroom) — 3 `\TODO`s
- [ ] ASC funding source
- [ ] Table 1 gaps in `discussion.tex`

## Relation to other repos

- `Nb3Sn_Cu_Paper` — coupon recipe development on Cu. Cavity sections move here; that
  paper becomes coupon-only.
- `Nb3Sn_Nb_Paper` — Nb/sapphire substrates, strain vs Sn decoupling.
- `Nb3Sn_SLAC_Paper` — hot-bronze films on bronze disks, SLAC mushroom cavity.
