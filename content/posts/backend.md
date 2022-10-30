+++
title = "Introducción al Backend"
date = "2022-10-28T20:02:10-04:00"
author = "Henrry Bourgeot"
authorTwitter = "estudiandev" #do not include @
description = "Seguramente, entraste a este post buscando orientarte sobre backend: qué lenguaje aprender, qué base de datos usar, pero no, aquí no verás tanto eso, más bien este post se concentra en las bases del backend, por lo que aquí, encontrarás lo que vas a aprender al desarrollar la parte del servidor de una web."
cover = ""
tags = ["backend", "desarrollo web", "cursos", "Platzi"]
color = "green" #color from the theme settings
draft = true
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

1. `GET`: este método solicita una representación de un recurso determinado, los navegadores nos muestran el frontend de una web a través de peticiones GET. Cabe destacar que **sólo** deben recuperar datos.
2. `HEAD`: pide una respuesta idéntica a la de una petición `GET`, con la excepción que no trae cuerpo de la respuesta, únicamente cabeceras.
3. `POST`: es muy utilizado actualmente para enviar una entidad a un recurso en específico, causando a menudo un cambio en el estado o incluso causando efectos secundarios en el servidor.
4. `PUT`: éste reemplaza todas las representaciones actuales del recurso de destino con la carga útil de la petición, por lo que podemos decir que **modifica o actualiza** los valores.
5. `DELETE`: borra un recurso en específico.
6. `CONNECT`: establece un túnel hacia el servidor identificado por el recurso.
7. `OPTIONS`: este método es normalmente utilizado para lograr describir las opciones de comunicación para el recurso de destino.
8. `TRACE`: realiza una prueba de bucle de retorno de mensaje a lo largo de la ruta al recurso de destino.
9. `PATCH`: éste es aplicado cuando se necesita realizar modificaciones parciales a un cierto recurso.

Puedes leer más sobre los métodos de HTTP en (nuevamente) los docs de [Mozilla](https://developer.mozilla.org/es/docs/Web/HTTP/Methods)

### Códigos de Estado

Los códigos de estado (en inglés _Status Code_) son muy importantes, ya que nos avisan el estado de nuestro sitio web, seguramente habrás visto el error **404**, **500** o algún otro, estos siempre tienen un significado, y se clasifican de la siguiente forma:

- 1XX: códigos de estado informativos.
- 2XX: códigos de estado exitosos.
- 3XX: códigos de estado redireccionales.
- 4XX: códigos de estado de error del cliente.
- 5XX: códigos de estado de error del servidor.

Aquí tienes un enlace a una imagen que te los detalla, proveniente de [Imgur](https://imgur.com/8Ql7ST7):

## Conceptos fundamentales.

Siempre estarás en un entorno donde se hablará mucho de _production_ (producción) y _deploy_ (desplegar), además de _localhost_, _dirección IP_ Y puertos, por lo que es muy importante conocer algunos conceptos fundamentales como _production_, _deploy_ y _localhost_.

### _Production_

Es aquel entorno donde tu sitio web (o aplicación) es visible para todo el mundo, es decir, que el entorno que te facilita el servidor, es lamado _production_, en español, entorno de producción.

### _Deploy_

Es el proceso de pasar tu aplicación web desde tu entorno local (tu computadora o laptop) a un servidor o _production environment_. Lo que se realiza para llevar a cabo este proceso, se debe hacer _push_ (enviar código) a un repositorio remoto como GitHub (sistema de control de versiones en la nube), este repositorio contiene el código fuente de tu proyecto.

### _Localhost_

Es la combinación de la dirección IP y un puerto de tu computadora.

### Servidor

Es una computadora que puede contener una aplicación o sitio web, y distribuye este mediante el protocolo HTTP a todo el internet.

### _The Cloud_ (La nube)

Es un conjunto de servidores que contienen aplicaciones y sitios web que logran hacer que el internet funcione.

### Hosting

Es un espacio en un servidor en el cual tu sitio web será guardado, aunque hay varios tipos de hosting, por ello, debes conocer lo siguiente:

#### IaaS

Es una

#### PaaS

#### SaaS
