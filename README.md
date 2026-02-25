# ACM CHI Paper Starter Template

A clean LaTeX starter template for ACM CHI (and similar ACM SIGCHI) conference papers, using the official [`acmart`](https://www.acm.org/publications/proceedings-template) document class.

## File Structure

```
main.tex                   ← Root document; compile this
defs.tex                   ← Custom macros and definitions
references.bib             ← Bibliography (export from Zotero here)
sections/
  abstract.tex             ← Abstract
  introduction.tex         ← Introduction
  related-work.tex         ← Related Work
  methods.tex              ← Methods / Study Design
  results.tex              ← Results / Findings
  discussion.tex           ← Discussion
  conclusion.tex           ← Conclusion
  acknowledgments.tex      ← Acknowledgments
```

## Getting Started

1. **Fill in paper metadata** in `main.tex`:
   - `\title{}`, `\author{}`, `\affiliation{}`, `\email{}`
   - ACM conference details (`\acmConference`, `\acmYear`, etc.)
   - CCS concepts (generate at <https://dl.acm.org/ccs>)
   - `\keywords{}`

2. **Write each section** by editing the corresponding file in `sections/`.  
   Replace every `% TODO` placeholder with your actual content.

3. **Add your references** to `references.bib`.  
   The easiest workflow is to export directly from [Zotero](https://www.zotero.org/)  
   using the **Better BibTeX** add-on (<https://retorque.re/zotero-better-bibtex/>).

4. **Add custom macros** to `defs.tex` as needed.

## Compiling

```bash
# Single command with latexmk (recommended):
latexmk -pdf main.tex

# Or manually:
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

## Template Options

The document class is set to `sigconf` (two-column proceedings, used for CHI).  
Other common options:

| Option       | Use case                          |
|--------------|-----------------------------------|
| `sigconf`    | CHI, CSCW, UIST proceedings       |
| `manuscript` | Single-column manuscript format   |
| `review`     | Adds line numbers for review      |

To remove the `review` option for camera-ready submission, edit the first line of `main.tex`:

```latex
\documentclass[sigconf]{acmart}
```