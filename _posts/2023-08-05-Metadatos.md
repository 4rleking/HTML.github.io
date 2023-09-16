---
layout: single
title: Metadatos (Las metatags de HTML)
excerpt: "Se habla acerca de la importancia de este tipo de datos en la estructura del archivo, depende de la información que proporciones el que pueda ser de los primeros resultados en buscar en internet, o como pueda ser que nadie la encuentre."
date: 2023-08-27
classes: wide
header:
  teaser: /assets/images/
  teaser_home_page: true
categories:
  - 
tags:
  - meta
---

<center>
    <img src='./../assets/images/Metatags/Intro.svg'>
</center>

Las *metatags de HTML* nos permiten dotar de metadatos a la página HTML. Es decir, de información relativa al contenido de la página, pero que no se representa de ninguna forma. Si bien son muy importantes ya que será una parte de información que leerán los buscadores web y un correcto uso de los metadatos harán que nuestra página sea mejor o peor indexada.

Por ejemplo, podremos encontrar dentro de los metadatos, la *descripción de la página*, un conjunto palabras que describan la página, el *tipo de codificación de la página*, información relativa al *autor de la página* o con qué herramienta ha sido construida, entre otras más.

La estructura general de las meta-tags se define mediante el elemento `meta`:

```text
<meta name="metadato" content="valor" http-equiv="cabecera-http" schema="esquema"/>
```

Dentro de los metadatos podríamos diferenciarlos de tres tipos:

* `Metadatos generales`: proporcionan información relativa al documento HTML.
* `Metadatos http`: son aquellos que modifican alguna propiedad de las cabeceras http.

## Metadatos Generales

Nos permiten definir información de metadatos generales del documento: *autor*, *descripción* palabras clave, …

Es estándar HTML 4.01 no define un perfil de metadatos a utilizar y deja abierto su uso. Si bien hace referencia al Dublin Core Profile para la descripción de documentos electrónicos. Algunos de los metadatos más utilizados son:

### Author

Para hacer referencia al autor del documento. La estructura sería:

```text
<meta name="author" content="Manual Web" />
```

### Description

Define la descripción del contenido del documento a forma de resumen. Es el elemento más importante de cara al posicionamiento, ya que Google y otros buscadores lo suelen utilizar para ser mostrado en los resultados de búsqueda. Su uso sería:

```text
<meta name="description" content="Manual Web que nos explica el uso del lenguaje HTML" />
```

### Keywords

Conjunto de palabras que describen el documento. Las palabras van separadas por comas.

Un ejemplo podría ser “coches, coches deportivos, coches de lujo”. Aunque en su momento esta etiqueta tuvo importancia, actualmente buscadores como Google ignoran esta información, ya que solía ser utilizada para incluir datos no relacionados con la página.

Se escribiría de la siguiente forma:

```text
<meta name="keywords" content="manual, html, elementos, atributos, ejemplos" />
```

### Revised

Información relativa a cuándo el documento fue revisado por última vez. Se utilizará de la siguiente forma:

```text
<meta name="revised" content="24/03/2016" />
```

### Copyright

Información sobre el copyright de la página.

```text
<meta name="copyright" content="Propietario del copyright" />
```

### Generator

Indica con qué herramienta se ha desarrollado la página, si es que se ha utilizado alguna en específico.

Por ejemplo, un valor para este elemento podría ser “WordPress”.

### Robots

Con esta etiqueta podremos definir las acciones que pueden tomar los robots de los motores de búsqueda en nuestra página web.

Podemos usar valores como `Disallow` y `Allow` en el `Robots.txt` de WordPress para que los robots accedan o no al contenido de las URLs que van encontrando.

* Index

Esta directriz permite al robot de búsqueda la indexación de una página de HTML, algo innecesario si se piensa que la indexación forma parte de su actividad habitual, así:

```text
<meta name="robots" content="index"/>
```

* Noindex

Se tiene que indicar expresamente si una página no debe ser incluida en el índice. Este tag prohíbe al buscador transferir contenidos de una página HTML a su base de datos:

```text
 <meta name="robots" content="noindex"/>
 ```

