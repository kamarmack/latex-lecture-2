## LaTeX Lecture 2

Focus areas of the lecture include citations and figures:

```plaintext
\documentclass{article}
\usepackage{amsmath}
\usepackage{amsthm}
\usepackage{amssymb}
\usepackage{xcolor}
\definecolor{lightblue}{RGB}{80,160,255}
\usepackage[colorlinks=false,
  linkbordercolor=lightblue,
  urlbordercolor=lightblue,
  citebordercolor=lightblue]{hyperref}
\usepackage{graphicx}
\title{My Second Mathematics Paper}
\author{Your Name}
\date{\today}

\begin{document}
\maketitle
\section{Second Lecture featuring Citations and Figures}

%%%%%%%% Example of citing a paper in your References section %%%%%%%%

A classical result of Euclid states that there are infinitely many
prime numbers \cite{euclid}.

%%%%%%%% Defining Figures via Image Uploads %%%%%%%%

% Upload graph.jpg and results-data-table.jpg into your Prism project first.

% Example of inserting a figure:
\begin{figure}[ht]
    \centering
    \includegraphics[width=0.6\textwidth]{graph.jpg}
    \caption{Example graph.}
    \label{fig:graph}
\end{figure}

Figure~\ref{fig:graph} shows an example graph.

% Example of inserting another figure:
\begin{figure}[ht]
    \centering
    \includegraphics[width=0.5\textwidth]{results-data-table.jpg}
    \caption{Example results data table.}
    \label{fig:results-table}
\end{figure}

Figure~\ref{fig:results-table} shows the results data table.

% \includegraphics{} inserts the image.
% width=0.6\textwidth makes the image 60% of the text width.
% \caption{} gives the figure a numbered caption.
% \label{} gives the figure an internal name.
% \ref{} prints the corresponding figure number.

%%%%%%%% Defining the References Section %%%%%%%%

% Use the number after the bibliography definition to tell LaTeX roughly how wide the largest citation label will be, so it can reserve indentation space.
% {1} => assumes labels about as wide as 1
% {2} => about as wide as 2
% ...
% {9} => same practical width as {1}
% {99} => reserves enough width for two-digit labels
% {999} => three-digit labels
\clearpage
\begin{thebibliography}{9}

% Citation via Title only (Don't use this)
\bibitem{euclid} Euclid, \textit{Elements}.

% Citation via URL
\bibitem{management} Puji W, Rafiantika M, Indi I, et al., \textit{Application of Graph Theory in Curriculum Management and Subject Interrelations in Secondary Schools. 2024. 20 p. Located at: \href{https://math.com}{click here}}

% Citation via DOI (Digital Object Identifier, a permanent and unique identifier for academic content)
\bibitem{knowledge-graph-approaches} Kechen Q, Kam C, Billy W, et al., \textit{A Survey of Knowledge Graph Approaches and Applications in Education. Elec. 2024;13(2537):1-18. doi: 10.3390/electron-ics13132537}

\end{thebibliography}

\end{document}

```
