# Módulo de estadísticas

* Status: accepted
* Deciders: Rubén, Pedro, Álvaro, Juan
* Date: 2023-11-09

## Context and Problem Statement

El sistema debe contar con un módulo de estadísticas que proporciona información sobre el estado(preparando,enviado,entregado) de los pedidos, la situación en tiempo real de los camiones y proporciona información de los clientes.

## Decision Drivers

* RF06: Módulo estadísticas

## Considered Options

* 0010-1-Crear clase Estadística

## Decision Outcome

Chosen option: "0010-1-Crear clase Estadística", because Al ser un módulo con una funcionalidad tan concreta se puede implementar en una única clase

### Positive Consequences

* Todo está contenido en una única clase lo que facilita su implementación
* Modulariza una función del sistema monolítico que debemos migrar

## Pros and Cons of the Options

### 0010-1-Crear clase Estadística

Se añadir una clase (Microservicio) en el paquete LogicBusiness que contendrá lo necesario para comunicarse con la base de datos y a partir de esos datos generar las estadísticas.

* Good, because Implementación sencilla
