---
layout: single
title: Tablas Básicas HTML
excerpt: ""
date: 2023-08-16
classes: wide
header:
  teaser: /assets/images/
  teaser_home_page: true
categories:
  - 
tags:
  - Tablas Básicas
---

<center>
    <img src='./../assets/images/Tablas/TablasBasicas.jpg'>
</center>

## Poner título a la tabla

Ahora que conocemos cómo se construye una tabla básica con HTML vamos a ir viendo qué posibilidades adicionales tenemos sobre las tablas.

Lo primero que haremos será poner un título a la tabla. Para ello vamos a utilizar el elemento `caption`. El contenido del elemento caption será el título que le asignemos a la tabla.

Añadimos el elemento caption antes de cualquier definición de filas dentro de la tabla.

Así, el código para poner el título a la tabla sería:

```
<table>
<caption>Mi tabla de ejemplo</caption>
  <tr>
    <td>Fila 1 Columna 1</td>
    <td>Fila 1 Columna 2</td>
    <td>Fila 1 Columna 3</td>
    <td>Fila 1 Columna 4</td>
  </tr>
</table>
```

## Resumen de la tabla

Aunque el título suele ser el elemento descriptivo de la tabla existe un atributo a nivel del elemento table de especial importancia. Este es el atributo `summary`. El atributo summary nos permite adjuntar un resumen de la información que contiene la tabla.

Este atributo será de gran interés para cuando nuestras páginas web sean interpretadas por programas para discapacitados, ya que la información que contiene una tabla suele ser de difícil interpretación.

Es por ello que es muy recomendable que siempre añadamos un resumen a nuestra tabla.

El código es tan sencillo como este:

```
<table summary="Tabla que contiene datos de ejemplo para poder explicar como construir tablas con el lenguaje HTML">
<caption>Mi tabla de ejemplo</caption>
  <tr>
    <td>Fila 1 Columna 1</td>
    <td>Fila 1 Columna 2</td>
    <td>Fila 1 Columna 3</td>
    <td>Fila 1 Columna 4</td>
  </tr>
</table>
```

## Definiendo Una Cabecera en la Tabla

Una cosa que vemos es que las tablas suelen tener una primera fila de encabezado. Dentro de las tablas en HTML podemos identificar esta fila mediante el elemento `th`. Es decir, para las celdas de la fila de cabecera en vez de utilizar un elemento `td` utilizaremos un elemento `th`.

Así, la cabecera de una tabla quedará de la siguiente forma:

```
<table>
  <tr>
    <th>Cabecera 1</th>
    <th>Cabecera 2</th>
    <th>Cabecera 3</th>
  </tr>
  <tr>
    <td>Fila 1 Columna 1</td>
    <td>Fila 1 Columna 2</td>
    <td>Fila 1 Columna 3</td>
  </tr>
</table>
```

## El atributo scope

Hay celdas de cabecera que necesiten una pequeña explicación sobre si la información que representan es la de las columnas o la de las filas. Suele suceder, normalmente, con la primera celda.

Para resolver este problema tenemos el atributo `scope`. El atributo scope solo se puede aplicar a las celdas de una cabecera. Y sus valores son: `col`, `row`, `colgroup` o `rowgroup`.

De esta forma si queremos que esta celda sea representativa de columnas la definiremos como:

```
<td scope="col">Contenido de la Celda</td>
```

## Agrupando Celdas

A la hora de presentar datos en una tabla nos puede surgir la necesidad de agrupar celdas, ya que el contenido a presentar refleja una agrupación de datos.

Imaginemos una tabla que nos saca los ingresos y gastos por meses. Existirá una columna con el mes, la cual agrupará dos columnas: ingresos y gastos.

Algo como lo siguiente:

<table>
  <tr>
    <td colspan="2">Enero</td>
    <td colspan="2">Febrero</td>
  </tr>
  <tr>
    <td>Ingresos</td>
    <td>Gastos</td>
    <td>Ingresos</td>
    <td>Gastos</td>
  </tr>
  <tr>
    <td>1.000€</td>
    <td>700€/td>
    <td>1.100€</td>
    <td>580€</td>
  </tr>
  <tr>
    <td>1.800€</td>
    <td>920€</td>
    <td>1.750€</td>
    <td>920€</td>
  </tr>
</table>

En este caso lo que estamos diciendo es que una celda ocupa dos espacios. Para ello vamos a utilizar el atributo `colspan` sobre el elemento `td` de la celda.

Así indicaremos que el colspan de esa celda es 2. Ya que ocupa dos celdas.

```
<td colspan="2">Enero</td>
```

El código completo sería:

```
<table>
  <tr>
    <td colspan="2">Enero</td>
    <td colspan="2">Febrero</td>
  </tr>
  <tr>
    <td>Ingresos</td>
    <td>Gastos</td>
    <td>Ingresos</td>
    <td>Gastos</td>
  </tr>
  <tr>
    <td>1.000€</td>
    <td>700€/td>
    <td>1.100€</td>
    <td>580€</td>
  </tr>
  <tr>
    <td>1.800€</td>
    <td>920€</td>
    <td>1.750€</td>
    <td>920€</td>
  </tr>
</table>
```

De igual manera nos puede suceder en sentido horizontal. Es decir, que queramos que una celda ocupe dos filas.

Si lo vemos sobre nuestro ejemplo veremos que podemos añadir una columna que simplemente ponga que los valores numéricos tengan el literal *“Datos Económicos”*. En este caso tendremos que indicar que esa celda ocupa dos filas.

<table>
  <tr>
    <td></td>
    <td colspan="2">Enero</td>
    <td colspan="2">Febrero</td>
  </tr>
  <tr>
    <td rowspan="3">Datos Económicos</td>
    <td>Ingresos</td>
    <td>Gastos</td>
    <td>Ingresos</td>
    <td>Gastos</td>
  </tr>
  <tr>
    <td>1.000€</td>
    <td>700€/td>
    <td>1.100€</td>
    <td>580€</td>
  </tr>
  <tr>
    <td>1.800€</td>
    <td>920€</td>
    <td>1.750€</td>
    <td>920€</td>
  </tr>
</table>

Para la agrupación de filas tenemos otro atributo que es `rowspan`. Este atributo, al igual que `colspan` se aplica sobre la celda td

```
<td rowspan="3">Datos Económicos</td>
```

El código completo de la tabla sería el siguiente:

<table>
  <tr>
    <td></td>
    <td colspan="2">Enero</td>
    <td colspan="2">Febrero</td>
  </tr>
  <tr>
    <td rowspan="3">Datos Económicos</td>
    <td>Ingresos</td>
    <td>Gastos</td>
    <td>Ingresos</td>
    <td>Gastos</td>
  </tr>
  <tr>
    <td>1.000€</td>
    <td>700€/td>
    <td>1.100€</td>
    <td>580€</td>
  </tr>
  <tr>
    <td>1.800€</td>
    <td>920€</td>
    <td>1.750€</td>
    <td>920€</td>
  </tr>
</table>