# Módulo incidencias

* Status: accepted
* Deciders: Rubén, Pedro, Álvaro, Juan
* Date: 2023-11-09

## Context and Problem Statement

El sistema debe contar con un módulo de incidencias que sirva para reportar a los gestores de las rutas cualquier tipo de incidencia

## Decision Drivers

* RF07: Módulo de incidencias

## Considered Options

* 0011-1-Clase incidencias

## Decision Outcome

Chosen option: "", because Al ser un módulo con una funcionalidad tan concreta se puede implementar en una única clase

### Positive Consequences

* Todo está contenido en una única clase lo que facilita su implementación
* Modulariza una función del sistema monolítico que debemos migrar

## Pros and Cons of the Options

### 0011-1-Clase incidencias

Se añadir una clase en el paquete LogicBusiness que contendrá lo necesario para crear una Incidencia. Puede hacer uso de un enumerado que contenga los tipos de incidencias si es necesario.

* Good, because Implementación sencilla
