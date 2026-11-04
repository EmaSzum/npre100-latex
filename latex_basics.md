# LaTeX Basics

## Initial Config
- The most basic LaTeX document can be configured with the follow commands:
```latex
\documentclass{article}
\begin{document}
This is where the body of the document will go
\end{document}
```

- The first line is the document type (class), which controls the appearance of the document. For a standard lab report, you should use the class 'article', but different types of documents may require different classes.
- After setting up the class, the body of the document is written between the '\begin{document}` and `\end{document}` tags.

- From here, the preamble of the document should be set up. A preamble acts at the document's "setup" section, where you can define the document class and load packages.
- An example of a simple preamble is found below:
```latex
\documentclass[12pt, letterpaper]{article} #additional parameters are included in square brackets
\usepackage{graphicx}
```

- A list of useful packages to include in your preamble are listed below:
```latex

```

- Now that the document is set up, a title page can be created. For your lab reports, the title page should include the title of the lab, the class, your name, partners, and the date.
- Your title should go in the preamble, not the main body of the text.
```latex
\document class [12pt, letterpaper]{article}
\title{Super Cool Lab Report Title\\ \normalsize NPRE 100}
\author{Ema Szum}
\date{3 November 2026}
```

- Putting it all together we get a basic LaTeX document setup for a lab report:
```latex
\documentclass[12pt, letterpaper]{article}
\title{Super Cool Lab Report Title\\ \normalsize NPRE 100}
\author{Ema Szum}
\date{3 November 2026}

\begin{document}
\maketitle

\end{document
```

## Units
- Units should not be put in math mode, this may cause spacing issues
- `siunitx` formats numbers and units consistently so you do not need to worry about spacing, typography, or unit symbols. To use this package, simply type out the unit's full name, and it will be renderef with the proper subscripts.
```latex
#include this in the rpeamble
\usepackage{siunitx}
```

As an example, this code:
```latex
\documentclass{article}
\usepackage{siunitx}

\begin{document}

speed: \qty{30}{\kilo\meter\per\hour}

number: \num{103007.234}

unit: \unit{\milli\liter}

\end{document}
```

will produce this result:
> speed: 30 km/h
> number : 103,007.234
> unit: mL

## Figures

## Tables

## Tips and Tricks

### Acknowledgments
