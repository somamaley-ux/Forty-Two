# Unified Capstone Manuscript

This directory contains an Overleaf-ready LaTeX project for the unified capstone manuscript.

## Contents

- `main.tex` --- master file
- `preamble.tex` --- packages, theorem environments, metadata, and source aliases
- `frontmatter/` --- title page and abstract
- `sections/` --- main theorem chain
- `appendices/` --- dependency register, formalization map, denial map, reading path, source ledger, and bibliography

## Build

Compile with standard `pdflatex`.

A typical local build sequence is:

```bash
pdflatex main.tex
pdflatex main.tex
```

The project is arranged to compile directly on Overleaf.

## Formalization claim discipline

This manuscript does **not** claim a unified capstone Lean development unless one is explicitly supplied in the declared source set. The formalization appendix states only what the current sources document: exact theorem wrappers where available, theorem-family correspondence where only that level is documented, and manuscript-specific Lean audit statements where that is the strongest available support.
