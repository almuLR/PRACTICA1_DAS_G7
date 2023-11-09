# Clase GestorPedidos

* Status: accepted
* Deciders: Rubén, Pedro, Juan, Álvaro
* Date: 2023-11-09

## Context and Problem Statement

Hace de intermediario entre los clientes, pedidos, el reparto y las incidencias comunicando dichas funcionalidades

## Decision Drivers

* RF10: Componente GestorPedidos

## Considered Options

* 0012-1-Crear una clase GestorPedidos

## Decision Outcome

Chosen option: "0012-1-Crear una clase GestorPedidos", because Se indica como requisito obligatorio que debe exister este componente para hacer de intermediaro entre los clientes, pedidos , el reparto y las incidencias comunicando dichas funcionalidades.

### Positive Consequences

* La gran mayoría de la comunicación entre servicos y módules del sistema está gestionada por un único paquete

## Pros and Cons of the Options

### 0012-1-Crear una clase GestorPedidos

Se añadir una clase en el paquete LogicBusiness que usará: Paquete GestorRutas, Paquete RealizarPedido, Clase Incidencias, Clase Estadística y DatosCliente. Además de comunicarse con la API de Gestión de Microservicios. Este clase como indica su nombre es un Gestor, y será por tanto el "cerebro" del paquete LogicBusiness comunicando los diferentes servicios del sistema.

* Good, because La gran mayoría de la comunicación entre servicos y módules del sistema está gestionada por un único paquete
