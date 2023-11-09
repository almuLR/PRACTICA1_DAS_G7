# Acceso a Datos de los Clientes

* Status: accepted
* Deciders: Rubén, Pedro, Juan, Álvaro
* Date: 2023-11-09

## Context and Problem Statement

Los empleados de la empresa tienen que poder acceder a los datos personales (nombre, apellido, teléfono) de los clientes

## Decision Drivers

* RF03: Acceso datos clientes

## Considered Options

* 0007-1-Crear una clase llamada DatosClientes

## Decision Outcome

Chosen option: "0007-1-Crear una clase llamada DatosClientes", because Porque la lógica de negocio debe contar con un módulo Clientes que permite acceder a los datos personales de los clientes

### Positive Consequences

* Modulariza una función del sistema monolítico que debemos migrar a una arquitectura basada en microservicios

## Pros and Cons of the Options

### 0007-1-Crear una clase llamada DatosClientes

Se añadir una clase en el paquete LogicBusiness que contendrá como atributos los datos de los clientes y los métodos necesarios para comunicarse con la base de datos

* Good, because Modulariza una función del sistema monolítico que debemos migrar a una arquitectura basada en microservicios
