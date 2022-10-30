+++
title = "Introducción al Backend"
date = "2022-10-28T20:02:10-04:00"
author = "Henrry Bourgeot"
authorTwitter = "estudiandev" #do not include @
description = "Seguramente, entraste a este post buscando orientarte sobre backend: qué lenguaje aprender, qué base de datos usar, pero no, aquí no verás tanto eso, más bien este post se concentra en las bases del backend, por lo que aquí, encontrarás lo que vas a aprender al desarrollar la parte del servidor de una web."
cover = ""
tags = ["backend", "desarrollo web", "cursos", "Platzi"]
color = "green" #color from the theme settings
+++

Seguramente, entraste a este post buscando orientarte sobre backend: qué lenguaje aprender, qué base de datos usar, pero no, aquí no verás tanto eso, más bien este post se concentra en las bases del backend, por lo que aquí, encontrarás lo que vas a aprender al desarrollar la parte del servidor de una web.

Antes de continuar, tengo que hacer énfasis en que estos son mis apuntes del **Curso de Introducción al Backend** de Platzi

## Framework Vs Librería

Antes de continuar, es sumamente necesario conocer la diferencia entre estos dos, que es fundamental para todo lo que tenga que ver con programación. Un _framework_ es un conjunto de librerías y reglas definidas, además de pasos y recetas que nos ayudan a poder construir un mejor producto digital. Mientras que en una **librería** no se tienen esas reglas y tenemos que valernos por nosotros mismos, ya que no existe un ejemplo de cómo se utilizaría algo en específico.

## ¿Cómo se conecta el Front-End con el Back-End?

Cuando realizamos una aplicación o sitio web, se debe unir el Back-End con el Front-End de alguna forma posible, en este caso, es a través de una API (_Aplication Program Interface_, en español es _Interfaz de Programación de Aplicaciones_).

### ¿Qué es una API?

Es simplemente una sección de nuestro backend que nos permite que el frontend pueda comunicarse con el primer mencionado, esto permite que haya un canal de información bidireccional, por lo que existen mensajes de entrada y de salida.

### Estándares para construir APIs

A lo largo de la historia del desarrollo web, se han desarrollado dos grandes estándares para construir APIS, los cuales son SOAP y REST.

#### SOAP (_Simple Object Acces Protocol_)

Mueve la información mediante un lenguaje llamado XML (_eXtensible Markup Language_), este es muy parecido a HTML, ya que son **lenguajes de mercado**. Sin embargo, este protocolo ya no se usa tanto hoy en día, ya que ahora se utiliza más que todo REST.

#### REST (_Representational State Transfer_)

Para poder crear una API basada en REST se debe confiar en otro lenguaje, llamado **JSON** (_JavaScript Object Notation_): es un lenguaje que nos facilita la comunicación entre un frontend y backend, es decir, a través de APIs. Y siempre trabajas con ellos en el backend.

### Datos curiosos sobre el lenguaje JSON en algunos lenguajes de programación.

- En `Python`, los **diccionarios** tienen la estructura de los JSON.
- Literalmente, JSON en `JavaScript` son los objetos, de ahí su nombre.
- En `Go` existe un _tag_ para darle una forma de JSON a los `struct`'s.

## El lenguaje del Internet: HTTP

HTTP es el acrónimo de _HyperText Transfer Protocol_, protocolo de transferencia de hipertexto, además de transferir texto, se tienen algunos agregados como _links_ o enlaces. Te explicaré con un ejemplo práctico, pero antes debes saber las definiciones de ciertas cosas.

- Cliente: son aquellos dispositivos que tienes a la disposición de tu mano, como un teléfono o computadora.
- Servidor: es un computador encendido 24/7 y contiene la aplicación o sitio web que podrás ver.

Cuando accedemos a un dominio, como este blog, lo que en realidad se hace es una **petición HTTP**, y como eres un cliente, puedes ver la información que tiene el servidor, esto es una **respuesta HTTP**. A las peticiones y respuestas HTTP se le dice en esta industria como _request y response_, respectivamente.

Puedes acceder más sobre HTTP en los docs de Mozilla pulsando [aquí](https://developer.mozilla.org/es/docs/Web/HTTP).

### Métodos de HTTP.

Existen varios métodos de HTTP, los cuales son:

1. GET:
2. POST:
3. PUT:
4. DELETE:

### Códigos de Estado
