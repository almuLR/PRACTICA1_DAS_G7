# Selección del Estilo

* Status: accepted
* Deciders: Rubén, Pedro, Álvaro, Juan
* Date: 2023-10-19

## Context and Problem Statement

Migrar la arquitectura de un sistema monolítico a una basada en microservicios

## Decision Drivers

* RF01: Migración de arquitectura

## Considered Options

* 0001-1-Arquitectura-Cliente-Servidor-Dos-Capas
* 0001-2-Arquitectura-Tres-Capas(Tiers)

## Decision Outcome

Chosen option: "0001-1-Arquitectura-Cliente-Servidor-Dos-Capas", because Este estilo es altamente eficaz en procesamiento de datos y transacciones. Las actualizaciones centralizadas son un gran punto a favor de este estilo ya que facilita el
control de versiones y errores, además de proporcionar un sistema optimizado. Todo esto hace que la empresa sea competitiva y capaz satisfacer las necesidades del cliente

Existen varios inconvenientes, mecionados en "negative consecuences", en el estilo que hemos de tener en cuenta como la dependencia del servidor y una menor flexibilidad. Sin embargo, son factores que estamos dispuestos a asumir como “mal menor” en comparación con las restricciones que ofrece el estilo “Tiers”.

El estilo por Tiers también presenta ciertos inconveninetes como: mayor
complejidad, latencia y gestión de versiones

La comunicación entre capas puede ofrecer cierta latencia lo que puede ser problemático en un entorno empresarial donde la velocidad es vital. Por ejemplo el caso en el que un cliente tenga que actualizar el inventario de su cesta en tiempo real
donde con un estilo “Tiers” el tiempo de comunicación entre capas podría ser visible al cliente, ralentizando así el proceso.

Además, la gestón de versiones puede volverse más tediosa debido al modularidad de la arquitectura.

Por tanto, hemos optido por  el estilo “Cliente – Servidor” porque consideramos más flexibles sus
inconvenientes respecto a los que ofrece el estilo “Tiers”.

### Positive Consequences

* Este estilo es altamente eficaz en procesamiento de datos y transacciones. Las actualizaciones centralizadas son un gran punto a favor de este estilo ya que facilita el control de versiones y errores, además de proporcionar un sistema optimizado. Todo esto hace que la empresa sea competitiva y capaz satisfacer las necesidades del cliente.

### Negative Consequences

* Por un lado, la dependencia del servidor en una arquitectura Cliente-Servidor de Dos Capas puede gestionarse mediante una buena planificación. Un posible ejemplo de
esto sería establecer un sistema de servidores gemelos donde si uno de ellos tuviera algún fallo el tráfico de datos se redirigiría al otro
* El segundo inconveniente era la poca flexibilidad ya que todas las operaciones del cliente están fuertemente relacionadas con el servidor. Sin embargo, esto también
implica que las modificaciones sean gestionadas de manera centralizada. Un caso donde se ejemplifique esto sería la actualización del servidor. Tras ser actualizado, todos los usuarios podrían acceder a la nueva funcionalidad sin la necesidad de ir
actualizando cliente a cliente la misma.

## Pros and Cons of the Options

### 0001-1-Arquitectura-Cliente-Servidor-Dos-Capas

Arquitectura-Cliente-Servidor-Dos-Capas (Client, Server)

* Good, because Rendimiento: La arquitectura cliente-servidor tiende a ser eficiente en términos de rendimiento, ya que las operaciones se ejecutan en un servidor centralizado que generalmente tiene más recursos de hardware y potencia de procesamiento que los clientes
* Good, because Facilidad de implementación: Puede ser más fácil de implementar y comprender, especialmente para aplicaciones más simples, ya que la lógica de negocio se concentra en el servidor.
* Good, because Actualizaciones centralizadas: Las actualizaciones de software y parches se pueden realizar en el servidor central, lo que facilita la gestión de versiones y correcciones.
* Bad, because Escalabilidad limitada: La escalabilidad puede ser un desafío, ya que el rendimiento y la capacidad del sistema dependen en gran medida del servidor central, lo que puede convertirse en un cuello de botella.
* Bad, because Dependencia del servidor: Los clientes dependen en gran medida del servidor para realizar cualquier tarea, lo que puede causar problemas si el servidor falla o experimenta problemas de red.
* Bad, because Menor flexibilidad: Puede ser menos flexible en comparación con las arquitecturas por capas, ya que las operaciones específicas del cliente suelen estar fuertemente acopladas con el servidor.

### 0001-2-Arquitectura-Tres-Capas(Tiers)

Arquitectura con tres capas principales en horizontal (Client, Business Logic, BaseData)

* Good, because Modularidad y flexibilidad: La arquitectura por capas permite una mayor modularidad y flexibilidad en el diseño, lo que facilita la expansión, el mantenimiento y la evolución del sistema.
* Good, because Mejor escalabilidad: Puede ser más escalable, ya que diferentes capas pueden escalar por separado para satisfacer las necesidades de rendimiento.
* Good, because Reutilización de componentes: Las capas separadas permiten la reutilización de componentes en diferentes partes del sistema
* Bad, because Mayor complejidad: La arquitectura por capas puede ser más compleja de diseñar, implementar y mantener, especialmente en sistemas muy grandes
* Bad, because Mayor latencia: La comunicación entre capas a través de la red o la interfaz puede introducir cierta latencia, especialmente en sistemas distribuidos
* Bad, because Gestión de versiones: La gestión de versiones y actualizaciones puede ser más compleja debido a la modularidad y la posibilidad de múltiples componentes interdependientes.
