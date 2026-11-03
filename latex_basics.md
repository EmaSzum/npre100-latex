# LaTeX Basics

## Initial Config

## Units
-Units should not be put in math mode, this may cause spacing issues
-`siunitx` formats numbers and units consistently so you do not need to wory about spacing, typography, or unit symbols. Type out the unit's full name, and it will be rendered with the proper subscripts.
``` latex
#include this in the preamble
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
