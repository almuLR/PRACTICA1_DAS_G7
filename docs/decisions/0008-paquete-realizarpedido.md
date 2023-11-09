# Paquete RealizarPedido

* Status: accepted
* Deciders: Rubén, Pedro, Álvaro, Juan
* Date: 2023-11-09

## Context and Problem Statement

Los clientes tienen que poder realizar pedidos de los productos a la empresa. 
Si un cliente intenta realizar un pedido se le permite un número de intentos por determinar.

## Decision Drivers

* RF04: Hacer pedidos a a empresa
* RF04.1: Número máximo de intentos

## Considered Options

* 0008-1-Crear un paquete RealizarPedido dentro de BusinessLogic

## Decision Outcome

Chosen option: "0008-1-Crear un paquete RealizarPedido dentro de BusinessLogic", because Los paquetes deben dividirse según las funciones que cumplen dentro del sistema para facilitar así la división de responsabilidades, cohesión y modularización. Lo que permite minimizar el número de cambios a realizar en el resto del sistema cuando se modifica un paquete.

### Positive Consequences

* Modulariza una función del sistema monolítico que debemos migrar a una arquitectura basada en microservicios

## Pros and Cons of the Options

### 0008-1-Crear un paquete RealizarPedido dentro de BusinessLogic

Este paquete será un microservicio que contendrá todas las clases necesarias para realizar el pedido salvo la pasarela de pago que al ser un serivcio crítico se mantendrá fuera de este paquete.

* Good, because Modulariza una función del sistema monolítico que debemos migrar a una arquitectura basada en microservicios
