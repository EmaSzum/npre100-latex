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
- After setting up the class, the body of the document is written between the `\begin{document}` and `\end{document}` tags.

- This is called the preamble of the document. A preamble acts at the document's "setup" section, where you can define the document class and load packages.
- An example of a simple preamble is found below:
```latex
\documentclass[12pt, letterpaper]{article} %additional parameters are included in square brackets
\usepackage{graphicx}
```

- A list of useful packages to include in your preamble are listed below:
```latex
\usepackage{graphicx} %provides support for managing graphics. Can scale and rotate images
\usepackage{siunitx} %allows users to type consistent numbers and units
\usepackage{amsmath} %helps with mathematical formatting
\usepackage{float} %allows the use of [H] for fomatting figures
```

- Now that the document is set up, a title page can be created. For your lab reports, the title page should include the title of the lab, the class, your name, partners, and the date.
- Your title should go in the preamble, not the main body of the text.
```latex
\title{Super Cool Lab Report Title\\  NPRE 100} %a double backslash makes a new line
\author{Ema Szum}
\date{3 November 2026}
```

- The body of the text should contain sections and subsections to organize your paper. This can be done with the commands `\section{Title of your Section}` and `\subsection{Title of your Subsection}`
- In the body, a table of contents should be included to keep track of sections and subsections. This can be done with one line: `\tableofcontents`.
- Putting it all together, we get a basic LaTeX document setup for a lab report:
```latex
\documentclass[12pt, letterpaper]{article}
\title{Super Cool Lab Report Title\\  NPRE 100}
\author{Ema Szum}
\date{3 November 2026}

\begin{document}
\maketitle
\newpage

\tableofcontents
\pagenumbering{gobble}
\newpage

\pagenumbering{arabic}
\section{Section Name}
\subsection{Subsection Name}

\end{document
```

## Figures
- Overleaf has a built in option to add figures. However, if you would like more personalization they can be added manually:

```latex
\begin{figure}[h] %[h] makes sure you figure will be placed roughly where you have it in the code, [H] acts as a sticter version of this
  \centering
  \includegraphics[width=0.75\textwidth]{NPRE100.jpg}
  \caption{A very insightful plot}
  \label{fig:NPRE100} %this allows you to dynamically reference figures in the text with \ref{fig:NPRE100}
\end{figure
```


## Tables
- Tables can be a helpful way to view data. Overleaf also has a built in option to add tables. However, you can create a table manually as displayed below:

```latex
\begin{center}
  \begin{tabular}{|c|c|c|} %vertical lines are placed between the columns in this section
    \hline %horizontal lines are places between the rows in this section
    cell1 & cell3 & cell3 \\
    \hline
    cell4 & cell5 & cell6 \\
    \hline
    cell7 & cell8 & cell9 \\
    \hline
  \end{tabular}
\end{center}
```

## Equations
- As engineering students, your lab reports will contain many equations. Luckily, equations can be easily formatted with LaTeX!
```latex
\begin{equation}
1 + 1 = 2
\end{equation}
```

- If you wish to write an equation with specific alignment that spans multiple lines, you can use the following to align equations where you place a & symbol in your equation:
```latex
\begin{align}
c & = 20
120 &= 6c
\end{align}
```

- There are many different symbols and mathematical operators that LaTeX supports. You can find a summary of symbols are operators below:
`https://oeis.org/wiki/List_of_LaTeX_mathematical_symbols`


### Acknowledgments
- Now you know the basics of LaTeX! If you get lost, please reference LaTeX's documentation page, there are also many helpful online forums.
- Happy writing!
