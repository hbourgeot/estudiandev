---
title: 'Tipos y Estructuras de Datos'
date: 2022-10-25T17:31:12-04:00
draft: false
author: 'Henrry Bourgeot'
categories: [estructuras de datos, universidad]
tags: [estructuras, universidad, datos, variables]
---

## Tipos de Datos

### Qué son?

Son definidos como un conjunto de valores que una variable definida puede tomar además de las operaciones que se pueden ejercer sobre la variable o con esta. En [amplitud.com](https://amplitude.com/blog/data-types) lo definen como un atributo asociado con un
dato que le dice a un sistema computacional cómo se debe interpretar el valor de este.

### Características

1. El término tipo de dato es usado comúnmente en la programación, ya que las variables son asignadas a un tipo de dato como se mencionó anteriormente en la definición
2. Los nombres de los tipos de datos usados no hacen alguna referencia a algún nombre que pertenezca a un lenguaje de programación específico. Esto quiere decir que Los tipos de datos como 'int' o `string', por ejemplo, están en todos los lenguajes de programación, externamente su nombre podría variar, pero internamente deben funcionar igual.

### Clasificación

Los tipos de datos se dividen principalmente en dos tipos, que posteriormente se subdividen:

- Simples:
  - Numéricos:
    1. Enteros.
    2. Reales (comúnmente conocidos como flotantes).
  - No Numéricos:
    1. Caracteres (`char` o `string` aunque este último está compuesto del primero).
    2. Lógicos (`true` y `false`).
- Estructurados:
  - Cadenas.
  - Registros:
    - Estáticos:
      - Arreglos:
        - Unidimensionales.
        - Bidimensionales.
  - Dinámicos:
    - Listas.
    - Pilas.
    - Colas.
    - Arboles.

## Estructuras de Datos

### ¿Qué son?

Las estructuras de datos se refieren a una colección definida de entidades que pertenecen a tipos de datos que son diferentes y dan como resultado una organización de pieza
de datos interrelacionadas. En [geeksforgeeks.org](https://www.geeksforgeeks.ora/dat
a-structures/) los definen como un espacio de almacenamiento que es usado para almacenar Y organizar datos, que puede ser accedida y actualizada eficientemente.

### Tipos

Las estructuras de datos poseen dos tipos, **estáticas y dinámicas**.

#### Estructuras Estáticas

Son aquellos en los que se sabe el tamaño que va a ocupar en memoria, por lo que son definidos previamente de la ejecución del programa.Es importante conocer que una vez definido el tamaño ocupado, no se puede modificar este mientras que el programa esté en ejecución, esto es lo que sucede con los arreglos y matrices.

Las estructuras estáticas son conformadas por los **arreglos y matrices**, que seguramente ya conoces y has trabajado con ellos, sin embargo es necesario recalcar la definición de estos.

1. Arreglos: secuencia de posiciones de memoria central, a los que se puede acceder directamente. Como es de costumbre y visto en todos los lenguajes de programación, contienen datos del mismo tipo (no como en JavaScript, que puedes tener un array con texto, números y booleanos), además, pueden ser seleccionados individualmente utilizando los subíndices.
2. Matrices: es literalmente, un **arreglo con dos o más dimensiones** , se caracteriza por mantener sus elementos relacionados entre si organizadamente. Estos elementos pueden ser seleccionados mediante instrucciones dadas por el programador, aunque también se pueden usar subíndices.

### Estructuras Dinámicas

A diferencia de las estructuras de datos estáticas, no cuentan con las mismas limitaciones o restricciones en el tamaño de memoria utilizada. Son definidas como aquellas que no se encuentran directamente soportadas por los lenguajes de programación. Cabe destacar que tienen ciertas operaciones que son definidas sobre estas mismas.

Por esto mismo, la categoría [estructuras de datos](/categories/estructuras-de-datos)
se basará en estas, las **Estructuras de Datos Dinámicas** y cómo se implementan en el
lenguaje de programación C y tal vez en Go.

**_P.D_**: Existen varios que las componen, a medida que avance en el 5to semestre las
iré colocando, ya que hasta el momento únicamente he visto listas.

Ya que son extensas, te adjuntaré posts de estos mismos, ya que son largos:

1. [Listas](/posts/listas)

### Rol

Las estructuras de datos poseen rol significativo en la resolución de problemas y en el diseño de programas, aquí te detallo algunos puntos de por qué es tan importantes:

- La selección de estas que se pueden emplear para la resolución de un problema específico es una de las mayores fuentes de variabilidad en el diseño de algoritmos.
- La selección de una estructura puede incidir sobre la facilidad (o no) con la cual un algoritmo se puede escribir.
- Al elegir una estructura de datos existe la posibilidad de aumentar o disminuir el requerimiento de espacio de almacenamiento además de otros recursos en una computadora.
- Del mismo modo puede aumentar o disminuir el tiempo de ejecución del programa.
- Los algoritmos y las estructuras de datos van de la mano con los principales bloquesde construcción de programas
