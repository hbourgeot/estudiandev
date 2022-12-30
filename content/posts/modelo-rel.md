+++
title = "Modelo Relacional"
date = "2022-11-19T10:17:30-04:00"
author = "Henrry Bourgeot"
authorTwitter = "estudiandev" #do not include @
cover = ""
tags = ["modelo relacional", "base de datos", "sistemas", "relacion", "bd"]
keywords = ["modelo relacional", "base de datos", "sistemas", "relacion", "bd"]
categories = ["bases de datos", "universidad"]
description = "En este post, encontrarás teoría relacionada al **modelo relacional** y también las reglas asociadas a dicho modelo para convertir un [modelo entidad-relacion](//modelo-entidad-relacion) a un modelo relacional."
color = "blue" #color from the theme settings
+++

En este post, encontrarás teoría relacionada al **modelo relacional** y también las reglas asociadas a dicho modelo para convertir un [modelo entidad-relacion](//modelo-entidad-relacion) a un modelo relacional.

## ¿En qué consiste?

Este modelo consiste en representar datos por medio de tablas, de las cuales las filas son llamadas como tuplas, y las columnas como variables. Además, se basan en la teoría de conjuntos y lógica de predicados.

Además, este **modelo de datos lógico** fue creado por Codd en 1970.

## Visión general

Las estructuras consisten en **tablas**, cuyas columnas serían **atributos** de tipo atómico, y las filas corresponden a **registros de datos**. Además, las operaciones están fundamentalmente orientadas al manejo de tablas como unos conjuntos de registros.

## Notación para relaciones

Esta notación, es utilizada para \*\*convertir un modelo entidad-relación a un modelo relacional. Este modelo se denota como:

```js
Relacion(Atributo1, Atributo2, ...AtributoN);
```

A continuación verás más ejemplos de cómo se denotan cuando veas las reglas.

## Regla #1

> - Para cada entidad regular se utiliza un esquema de relación.
> - Para cada atributo compuesto se consideran sus componentes.
> - La clave de la entidad es la clave del esquema de relación.

### Ejemplo ER Regla #1

![Regla nro. 1](/img/regla1.png)

### Ejemplo Esquema de Relación de la regla #1

```js
Empleado(codigo, direccion_calle, direccion_numero, sueldo, telefono);
```

## Regla #2

> - Para cada tipo de entidad débil se crea un esquema de relación.
> - Los atributos se manejan por la regla #1
> - La clave del esquema está formada por la clave parcial de la entidad débil más la clave de la entidad que la identifica, es decir, la entidad fuerte.

### Ejemplo ER Regla #2

![Regla nro. 2](/img/regla2.png)

### Ejemplo Esquema de Relación de la regla #2

```js
Empleado(codigo, apellemp, sueldo);
Dependiente(codigo, codigodep, fecnac);
```

## Regla #3

> Para cada tipo de relación `1:1` entre dos entidades, se elige una de ellas para incluir la clave primaria del otro. Además, es preferible elegir la que participa totalmente.

### Ejemplo ER Regla #3

![Regla nro. 3](/img/regla3.png)

### Ejemplo Esquema de Relación de la regla #3

```js
Departamento(nrodept, codigo, nombredept);
Empleado(codigo, apellemp, sueldo);
```

## Regla #4

> Para cada tipo de relación `1:N` se incluye la clave primaria de la entidad con cardinalidad `1` en la entidad con cardinalidad `N`

### Ejemplo ER de la regla #4

![Regla nro. 3](/img/regla4.png)

### Ejemplo Esquema de Relación de la regla #4

```js
Departamento(nrodept, nombredept);
Empleado(codigo, apellemp, sueldo, nrodept);
```

## Regla #5

> Para cada tipo de Relación N:N se cfea un esquema de relación donde la clave está formada por la clave de las dos entidades que participan en la relación.

## Ejemplo ER de la regla #5

![Regla nro. 5](/img/regla5.png)

### Ejemplo Esquema de Relación de la regla #5

```js
Proyecto(nroproy, nomproy);
Empleado(codigo, nombre, direccion_calle, direccion_numero);
ProyectoEmpleado(nroproy, codigo, horasem);
```

## Regla #6

> Para cada tipo de entidad que incluya un atributo multivaluado se crea un esquema de relación donde la clave de la entidad más el atributo multivaluado.

## Ejemplo ER de la regla #6

![Regla nro. 6](/img/regla6.png)

### Ejemplo de Esquema de Relación de la regla #6

```js
Empleado(codigo, nombre, direccion_calle, direccion_numero, telefono);
EmpleadoTelf(codigo, telefono);
```

## Regla #7

> Para cada tipo de interrelación `R` de grado > 2 se crea un esquema de relación que representa en `R`, cuya clave primaria la forma por claves primarias de las entidades que participan en la interrelación `R` incluyendo a los atributos simples propios de la interrelación.

## Ejemplo ER de la regla #7

![Regla nro. 7](/img/regla7.png)

### Ejemplo de Esquema de Relación de la regla #7

```js
Proveedor(codprov, nomprov);
Proyeccto(numproy, nombre);
Componente(codigocomp, nombrecomp);
Suministrar(codprov, numproy, codigocomp, cantidad);
```
