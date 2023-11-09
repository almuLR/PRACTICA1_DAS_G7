# Paquete GestorRutas

* Status: accepted
* Deciders: Rubén, Pedro, Álvaro, Juan
* Date: 2023-11-09

## Context and Problem Statement

Se debe poder gestionar las flotas de transporte a los clientes y las rutas de los camiones.

## Decision Drivers

* RF05: Gestión de flotas y rutas

## Considered Options

* 0009-1-Crear un paquete GestorRutas dentro de BusinessLogic

## Decision Outcome

Chosen option: "0009-1-Crear un paquete GestorRutas dentro de BusinessLogic", because Los paquetes deben dividirse según las funciones que cumplen dentro del sistema para facilitar así la división de responsabilidades, cohesión y modularización. Lo que permite minimizar el número de cambios a realizar en el resto del sistema cuando se modifica un paquete.

### Positive Consequences

* Modulariza una función del sistema monolítico que debemos migrar

## Pros and Cons of the Options

### 0009-1-Crear un paquete GestorRutas dentro de BusinessLogic

Este paquete  NO es un microservicio. Contendrá todas las clases necesarias  para la gestión de las flotas de transporte (flotas...) y las rutas de las camiones (algortimos...)

* Good, because Modulariza una función del sistema monolítico que debemos migrar a una arquitectura basada en microservicios
