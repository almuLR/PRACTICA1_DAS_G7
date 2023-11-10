# Proposición API gestión de microservicios

* Status: accepted
* Deciders: Rubén, Pedro, Álvaro, Juan
* Date: 2023-11-09

## Context and Problem Statement

Migrar la arquitectura de un sistema monolítico a una basada en microservicios por lo que necesitamos una API de gestión de microservicios

## Decision Drivers

* RF01: Migración de arquitectura

## Considered Options

* 0006-1-Spring Cloud
* 0006-2-Consul (Java Driver: Consult Java Driver)

## Decision Outcome

Chosen option: "0006-2-Consul", because Como API de gestión de microservicios hemos decido escoger Consul porque creemos que se adapta mejor a nuestras necesidades.

Una de las ventajas que Consul ofrece, es un enfoque en la gestión y descubrimiento de servicios, lo que facilita la construcción de arquitecturas microservicios.

Otra diferencia importante entre Consul y Spring Cloud radica en el hecho de que Consul proporciona una API dedicada, mientras que Spring Cloud se centra en proveer bibliotecas. Esto es esencial, ya que puede haber dependencias de versiones específicas de la biblioteca.

Otro punto a favor de Consul es su orientación a los principios RESTful en su API, esto hace más fácil la integración con diversas herramientas y lenguajes de programación,favoreciendo así la compatibilidad.

Por otro lado , si bien Spring Cloud se integra bien con micorservicios programados en Spring Boot, esto podría dar lugar a problemas en cuanto a flexibilidad. Depender solamente de Spring Boot como requisito para la integración limitaría el desarrollo.

En conclusión, creemos que Consul es la opción más adecuada para nuestra migración hacia una arquitectura microservicios ya que asegura tener una gestión efectiva y
escalable.

### Positive Consequences

* Facilita la integración
* Consul tiene orientación a los principios RESTful en su API
* Fexibilidad del lenguaje

### Negative Consequences

* Mayor complejidad

## Pros and Cons of the Options

### 0006-1-Spring Cloud

Spring Cloud es una herramienta de código abierto construida en Java que facilita el uso de marcos basados en Java para crear microservicios y aplicaciones web proporcionando bibliotecas.

* Good, because Permite a los microservicios encontrar y comunicarse entre sí de manera dinámica.
* Good, because Ofrece soluciones para la gestión de configuración distribuida en entornos de microservicios.
* Good, because Integra soluciones para el balanceo de carga dinámico, asegurando una distribución equitativa del tráfico entre los servicios.
* Good, because Implementa patrones de tolerancia a fallos
* Bad, because Puede haber una curva de aprendizaje significativa para comprender completamente todas las características y componentes de Spring Cloud.
* Bad, because La implementación completa de Spring Cloud puede introducir cierto overhead
* Bad, because Su integración se realiza de manera sencilla principalmente en  servicios construidos con Spring Boot

### 0006-2-Consul

Consul API no es un gateway en el sentido tradicional de un servidor de puerta de enlace (gateway) que actúa como intermediario entre los clientes y los servicios. Consul es una plataforma más amplia que proporciona funciones de descubrimiento de servicios, gestión de configuración, y herramientas para la construcción de infraestructuras distribuidas.

* Good, because Proporciona un sólido servicio de registro y descubrimiento de servicios, lo que facilita la construcción de arquitecturas de microservicios.
* Good, because La API de Consul sigue los principios RESTful, facilitando su integración con diversas herramientas y lenguajes de programación.
* Good, because Ofrece una solución para la gestión centralizada de la configuración, permitiendo la actualización dinámica de la configuración de la aplicación.
* Good, because Consul incluye una interfaz de usuario web que facilita la visualización y gestión de servicios y nodos.
* Good, because Consul está diseñado para ser resistente a fallos, lo que significa que puede funcionar de manera fiable en entornos distribuidos y heterogéneos.
* Bad, because Configurar Consul para casos de uso específicos puede requerir tiempo y esfuerzo debido a su rica gama de características.
* Bad, because Puede tener ciertos requerimientos de recursos en términos de CPU y memoria, especialmente en despliegues más grandes.
* Bad, because Para usuarios nuevos, puede haber una curva de aprendizaje asociada con la configuración y el uso eficiente de Consul.

## Links

* https://www.hashicorp.com/blog/announcing-hashicorp-consul-api-gateway
* https://spring.io/projects/spring-cloud
