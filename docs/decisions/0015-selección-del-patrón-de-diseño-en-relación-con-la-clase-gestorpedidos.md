# Selección Del Patrón de Diseño en relación con la clase GestorPedidos

* Status: proposed
* Deciders: Rubén, Pedro
* Date: 2023-11-11

## Context and Problem Statement

La clase GestorPedidos hace de intermediario entre los clientes, pedidos, el reparto y las incidencias comunicando dichas funcionalidades. Por tanto es una clase que tiene muchas dependencias con distintos objetos independientes entre sí y por ello se propone usar un patrón para gestionar las interacciones entre estos componentes.

## Decision Drivers

* RF10: Componente Gestor Pedidos

## Considered Options

* 0015-1-Patrón Mediator
* 0015-1-Patrón Facade

## Decision Outcome

Chosen option: "", because comes out best.

## Pros and Cons of the Options

### 0015-1-Patrón Mediator

Mediator es un patrón de diseño de comportamiento que te permite reducir las dependencias caóticas entre objetos. El patrón restringe las comunicaciones directas entre los objetos, forzándolos a colaborar únicamente a través de un objeto mediador.

* Good, because Desacoplamiento: el patrón Mediator reduce las dependencias directas entre objetos. Cada objeto no necesita conocer detalles de implementación de otros objetos con los que se comunica.
* Good, because La lógica de coordinación y comunicación se centraliza en el objeto Mediator.
Al reducir las dependencias directas, el patrón Mediator promueve la modularidad del sistema.
* Good, because Los objetos pueden ser reutilizados de manera más efectiva, ya que no están fuertemente acoplados entre sí.
* Good, because El Mediator proporciona un punto centralizado para la comunicación entre objetos.

### 0015-1-Patrón Facade

Facade es un patrón de diseño estructural que proporciona una interfaz simplificada a una biblioteca, un framework o cualquier otro grupo complejo de clases

* Good, because Facade reduce el acoplamiento entre los clientes y los subsistemas detrás de la fachada
* Good, because Los clientes no necesitan conocer los detalles internos de los subsistemas.
* Good, because Al proporcionar una interfaz única y clara, Facade promueve la modularidad del sistema
* Good, because Cada subsistema puede cambiar internamente sin afectar a los demás
* Good, because Facade simplifica la complejidad del sistema, haciendo que sea más fácil para los clientes utilizarlo.