El atributo `“robots”` se dirige a todos los buscadores, y `“noindex”` indica que no se permite la indexación. Si queremos impedirle el proceso solo a un buscador, podemos indicarlo con un atributo alternativo como, por ejemplo, `“googlebot”`.

* Follow

El comportamiento estándar de los motores de búsqueda consiste en recorrer los enlaces que encuentra en una página de HTML, a no ser que se les indique lo contrario. Esta información se puede incluir en las metaetiquetas, aunque no es necesario:

```text
<meta name="robots" content="follow"/>
 ```

* Nofollow

Si se quiere impedir que un robot de búsqueda alcance determinadas subpáginas de un sitio o rastree los enlaces en otro dominio se añade:

```text
<meta name="robots" content="nofollow"/>
```

El robot ignora, así, los enlaces por completo, pero no el contenido de la página, que sí será transferido a la base de datos del buscador.

Los meta tags `Index`/`Noindex` y `Follow`/`Nofollow` se pueden usar solos o combinados. Se puede, por ejemplo, determinar que una página sea indexada pero que los links sean ignorados, así como permitir o impedir ambas acciones a los robots.

```text
<meta name="robots" content="index,nofollow" />
<meta name="robots" content="index,follow" />
<meta name="robots" content="noindex,nofollow" />
```

Todas las etiquetas meta son opcionales, de forma que la página seguirá funcionando correctamente aunque no tengamos ninguna.

De hecho, lo normal es que no tengamos todas ellas.

Eso sí, algunas son muy importantes para mejorar el posicionamiento de nuestra web, en especial la etiqueta *description*.

## Metadatos Cabeceras HTTP

Las *cabeceras http* suelen ser establecidas en el servidor, si bien podemos modificarlas en el cliente mediante las *meta-tags*. El navegador realizará alguna acción al interpretar estas cabeceras. Por ejemplo, podemos decirle al navegador cada cuanto tiempo tiene que recargar la página, o durante cuánto tiempo debe de cachear la página.

Estos metadatos se apoyan en el atributo *http-equiv*.

### Refresh

Especifica cada cuanto tiempo tiene que recargar la página el navegador web. El tiempo es en *segundos*.

```
<meta http-equiv="refresh" content="5" />
```

Incluso podemos utilizar este tipo para hacer una redirección a otra página.

```
<meta http-equiv="refresh" content="2; http://lineadecodigo.com" />
```

### Content-type

Nos sirve para identificar el tipo de documento, que será un documento de tipo *text/html* y la codificación del contenido. Si es *ISO 8859-1*, *UTF-8*, … Esto servirá al navegador a interpretar los caracteres que vayan dentro del contenido.

#### UTF-8

```
<meta http-equiv=”Content-Type” content=”text/html; charset=UTF-8″ />
```

#### ISO-8859-1

```
<meta http-equiv=”Content-Type” content=”text/html; charset=ISO-8859-1″ />
```

### Cookie

Nos sirve para guardar una cookie. Los datos guardados son clave/valor

```
<meta http-equiv="cookie" content="clave=valor; expires=Saturday, 25-Mar-16 23:59:59 GMT;" />
```

## Metadatos y el Open Graph Protocol

Como hemos comentado anteriormente la especificación *HTML 4.01* no habla de un perfil de metadatos. Es por ello que hay diferentes perfiles que están proliferando diferentes perfiles que nos permiten metadatar el documento con algún fin. Uno de esos perfiles es el *Open Graph Protocol*, este perfil es utilizado, entre otros, por Facebook para poder interpretar el documento de una forma más sencilla. Algunos de los metadatos que define el Open Graph Protocol son:

### og:title

Define el título del documento.

```
<meta name="og:title" content="Manual Web. Manuales en Español" />
```

### og:type

Indica el tipo de objeto que representa la página. Si es un artículo, un vídeo, una imagen,…

```
<meta name="og:type" content="article" />
```

### og:image

Permite establecer la imagen más representativa del documento

```
<meta name="og:image" content="http://www.manualweb.net/logo.png" />
```

### og:url

Nos ayuda a definir la URL asociada al documento. Esto es por si queremos utilizar alguna diferente a la URL que ya tenga.

```
<meta name="og:url" content="http://www.manualweb.net" />
```