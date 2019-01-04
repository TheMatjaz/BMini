BMini: a Minimal LaTeX Beamer theme and `.tex` file preamble
================================================================

Features
---------------------------------------

- Supports PdfLaTeX and XeLaTeX
- Sets the language end encoding
- Sets the document metadata (author, title, PDF metadata etc.)
- Configures the syntax highlighting for `lstlisting` code snippets
- Adds some tweaks, fonts and colors to the _Default_ Beamer theme
- Removes navigation symbols
- Adds slide number in the bottom right corner
- `\section{A title}` creates a blank slide with only `A title` in bold
  in the middle
- Additional custom commands


Usage
---------------------------------------

Clone this repository using Git Subtree into the Git repository with
the LaTeX document you are currently editing:

```bash
git subtree add --prefix=bmini https://github.com/TheMatjaz/BMini.git master --squash
```

Add these lines immediately after the `\documentclass` command.
Change the author, title, subtitle and abstract as you prefer
or leave them empty. Alter the `\bminipath` based on the prefix you
used in the Git Subtree command.

```tex
\newcommand{\bminipath}{bmini}
\newcommand{\presentationauthor}{Name Surname}
\newcommand{\presentationtitle}{My title}
\newcommand{\presentationsubtitle}{}  % Empty subtitle
\newcommand{\presentationabstract}{This presentation is about BMini}
\input{\bminipath/bmini.tex}
```

To update BMini to the latest version, run
```bash
git subtree pull --prefix=bmini --prefix= https://github.com/TheMatjaz/BMini.git master --squash
```
