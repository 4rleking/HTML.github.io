---
layout: single
title: Entidades HTML
excerpt: "Para insertar algunos caracteres, es importante saber que entidad debemos de insertar y como está conformada cada entidad que se pueda utilizar en este tipo de documentos."
date: 2023-08-24
classes: wide
header:
  teaser: /assets/images/
  teaser_home_page: true
categories:
  - 
tags:
  - Entidades (Código)
---

![](/assets/images/)

Cuando estemos insertando texto en nuestros documentos HTML puede darse el caso de que necesitemos insertar *símbolos*. Bien ya sean símbolos de la codificación que estemos utilizando o símbolos de carácter general. Esto pueden ser monedas, símbolos de puntuación, etc.

Para ello HTML nos ofrece las `entidades`. Las entidades son unas estructuras que, mediante el uso de una codificación, nos permiten representar un símbolo.

La estructura de la entidad HTML es un `ampersand(&)` seguido del código o nombre de la entidad y terminado en un punto y coma.

```
&codigo;
```

En el caso de que utilicemos los códigos, estos se anteponen de una almohadilla.

Algunos de las entidades más utilizadas son los acentos:

```
á	&aacute;
é	&eacute;
í	&iacute;
```

Los símbolos que utiliza el propio lenguaje HTML:

```
&	&amp;
<	&lt;
>	&gt;
```

U otros comunes:

```
€	&euro;
£	&pound;
©	&copy;
®	&reg;
```

## Principales entidades HTML

Para revisar las entidades de HTML puedes visitar la [lista oficial de entidades HTML](https://html.spec.whatwg.org/multipage/named-characters.html#named-character-references), la cuál es actualizada constantemente.

Existen varios sitios el cual ofrecen estos códigos, por ejemplo:

* [symbl.cc](https://symbl.cc/es/html-entities/)
* [mclibre.org](https://www.mclibre.org/consultar/htmlcss/html/html-entidades-caracter.html)
* [htmlquick.com](https://www.htmlquick.com/es/reference/character-entity-reference.html)
* [ascii.cl](https://ascii.cl/es/codigos-html.htm)
* [imd.guru](https://www.imd.guru/sistemas/html/html-entidades-utiles.html)
* [it.uc3m.es](http://www.it.uc3m.es/~amillares/Module4/entidades.html)

Además para evitar el buscar el codigo de una entidad, hay una herramienta online que codifica por tí:

* [rakko.tools](https://es.rakko.tools/tools/21/)
* [magictool.ai](https://magictool.ai/tool/html-decoder-encoder/es/)