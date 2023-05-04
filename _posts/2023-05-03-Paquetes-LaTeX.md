---
title: 'Paquetes interesantes la LaTeX'
date: 2023-05-03
tags:
  - software
---
- **qrcode**: un paquete que permite crear códigos QR e insertarlos directamente en un documento $\LaTeX$. Manual disponible [aquí](https://ctan.dcc.uchile.cl/macros/latex/contrib/qrcode/qrcode.pdf). El uso es muy simple, por ejemplo, con el siguiente código se genera e incrusta un link a la página [gfrubi.github.io](https://gfrubi.github.io/):
```
	  \usepackage{qrcode}
	  ...
	  \qrcode[hyperlink, height=5cm]{gfrubi.github.io}
```
<img src="https://raw.githubusercontent.com/gfrubi/gfrubi.github.io/master/images/2023-05-03_21-07.png" width="100">


- [**Tikz**](https://github.com/pgf-tikz/pgf): un paquete que permite crear diagramas/esquemas de diverso tipo. Manual disponible [aquí](https://pgf-tikz.github.io/pgf/pgfmanual.pdf). Por ejemplo, el código
```
\documentclass[12pt]{article}
\usepackage{tikz}
\usetikzlibrary{calc, angles, quotes}
\def\radius{1.2cm}
\begin{document}
    \begin{tikzpicture}[line cap=round, line join=round]
    %Coordenadas
    \coordinate (sol) at (1.5,3);
    \coordinate (Tierra) at ($(sol)+(120:\radius)$);
    \coordinate (sistema binario) at (7,3);
    %Órbita
    \draw (sol) circle (\radius);
    %Línea
    \draw[dashed] (Tierra) -- (sol) -- (sistema binario);
    %Cuerpos
    \draw[inner color = yellow, outer color = orange, draw = orange] (sol) circle (4pt);
    \draw[left color = green, right color = blue, draw=white] (Tierra) circle (2pt);
    \draw[inner color = orange, outer color = red, draw=red, rotate=90] (sistema binario) ellipse (3.5pt and 2pt);
    %Ángulo
    \pic[draw, "$\theta$", angle eccentricity=1.8, angle radius=0.3cm] {angle = sistema binario--sol--Tierra};
    %Nodos
    \node[shift={(0,-0.5)}] at (sol) {\small Sol};
    \node[shift={(-0.4,+0.25)}] at (Tierra) {\small Tierra};
    \node[shift={(0,-0.7)}, align=center] at (sistema binario) {Sistema binario};
\end{tikzpicture}
\end{document}
```
genera el siguiente diagrama: ![tikz](https://raw.githubusercontent.com/gfrubi/gfrubi.github.io/master/images/2023-05-03_20-30.png|width=300px)

Puede encontrar muchos ejemplos de diagramas creados con Tikz (y el código correspondiente) en [tikz.net](https://tikz.net/).
- El paquete Beamer también permite crear posters para conferencias. Por ejemplo, [aquí](https://www.overleaf.com/latex/templates/unofficial-poster-template-for-university-of-cambridge/mtjqrnmghxsc) hay un ejemplo de un poster en formato horizontal (seleccionar "View Source") para ver el código $\LaTeX$ ![posterH](https://raw.githubusercontent.com/gfrubi/gfrubi.github.io/master/images/26516.jpeg|width=300px)
		-
- Similarmente un ejemplo de poster en formato vertical está disponible [aquí](https://www.overleaf.com/latex/templates/portrait-beamer-poster-template-jacobs-style/fxfzyznxpghw): ![posterV](https://raw.githubusercontent.com/gfrubi/gfrubi.github.io/master/images/2205.jpeg|width=300px)

- [**MusiXTeX**](http://icking-music-archive.org/software/htdocs/): un paquete que permite escribir música en $\LaTeX$. Manual disponible [aquí](https://ctan.dcc.uchile.cl/macros/musixtex/doc/musixdoc.pdf). Por ejemplo, el codigo siguiente:
```
\begin{music}
    \parindent10mm
    \instrumentnumber{1} 
    \setname1{Piano} 
    \setstaffs1{2} 
    \generalmeter{\meterfrac44} 
    \startextract 
    \Notes\ibu0f0\qb0{cge}\tbu0\qb0g|\hl j\en
    \Notes\ibu0f0\qb0{cge}\tbu0\qb0g|\ql l\sk\ql n\en
    \bar
    \Notes\ibu0f0\qb0{dgf}|\qlp i\en
    \notes\tbu0\qb0g|\ibbl1j3\qb1j\tbl1\qb1k\en
    \Notes\ibu0f0\qb0{cge}\tbu0\qb0g|\hl j\en
    \zendextract 
\end{music}
```
genera el siguiente resultado: ![MusiXTeX](https://raw.githubusercontent.com/gfrubi/gfrubi.github.io/master/images/2023-05-03_20-15.png|width=300px)
- Puede explorar y descubrir otros paquetes en la página de [CTAN](https://ctan.org/pkg)