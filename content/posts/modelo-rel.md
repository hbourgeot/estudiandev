+++
title = "Modelo Relacional en Base de Datos"
date = "2022-11-19T10:17:30-04:00"
author = "Henrry Bourgeot"
authorTwitter = "estudiandev" #do not include @
cover = ""
tags = ["programacion", "base de datos"]
keywords = ["", ""]
description = "En este post encontraras las reglas asociadas al modelo relacional, aunque no se utilicen mucho actualmente, puede que necesites información sobre estas, y aquí la tendrás"
showFullContent = false
hideComments = false
color = "blue" #color from the theme settings
+++

En este post, encontrarás las reglas asociadas al **modelo relacional**, específicamente, son 7 reglas asociadas.

**PD: Esto no se usa actualmente, pero existen ciertos profesores que están desactualizados y capaz te manden este tema.**

## Regla #1

> - Para cada entidad regular se utiliza un esquema de relación.
> - Para cada atributo compuesto se consideran sus componentes.
> - La clave de la entidad es la clave del esquema de relación.

### Ejemplo ER Regla #1

![Regla nro. 1](/img/regla1.png)

## Regla #2

> - Para ada tipo de entidad débil se crea un esquema de relación.
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

> Para cada tipo de entidad que inluya un atributo multivaluado se crea un esquema de relación donde la clave de la entidad más el atributo multivaluado.

### Ejemplo de Esquema de Relación de la regla #6

```js
Empleado(codigo, nombre, direccion_calle, direccion_numero, telefono);
EmpleadoTelf(codigo, telefono);
```

## Regla #7

> Para cada tipo de interrelación `R` de grado > 2 se crea un esquema de relación que representa en `R`, cuya clave primaria la forma por claves primarias de las entidades que participan en la interrelación `R` incluyendo a los atributos simples propios de la interrelación.

### Ejemplo de Esquema de Relación de la regla #7

```js
Proveedor(codprov, nomprov);
Proyeccto(numproy, nombre);
Componente(codigocomp, nombrecomp);
Suministrar(codprov, numproy, codigocomp, cantidad);
```
