---
layout: single
title: Metadatos (Las metatags de HTML)
excerpt: ""
date: 2023-08-27
classes: wide
header:
  teaser: /assets/images/20230802/Intro.png
  teaser_home_page: true
categories:
  - Programación
tags:
  - Fundamentos
---

Las *metatags de HTML* nos permiten dotar de metadatos a la página HTML. Es decir de información relativa al contenido de la página, pero que no se representa de ninguna forma. Si bien son muy importantes ya que será una parte de información que leerán los buscadores web y un correcto uso de los metadatos harán que nuestra página sea mejor o peor indexada.

Por ejemplo podremos encontrar dentro de los metadatos, la *descripción de la página*, un conjunto palabras que describan la página, el *tipo de codificación de la página*, información relativa al *autor de la página* o con qué herramienta ha sido construida, entre otras más.

La estructura general de las meta-tags se define mediante el elemento meta:

~~~
<meta name="metadato" content="valor" http-equiv="cabecera-http" schema="esquema"/>
~~~

Dentro de los metadatos podríamos diferenciarlos de tres tipos:

* **Metadatos generales**: proporcionan información relativa al documento HTML.
* **Metadatos http**: son aquellos que modifican alguna propiedad de las cabeceras http.

## Metadatos Generales

Nos permiten definir información de metadatos generales del documento: *autor*, *descripción* palabras clave,… 

Es estándar HTML 4.01 no define un perfil de metadatos a utilizar y deja abierto su uso. Si bien hace referencia al Dublin Core Profile para la descripción de documentos electrónicos. Algunos de los metadatos más utilizados son:

### Author

Para hacer referencia al autor del documento. La estructura sería:

~~~
<meta name="author" content="Manual Web" />
~~~

### Description

Define la descripción del contenido del documento a forma de resumen. Su uso sería:

~~~
<meta name="description" content="Manual Web que nos explica el uso del lenguaje HTML" />
~~~

### Keywords

Conjunto de palabras que describen el documento. Las palabras van separadas por comas. Se escribiría de la siguiente forma:

~~~
<meta name="keywords" content="manual,html,elementos,atributos,ejemplos" />
~~~

### Revised

Información relativa a cuándo el documento fue revisado por última vez. Se utilizará de la siguiente forma:

~~~
<meta name="revised" content="24/03/2016" />
~~~

## Metadatos Cabeceras HTTP

Las *cabeceras http* suelen ser establecidas en el servidor, si bien podemos modificarlas en el cliente mediante las *meta-tags*. El navegador realizará alguna acción al interpretar estas cabeceras. Por ejemplo podemos decirle al navegador cada cuanto tiempo tiene que recargar la página, o durante cuánto tiempo debe de cachear la página.

Estos metadatos se apoyan en el atributo *http-equiv*.

### Refresh

Especifica cada cuanto tiempo tiene que recargar la página el navegador web. El tiempo es en *segundos*.

~~~
<meta http-equiv="refresh" content="5" />
~~~

Incluso podemos utilizar este tipo para hacer una redirección a otra página.

~~~
<meta http-equiv="refresh" content="2; http://lineadecodigo.com" />
~~~

### Content-type

Nos sirve para identificar el tipo de documento, que será un documento de tipo *text/html* y la codificación del contenido. Si es *ISO 8859-1*, *UTF-8*,… Esto servirá al navegador a interpretar los caracteres que vayan dentro del contenido.

#### UTF-8

~~~
<meta http-equiv=”Content-Type” content=”text/html; charset=UTF-8″ />
~~~

#### ISO-8859-1

~~~
<meta http-equiv=”Content-Type” content=”text/html; charset=ISO-8859-1″ />
~~~

### Cookie

Nos sirve para guardar una cookie. Los datos guardados son clave/valor

~~~
<meta http-equiv="cookie" content="clave=valor; expires=Saturday, 25-Mar-16 23:59:59 GMT;" />
~~~

## Metadatos y el Open Graph Protocol

Como hemos comentado anteriormente la especificación HTML 4.01 no habla de un perfil de metadatos. Es por ello que hay diferentes perfiles que están proliferando diferentes perfiles que nos permiten metadatar el documento con algún fin. Uno de esos perfiles es el *Open Graph Protocol*, este perfil es utilizado, entre otros, por Facebook para poder interpretar el documento de una forma más sencilla. Algunos de los metadatos que define el Open Graph Protocol son:

### og:title

Define el título del documento.

~~~
<meta name="og:title" content="Manual Web. Manuales en Español" />
~~~

### og:type

Indica el tipo de objeto que representa la página. Si es un artículo, un vídeo, una imagen,…

~~~
<meta name="og:type" content="article" />
~~~

### og:image

Permite establecer la imagen más representativa del documento

~~~
<meta name="og:image" content="http://www.manualweb.net/logo.png" />
~~~

### og:url

Nos ayuda a definir la URL asociada al documento. Esto es por si queremos utilizar alguna diferente a la URL que ya tenga.

~~~
<meta name="og:url" content="http://www.manualweb.net" />
~~~