---
layout: single
title: Agrupaciones HTML
excerpt: ""
date: 2023-08-18
classes: wide
header:
  teaser: /assets/images/
  teaser_home_page: true
categories:
  - 
tags:
  - Agrupaciones
---

![](/assets/images/)

Hasta ahora hemos visto cómo insertar diferentes elementos sobre un documento HTML. Estos elementos se irán mostrando según la secuencia en la que hayamos escrito el documento HTML.

Una de las cosas que tenemos que saber de los elementos html es si son *elementos de bloque* o *elementos de línea*.

Un `elemento de bloque` es aquél que una vez utilizado aparece en la siguiente línea y ocupa todo el ancho. Elementos de tipo bloque son los párrafos `p`, los formularios `form`, o las cabeceras `hx`.

Un `elemento en línea` es aquel que se muestra justo a continuación del anterior elemento. Estos elementos serían los enlaces `a`, imágenes `img`,…

El lenguaje HTML nos permite agrupar un conjunto de elementos mediante una agrupación en bloque o una agrupación en línea.

## Agrupaciones en Bloque

Un elemento en bloque siempre empieza con una línea y su tamaño será igual al ancho disponible. El ancho disponible inicialmente es el de la página.

El elemento que nos permite realizar agrupaciones en bloque es el elemento `div` o más conocidos como capas. La estructura del elemento div es:

```
<div>
<!-- Contenido de la Capa -->
</div>
```

Los elementos en bloque pueden contener a otros elementos en bloque o bien a otros elementos en línea.

Por ejemplo podríamos agrupar en un bloque el siguiente contenido.

```
<div id="micapa">
  <h2>Título del Contenido</h2>
    Este es el contenido del artículo
    <img src="logo.jpg" />
    <p>Más contenido del artículo</p>
</div>
```

## Agrupaciones en Línea

Para poder realizar agrupaciones en línea tenemos el elemento `span`. La estructura del elemento span será:

```
<span> <!-- Contenido --></span>
```

Las agrupaciones en línea sólo pueden contener a otros elementos en línea, no a elementos de tipo bloque.

Por ejemplo podríamos tener la siguiente agrupación en línea.

```
<span id="entrada">
  <strong>Articulo Nuevo</strong>,
  <em>,12 de marzo de 2016</em>
</span>
```

Es muy normal que los agrupadores, ya sean o bien `div`, o bien `span` lleven el atributo `id` o `class`, ya que a posteriori serán manipulados mediante hojas de estilo CSS utilizando dichos identificadores.