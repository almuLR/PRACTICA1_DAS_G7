# Cambio del estilo de la arquitectura

* Status: accepted
* Deciders: Rubén, Pedro, Juan, Álvaro
* Date: 2023-10-31

## Context and Problem Statement

Migrar la arquitectura de un sistema monolítico a una basada en microservicios

## Decision Drivers

* RF01: Migración de arquitectura

## Considered Options

* 0001-1-Arquitectura-Cliente-Servidor-Dos-Capas (Cliente-Servidor)
* 0001-1-Arquitectura-Cliente-Servidor-Tres-Capas (Cliente-Business Logic/Servidor-Datos)

## Decision Outcome

Chosen option: "0001-1-Arquitectura-Cliente-Servidor-Tres-Capas", because La capa servidor se separa en dos capas llamadas, Business Logic y Datos respectivamente, ya que las bases de datos que conforman esta capa no forman parte del servidor, como era usual hace décadas,  sino que son bases de datos externas por lo que deben estar en capas separadas.

### Positive Consequences

* Mayor escalabilidad, modularidad y reutlización de componentes

### Negative Consequences

* Al no tener la base de datos propia puede producirse mayor latencia en las peticiones relacionadas con las bases de datos

## Pros and Cons of the Options

### 0001-1-Arquitectura-Cliente-Servidor-Dos-Capas

* Good, because Rendimiento: La arquitectura cliente-servidor tiende a ser eficiente en términos de rendimiento, ya que las operaciones se ejecutan en un servidor centralizado que generalmente tiene más recursos de hardware y potencia de procesamiento que los clientes
* Good, because Facilidad de implementación: Puede ser más fácil de implementar y comprender, especialmente para aplicaciones más simples, ya que la lógica de negocio se concentra en el servidor.
* Good, because Actualizaciones centralizadas: Las actualizaciones de software y parches se pueden realizar en el servidor central, lo que facilita la gestión de versiones y correcciones.
* Bad, because Escalabilidad limitada: La escalabilidad puede ser un desafío, ya que el rendimiento y la capacidad del sistema dependen en gran medida del servidor central, lo que puede convertirse en un cuello de botella.
* Bad, because Dependencia del servidor: Los clientes dependen en gran medida del servidor para realizar cualquier tarea, lo que puede causar problemas si el servidor falla o experimenta problemas de red
* Bad, because Menor flexibilidad: Puede ser menos flexible en comparación con las arquitecturas por capas, ya que las operaciones específicas del cliente suelen estar fuertemente acopladas con el servidor.

### 0001-1-Arquitectura-Cliente-Servidor-Tres-Capas

* Good, because Modularidad y flexibilidad: La arquitectura por capas permite una mayor modularidad y flexibilidad en el diseño, lo que facilita la expansión, el mantenimiento y la evolución del sistema.
* Good, because Mejor escalabilidad: Puede ser más escalable, ya que diferentes capas pueden escalar por separado para satisfacer las necesidades de rendimiento.
* Good, because Reutilización de componentes: Las capas separadas permiten la reutilización de componentes en diferentes partes del sistema
* Bad, because Mayor complejidad: La arquitectura por capas puede ser más compleja de diseñar, implementar y mantener, especialmente en sistemas muy grandes
* Bad, because Mayor latencia: La comunicación entre capas a través de la red o la interfaz puede introducir cierta latencia, especialmente en sistemas distribuidos
* Bad, because Gestión de versiones: La gestión de versiones y actualizaciones puede ser más compleja debido a la modularidad y la posibilidad de múltiples componentes interdependientes.
