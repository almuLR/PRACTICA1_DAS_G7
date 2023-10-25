# Propuesta del Gateway

* Status: proposed
* Deciders: Rubén,Pedro
* Date: 2023-10-25

## Context and Problem Statement

El acceso actual a las bases de datos se pretende que sea sustituido por protocolos HTTP/REST mediante un componente Gateway adecuado.

## Decision Drivers

* RF02:Acceso con protocolos HTTP/REST mediante un Gateway

## Considered Options

* 0002-1- Kong API Gateway  (Versión Gratuita)
* 0002-2-Azure API Gateway

## Decision Outcome

Chosen option: "", because comes out best.

## Pros and Cons of the Options

### 0002-1- Kong API Gateway 

Es un sistema intermediario que proporciona una interfaz API REST para hacer de enrutador desde un único punto de entrada, el API Gateway, hacia un grupo de microservicios y/o API de terceros definidos.

* Good, because Código abierto
* Good, because Optimizada para la arquitectura de microservicios
* Good, because Construida sobre un proxy liviano, por lo que puedes minimizar la latencia y escalar para múltiples aplicaciones de microservicios sin importar dónde se ejecuten.
* Good, because Administrar y limitar las solicitudes de API
* Good, because Proporciona una capa de autenticación para proteger tus servicios y un análisis para monitorear el tráfico a tus API y microservicios.
* Good, because Gratuito
* Good, because Gestión centralizada
* Good, because Personalizar las solicitudes y respuestas, facilitando así la adaptación de los datos y la lógica entre los microservicios
* Good, because Comunidad activa de usuarios y desarrolladores
* Bad, because Configuración compleja,
* Bad, because Costo adicional para funciones empresariales (e.j. control de tráfico avanzado, atención al cliente, gateway mocking)
* Bad, because Dependencia de la plataforma

### 0002-2-Azure API Gateway

Es un servicio de administración de API ofrecido por Microsoft Azure que se utiliza para crear, publicar, administrar y asegurar API en la nube. Esta plataforma permite a las organizaciones exponer sus servicios y datos a través de APIs de una manera segura y escalable

* Good, because Gestión centralizada
* Good, because Enrutamiento y balanceo de carga
* Good, because Proporciona capacidades de seguridad integradas, como autenticación, autorización y protección contra amenazas comunes
* Good, because Control de versiones: Puede gestionar múltiples versiones de sus API y realizar actualizaciones de manera controlada sin afectar a los clientes existentes
* Good, because Escalabilidad: Permite escalar los microservicios de acuerdo con las necesidades de tráfico
* Good, because Facilita la creación de documentación clara y accesible para los microservicios, lo que ayuda a los desarrolladores
* Bad, because Dependencia de la plataforma
* Bad, because Latencia potencial: El enrutamiento a través de la API Gateway puede introducir cierta latencia adicional en las solicitudes
* Bad, because Configuración y mantenimiento pueden ser complejos
* Bad, because Suscripcion de pago mensual y posibilidad de costos adicionales en entornos de gran escala

## Links

* https://blog.hubspot.es/website/que-es-api-gateway
* https://es.linkedin.com/pulse/qu%C3%A9-es-kong-gateway-ithreexglobal
* https://konghq.com/products/kong-gateway
