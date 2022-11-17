---
title: 'Listas'
date: 2022-10-25T17:37:24-04:00
draft: false
author: 'Henrry Bourgeot'
categories: [estructuras de datos, universidad]
cover: 'img/listas.png'
tags: [estructuras, universidad, datos, variables, listas]
keywords:
  [
    programacion,
    listas,
    estructuras de datos,
    datos,
    universidad,
    tda,
    datos abstractos,
  ]
definition: 'Las listas enlazadas son una colección lineal de elementos de datos que son llamados nodos. Puedes aprender más en este post sobre ellos'
---

Existen dos tipos de Listas, los cuales son **Enlazadas, Circularmente Enlazadas y Doble Enlazadas**. Sin embargo por los momentos verás el primer mencionado.

## Listas Enlazadas

### ¿Qué son?

Las listas enlazadas son una colección lineal de elementos de datos que son llamados nodos. Cada nodo consta de dos partes, una parte contiene la información, y otra contiene un puntero que apunta al siguiente nodo. Como referencia, en [tutorialspoint.com](https://www.tutorialspoint.com/data_structures_algorithms/linked_list_algorithms.htm) definen a las listas enlazadas como una secuencia de enlaces que contienen objetos. Además, agregan que cada enlace contiene una conexión a otro enlace.

Es importante hacer mención a que es la segunda estructura de datos más usada, justamente está después del arreglo. ¿Ya ves lo importante que es aprender estas?

En la portada del post, puedes apreciar una imagen de cómo es la representación de una lista enlazada.

### Características

- Son mucho más flexibles que otras listas que fueron creadas anteriormente, ya que la inserción o borrado del elemento N no requiere el desplazamiento de los otros elementos de la misma lista.
- Los elementos son almacenados en posiciones de memoria que no son continuas o adyacentes, por ello es que emplean la dirección del siguiente nodo en la parte del puntero.
- El valor `null` en la lista es usado en casi todas las operaciones para poder detectar cuando termina esta.
- Normalmente se mantienen en un orden particular, que puede ser ascendente o descendente para números y un orden lexicográfico para datos de tipo `string`.
- Al igual que contienen punteros al final del nodo, las listas enlazadas contienen una cabecera que nos permite reconocer el inicio de estas. Si la iniciamos con `null`, nos indica que está vacía.

### Operaciones

En una lista enlazada, puedes realizar las siguientes operaciones:

- Insertar elementos.
- Borrar elementos.
- Modificar elementos.
- Encontrar elementos.

## Listas en C

Las listas se componen de la siguiente manera:

```c
 struct nodo {
     int data;
     struct nodo *next;
   }
```

Un ejemplo de la vida cotidiana sería:

```c
 struct nodo {
     int estudiante_id;
     string estudiante_nombre;
     struct nodo *next;
   }
```

Y así se crearía una lista enlazada:

```c
 struct nodo* CrearLista(){
     struct nodo *L = (struct nodo*)malloc(sizeof(struct nodo));
     L->next = null;
     return L;
   }
```

Si accedes a [este enlace](https://github.com/hbourgeot/ejercicios-cpp/blob/main/listas.cpp) podrás observar un ejercicio en el que se implementa una lista enlazada definida por el propio lenguaje C++.
