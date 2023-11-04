# Selección De La Pasarela De Pago

* Status: accepted
* Deciders: Rubén, Pedro, Juan, Álvaro
* Date: 2023-10-31

## Context and Problem Statement

El sistema debe permitir conectarse a una pasarela de pago externa que proporciona otra empresa para realizar los pagos.

## Decision Drivers

* RF08: Conexión con pasarela

## Considered Options

* 0004-1: Strike (Java: SDK Stripe)
* 0004-2: Paypal (Java: SDK PayPal)

## Decision Outcome

Chosen option: "0004-1: Strike", because Al seleccionar la pasarela de pago para nuestra arquitectura es importante considerar las necesidades específicas de nuestro negocio. Tras una evaluación, hemos decidido que Stripe es la opción más adecuada.

En cuanto a Tarifas y Costos Stripe ofrece tan solo 2,9% + 30 cent por transacción, lo que representa un ahorro significativo respecto al 3,4% + 30 cent que cobra paypal. Además, Stripe no impone costos por mantenimiento.

En cuanto a Seguridad, ambos ofrecen una seguridad robusta. Sin embargo, Stripe se distingue por un enfoque exhaustivo en la encriptación de datos y el acceso restringido.

La eficiencia en el proceso de pago es algo de vital importancia y Stripe procesa los pagos de manera muy eficiente, en segundos. Esto garantiza una experiencia de compra rápida y sin interrupciones para el cliente.

Por último, es importante destacar la cantidad de métodos de pago que Stripe ofrece como por ejemplo tarjetas de débito y crédito, opciones de pago digital como ApplePay o GooglePay. Esto hace que el cliente tenga una gran flexibilidad.

En conclusión, Stripe ofrece una combinación de eficiencia, seguridad y flexibilidad que hace que sea una opción muy solidad para una compañía como la nuestra.

### Positive Consequences

* Ofrece mejores tarifas y costos por transacción respecto a Paypal
* Un enfoque exhaustivo en la encriptación de datos y el acceso
restringido.
* Procesa los
pagos de manera muy eficiente, en segundos
* Ofrece una a cantidad de métodos de pago

## Pros and Cons of the Options

### 0004-1: Strike

Stripe es una opción sólida para la gestión de pagos en aplicaciones. Ofrece una API muy flexible y fácil de usar, lo que hace que sea sencillo integrarla con la lógica de tu aplicación. Además, Stripe proporciona herramientas de informes y análisis que pueden ayudarte a realizar un seguimiento de las transacciones y generar estadísticas.

* Good, because Darse de alta es gratuito
* Good, because Comisiones bajas por cada venta (en comparación con la competencia)
* Good, because Pago integrado en la propia web (no hay redirección)
* Good, because Acepta cualquier tipo de tarjeta bancaria (además de aplicaciones móviles)
* Good, because Seguridad alta
* Good, because Plataforma de pago global
* Good, because Proporciona herramientas de informes y análisis
* Bad, because Cuenta bancaria requerida
* Bad, because Sorporte limitado (documentación y recursos en línea) para cuentas gratuitas
* Bad, because Necesidad de conocimientos técnicos en desarrollo web para integrar Stripe

### 0004-2: Paypal

PayPal es una opción popular para la integración de pagos en aplicaciones. Ofrece una API robusta y ampliamente utilizada que puede integrarse con facilidad. Además, PayPal proporciona herramientas para el seguimiento de transacciones y la generación de informes

* Good, because Solo es necesario asociar una tarjeta o una cuenta bancaria a una cuenta de e-mail con la que realizarás tus pagos en Internet
* Good, because Amplia variedad de métodos de pago
* Good, because Gratuito para el comprador, pequeña comisión para el vendedor
* Good, because Ofrece informes detallados y herramientas de análisis que pueden ayudarte a realizar un seguimiento de tus transacciones y generar informes útiles para la toma de decisiones
* Good, because El mismo día que realices el pago el dinero estará disponible en la cuenta del vendedor
* Bad, because Resolución de disputas pueden favorecer al comprador, obligando a demostrar que el vendedor a cumplido sus obligaciones
* Bad, because Cuentas limitidas o suspendidas sin previo aviso si detecta actividad sospechosa
* Bad, because La atención al cliente puede ser inconsestente y llevar tiempo
* Bad, because Las cuentas de Paypal pueden ser vulnerables a ataques si no se toman precauciones adecuadas

## Links

* https://blog.arcadina.com/ventajas-de-usar-paypal-para-tus-pagos-en-internet/
* https://www.easyappcode.com/que-es-stripe-como-funciona-ventajas-e-inconvenientes
* https://www.gluo.mx/blog/stripe-vs-paypal-cual-es-la-mejor-pasarela-de-pago
