# ASC 2026 Paper

"A Compact 11 GHz Split Cavity for Rapid RF Evaluation of Superconducting Films in a
Standard PPMS" — IEEE Transactions on Applied Superconductivity, ASC 2026 special issue
(presentation 1MPo2D-06).

## Files

| File | Purpose |
|---|---|
| `main.tex` | Manuscript |
| `refs.bib` | References |
| `IEEEtran.cls` | IEEE class, V1.8b (current IEEE Transactions template) |
| `IEEEtran.bst` | IEEE bibliography style, 1.14 |
| `cavity_photo.png`, `sim_modes.png`, `Quality.png` | Figures (flattened, no alpha) |
| `cover_letter.tex` / `.pdf` | Cover letter |

The layout is flat (no subfolders) and `main.tex` follows the ScholarOne LaTeX guide:
`%&pdflatex` first line, figures referenced without extension, no siunitx/hyperref
(siunitx is broken on the IEEE submission server).

## Build

```
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

## ScholarOne upload

ScholarOne does not run BibTeX, so upload the generated `.bbl` with the same base name
as the `.tex` (e.g. `main.tex` + `main.bbl`), plus `refs.bib`, `IEEEtran.cls`,
`IEEEtran.bst`, and the three PNGs, all as TeX/LaTeX Suppl Files.
