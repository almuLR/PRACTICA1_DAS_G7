# Selección del patrón de diseño para calcular la ruta

* Status: accepted
* Deciders: Rubén, Pedro, Álvaro, Juan
* Date: 2023-11-09

## Context and Problem Statement

A la hora de seleccionar la ruta de camión se cuenta con 2 algoritmos de optimización que se seleccionan en función de la demora del camión.

## Decision Drivers

* RF05.1: Gestión con dos algoritmos

## Considered Options

* 0014-1-Patrón Strategy

## Decision Outcome

Chosen option: "0014-1-Patrón Strategy", because Encaja perfectamente con el problema que se presenta en nuestro sistema a la momento de elegir que ruta se adecua más en determinadas condiciones como puede ser el tiempo, distancia o coste.

### Positive Consequences

* Cada estrategia o algoritmo se encapsula en su propia clase, lo que facilita la gestión y mantenimiento del código. Cada estrategia es independiente, lo que mejora la cohesión y reduce la complejidad.
* Permite seleccionar dinámicamente un algoritmo específico en tiempo de ejecución
* Permite definir una familia de algoritmos, encapsular cada uno de ellos y hacer que sean intercambiables.
* Al encapsular algoritmos en clases separadas, se fomenta la reutilización de código.
* Como cada estrategia se encuentra en su propia clase, las pruebas unitarias son más fáciles de realizar.
* Cumple con el principio "Open/Closed" de SOLID, ya que puedes introducir nuevas estrategias sin modificar las clases existentes.
* Claridad del Código

## Pros and Cons of the Options

### 0014-1-Patrón Strategy

El patrón Strategy sugiere que tomes esa clase que hace algo específico de muchas formas diferentes y extraigas todos esos algoritmos para colocarlos en clases separadas llamadas estrategias. En nuestra arquitectura utilizaremos este patrón para seleccionar siempre el algoritmo más eficaz a la hora de elegir la mejor ruta posible para cada pedido.

* Good, because Cada estrategia o algoritmo se encapsula en su propia clase, lo que facilita la gestión y mantenimiento del código. Cada estrategia es independiente, lo que mejora la cohesión y reduce la complejidad.
* Good, because Permite seleccionar dinámicamente un algoritmo específico en tiempo de ejecución
* Good, because Permite definir una familia de algoritmos, encapsular cada uno de ellos y hacer que sean intercambiables.
* Good, because Al encapsular algoritmos en clases separadas, se fomenta la reutilización de código.
* Good, because Como cada estrategia se encuentra en su propia clase, las pruebas unitarias son más fáciles de realizar.
* Good, because Cumple con el principio "Open/Closed" de SOLID, ya que puedes introducir nuevas estrategias sin modificar las clases existentes.
* Good, because Claridad del Código

## Links

* https://refactoring.guru/es/design-patterns/strategy
