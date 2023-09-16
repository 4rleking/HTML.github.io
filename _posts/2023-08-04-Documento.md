---
layout: single
title: Documento HTML
excerpt: "Un documento HTML se divide en 2 partes, se habla del contenido de la cabecera y el contenido del cuerpo."
date: 2023-08-28
classes: wide
header:
  teaser: /assets/images/
  teaser_home_page: true
categories:
  - 
tags:
  - Cabecera
  - Título
  - Cuerpo
---

<center>
    <img src='./../assets/images/Documento/Intro.svg'>
</center>

El documento HTML tiene dos partes bien diferenciadas. La primera será la `cabecera del documento (head)` en la que irá información relativa a la semántica del documento, metadatos, o a los recursos que necesita para su correcta visualización.

Por otro lado, tenemos el `cuerpo (body)`. El cuerpo contendrá la estructura del documento HTML. Dentro del cuerpo iremos situando los diferentes elementos del lenguaje HTML para la correcta visualización de la página.

Pero el documento HTML se caracteriza por empezar y terminar por el elemento `<html>`. Es decir, al principio y al final del documento encontraremos el elemento de inicio y cierre respectivamente.

```text
<html>
  <!-- Documento HTML -->
</html>
```

Importante es saber que antes del primer elemento html vamos a encontrar la definición del `tipo de documento HTML (doctype)` sobre el que trabajemos. Como vimos en el capítulo [tipos de documentos HTML](https://4rleking.github.io/HTML.github.io/Tipos/) podemos tener diferentes tipos o doctypes.

De esta forma la estructura básica del documento HTML será la siguiente:

```text
<!doctype html>
<html>
  <!-- Documento HTML -->
</html>
```

## La cabecera del documento

Lo primero que encontraremos dentro del documento HTML será la cabecera. La cabecera se delimita mediante el elemento `head`.

```text
<head>
  <!-- Elementos de cabecera -->
</head>
```

Dentro de la cabecera vamos a encontrar elementos que nos definen la `semántica del documento`, estos serán las `metatags o metadatos`. Además podremos encontrar `scripts`, `hojas de estilo` y el más importante, el `título de la página`.

Es importante remarcar que el contenido que se encuentre dentro de la cabecera no tiene una representación visual directa.

## Título del documento

El título del documento se definirá utilizando el elemento `title`. Cómo contenido del elemento encontraremos el texto que represente dicho título.

La estructura sería la siguiente:

```text
<title>Título del documento</title>
```

El título del documento se suele cargar, por convenio como contenido de las pestañas de los navegadores web.

## El cuerpo del documento

El cuerpo del documento será el que contenga los elementos de la estructura. Es decir, aquellos elementos que van a dotar de contenido al documento HTML.

El cuerpo del documento se delimita mediante el elemento `body`.

```text
<body>
  <!-- Cuerpo del documento -->
</body>
```

Dentro del cuerpo del documento irán todos los elementos que vamos a ir explicando poco a poco. Con la estructura del documento HTML que hemos visto podemos ver como estructura base de cualquier documento HTML la siguiente:

```text
<!doctype html>
<html>
  <head>
    <title>Título de la Página</title>
    <meta charset=”utf-8”/>
  </head>

  <body>
    <!-- Cuerpo del documento HTML -->
  </body>
</html>
```
