# ASC 2026 Conference Paper

4-page IEEE-format paper for the 2026 Applied Superconductivity Conference, covering
RF characterization of a sputtered Nb-coated (Cu/Ta/Nb) two-piece hexagonal copper
cavity at 11 GHz, benchmarked against bulk copper (measured and simulated) and the
BCS-limited surface resistance of niobium.

Built from `ASC2026_Poster_final.pptx`. Scoped to that poster's content only — the
full multi-cavity journal manuscript (Nb₃Sn, 8-piece, and cylindrical-cavity results)
lives separately in [`ASC_Cavity_Paper`](https://github.com/dreynater-sketch/ASC_Cavity_Paper).

## Build

```
pdflatex main.tex
pdflatex main.tex
```

Plain `thebibliography` — no biber/biblatex step needed.

## Before submitting

- [ ] Verify the Kajfez & Hwan (1984) citation's exact volume/page
- [ ] Confirm author emails/affiliations for all five authors
