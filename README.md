# tuftenote

Tufte-inspired LaTeX style for notes and reports. Wide right margin for sidenotes, margin figures, and annotations.

## Features

- A4 page with 6 cm right margin for sidenotes
- `\marginpar`, `\marginnote`, `\sidenote`, `\marginfigure` ready to use
- Math: amsmath, mathtools, tikz, `\argmax`, `\argmin`
- Russian language support (babel T2A)
- biblatex with biber
- Optional debug labels for equation references

## Installation

Clone into your local texmf tree:

```bash
git clone git@github.com:newrlan/tuftenote.git ~/Library/texmf/tex/latex/tuftenote
```

On Linux the path is `~/texmf/tex/latex/tuftenote`.

## Usage

```latex
\documentclass{article}
\usepackage{tuftenote}

\graphicspath{{pics/}}
\addbibresource{biblio.bib}

\begin{document}
Hello world.\marginnote{A side note.}
\end{document}
```

To show equation label keys (for debugging):

```latex
\usepackage[showkeys]{tuftenote}
```

## What stays in your document

The style handles layout and packages. Keep these in your `.tex` file:

- `\graphicspath{...}` -- project-specific image path
- `\addbibresource{...}` -- project-specific bibliography
- `\newtheorem{...}` -- document-specific theorem definitions
