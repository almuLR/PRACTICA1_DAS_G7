# Selección Del Patrón de Diseño en relación con la clase GestorPedidos

* Status: accepted
* Deciders: Rubén, Pedro, Álvaro, Juan
* Date: 2023-11-11

## Context and Problem Statement

La clase GestorPedidos hace de intermediario entre los clientes, pedidos, el reparto y las incidencias comunicando dichas funcionalidades. Por tanto es una clase que tiene muchas dependencias con distintos objetos independientes entre sí y por ello se propone usar un patrón para gestionar las interacciones entre estos componentes.

## Decision Drivers

* RF10: Componente Gestor Pedidos

## Considered Options

* 0015-1-Patrón Mediator
* 0015-1-Patrón Facade

## Decision Outcome

Chosen option: "0015-1-Patrón Mediator", because Hemos escogido el patrón Mediator para la clase Gestor Pedidos porque necesitamos
gestionar las interacciones entre objetos de la manera más eficiente.

Nos hemos decantado para el patrón Mediator por la capacidad que tiene para
minimizar las dependencias directas entre objetos. Con mediator, se establece un
punto de comunicación.

Otro punto que mejora con la elección de Mediator es el modularidad, esto es debido a
que lógica de coordinación se centraliza en este objeto.

En contraste, el patrón Facade, si bien es útil para simplificar interfaces hacia conjuntos
más grandes de clases , no se ajusta a nuestra necesidad de gestionar las interacciones
entre objetos independientes.

En conclusión, nos hemos quedado con el plan Mediator para la clase Gestor Pedidos
por su capacidad para gestionar las interacciones entre objetos de manera eficiente,
evitando así las dependencias directas.

### Positive Consequences

* Minimiza las dependencias directas entre objetos
* Mayor modularidad

## Pros and Cons of the Options

### 0015-1-Patrón Mediator

Mediator es un patrón de diseño de comportamiento que te permite reducir las dependencias caóticas entre objetos. El patrón restringe las comunicaciones directas entre los objetos, forzándolos a colaborar únicamente a través de un objeto mediador.

* Good, because Desacoplamiento: el patrón Mediator reduce las dependencias directas entre objetos. Cada objeto no necesita conocer detalles de implementación de otros objetos con los que se comunica.
* Good, because La lógica de coordinación y comunicación se centraliza en el objeto Mediator. Al reducir las dependencias directas, el patrón Mediator promueve la modularidad del sistema.
* Good, because Los objetos pueden ser reutilizados de manera más efectiva, ya que no están fuertemente acoplados entre sí.
* Good, because El Mediator proporciona un punto centralizado para la comunicación entre objetos.

### 0015-1-Patrón Facade

Facade es un patrón de diseño estructural que proporciona una interfaz simplificada a una biblioteca, un framework o cualquier otro grupo complejo de clases

* Good, because Facade reduce el acoplamiento entre los clientes y los subsistemas detrás de la fachada
* Good, because Los clientes no necesitan conocer los detalles internos de los subsistemas.
* Good, because Al proporcionar una interfaz única y clara, Facade promueve la modularidad del sistema
* Good, because Cada subsistema puede cambiar internamente sin afectar a los demás
* Good, because Facade simplifica la complejidad del sistema, haciendo que sea más fácil para los clientes utilizarlo.

## Links

* https://refactoring.guru/es/design-patterns/mediator
* https://refactoring.guru/es/design-patterns/facade
