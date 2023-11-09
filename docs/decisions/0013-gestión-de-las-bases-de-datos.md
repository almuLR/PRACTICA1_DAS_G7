# Gestión de las bases de datos

* Status: accepted
* Deciders: Rubén, Pedro, Álvaro, Juan
* Date: 2023-11-09

## Context and Problem Statement

El sistema cuenta con dos bases de datos, además de varios módulos que hacen uso de las mismas.

## Decision Drivers

* RF03: Acceso datos clientes
* RF06: Módulo de estadísticas
* RF09: Sistema con dos bases de  datos

## Considered Options

* 0013-1-Crear una clase GestorBasesDatos

## Decision Outcome

Chosen option: "0013-1-Crear una clase GestorBasesDatos", because Desacopla de las clases Estadística y DatosCliente la necesidad de gestionar las bases de datos.  Las clases de Estadística y DatosCliente se comunicaran ahora con esta clase en vez de trata directamente con la base de datos.

### Positive Consequences

* Desacopla de las clases Estadística y DatosCliente la necesidad de gestionar las bases de datos
* Se contiene toda la lógica de la comunicación con las bases de datos lo que permite la separación de funcionalidades
* Modularización

## Pros and Cons of the Options

### 0013-1-Crear una clase GestorBasesDatos

Clase que se encarga de comunicarse con las APIs de las bases de datos siempre que se requiera añadir/consultar/cambiar cualquier información por parte de una clase. Debe contener los métodos necesarios para realizar estas funciones. Las clases de Estadística y DatosCliente se comunicaran ahora con esta clase en vez de trata directamente con la base de datos

* Good, because Se contiene toda la lógica de la comunicación con las bases de datos lo que permite la separación de funcionalidades
* Good, because Desacopla de las clases Estadística y DatosCliente la necesidad de gestionar las bases de datos
