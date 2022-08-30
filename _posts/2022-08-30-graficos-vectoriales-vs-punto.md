---
title: 'Sobre Gráficos de Mapas de Bits y Gráficos vectoriales'
date: 2022-08-30
tags:
  - software
---
A la hora de incluir un gráfico en algún texto (por ejemplo, en un artículo científico escrito usando $\LaTeX$) es importante conocer las diferencias entre formatos de gráficos de mapas de bits ("bitmaps", o "gráficos rasterizados") y vectoriales, y qué tipo de gráfico hay que usar dependiendo del objetivo que se persiga, ya que usar el tipo de gráfico equivocado tiene consecuencias en la calidad del resultado final...

Los formatos de mapas de bits (.jpg, .gif, .png, .tif, .bmp, ...) están diseñados para almacenar imágenes (típicamente fotografías) sin tomar en cuenta una posible estructura, ya que la información almacenada en el archivo corresponde a la de los colores, intensidad, etc. de cada uno de los puntos que constituyen la imagen. Por esto, estos formatos necesariamente requieren especificar una determinada resolución (el número de puntos, píxeles, que constituyen la imagen. Por ejemplo, 800×600 ó 1920×1080).

Por otro lado, los formatos de gráficos vectoriales (.svg, .odg, .ps, .eps, .pdf) están diseñados especialmente para almacenar la estructura del gráfico, en forma independiente de una resolución. Por esto, este tipo de formato gráfico es ideal para almacenar diagramas o esquemas, así como texto (usando fuentes tipográficas).

Entonces... lo que no hay que hacer es crear gráficos que correspondan a diagramas o esquemas usando software diseñado para editar gráficos de mapas de bits. También debe evitarse crear diagramas con programas diseñados para producir gráficos vectoriales, pero finalmente exportar el resultado en un formato de mapa de bits. En ambos casos, el resultado será un mapa de bits del diagrama. ¿Por qué es esto importante?. Porque el resultado no es óptimo debido a la pixelación y a la degradación de la imagen si además se usan formatos con compresión (.jpg, .png, .gif). Este tipo de problemas se evidencian fácilmente al ampliar (zoom) el resultado final.

## Referencias:

* [Gráficos de Mapas de Bits](http://es.wikipedia.org/wiki/Gr%C3%A1ficos_rasterizados) (Wikipedia).
* [Gráficos Vectoriales](http://es.wikipedia.org/wiki/Gr%C3%A1fico_vectorial) (Wikipedia).
