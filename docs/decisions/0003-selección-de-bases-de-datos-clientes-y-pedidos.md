# Selección de Bases de Datos Clientes y Pedidos

* Status: accepted
* Deciders: Rubén, Pedro, Juan, Álvaro
* Date: 2023-10-31

## Context and Problem Statement

La arquitectura existente cuenta con una parte de clientes PC y móvil que acceden a los datos de la empresa alojados en 2 BBDD SQL (Clientes, Pedidos). La BBDD de Clientes contiene datos de clientes y pagos mientras que
la BBDD de Pedidos se encarga de almacenar los datos restantes.

## Decision Drivers

* RF09: Sistema con dos bases de datos
* RF09.1: BBDD SQL de clientes y pagos
* RF09.2: BBDD SQL de pedidos

## Considered Options

* 0003-1-MySQL (Java Driver: MySQL Connector/J)
* 0003-2-Oracle Database (Java Driver: Oracle JDBC Driver

## Decision Outcome

Chosen option: "0003-1-MySQL", because Para una arquitectura de microservicios como la nuestra hemos decido que las dos bases de datos sean MySQL.

MySQL tiene una distribución libre y gratuita lo que significa un ahorro importante para la compañía

Otra de las ventajas que te ofrece MySQL es su versatilidad multiplataforma compatible con sistemas operativos como Linux o Windows, esto aporta gran flexibilidad a la arquitectura

Además, tiene una fácil configuración lo que es importante en un entorno con microservicios, donde la agilidad y la rapidez en el despliegue de servicios son muy importantes para preservar una gran eficiencia.

En conclusión, pensamos que la elección de MySQL es la mejor por su condición de código abierto, distribución gratuita y una instalación sencilla.

### Positive Consequences

* Código abierto
* Distribución gratuita
* Instalación sencilla
* Versatilidad multiplataforma

## Pros and Cons of the Options

### 0003-1-MySQL

Base de datos recomendada para aplicaciones web, aplicaciones empresariales de tamaño mediano, y proyectos que requieran una base de datos relacional sólida y de código abierto.

* Good, because Distribución libre y gratuita, podemos descargarlo del sitio web oficial de MySQL sin ningún costo.
* Good, because Open Source
* Good, because Multiplataforma (Linux, Windows...)
* Good, because Instalación y configuración sencilla
* Bad, because Una mala configuración recudece mucho la seguridad
* Bad, because Varias de las utilidades de MySQL no están documentadas
* Bad, because No es la opción más eficiente con bases de datos de tamaño elevado

### 0003-2-Oracle Database (Java Driver: Oracle JDBC Driver

Base de datos recomendada para grandes empresas, aplicaciones empresariales a gran escala y proyectos que requieren una base de datos de alto rendimiento con características avanzadas.

* Good, because Más usada a nivel mundial
* Good, because Multiplataforma absoluta (incluye superordenadores)
* Good, because Soporta todas las funciones que se esperan de un servidor "serio": un lenguaje de diseño de bases de datos muy completo (PL/SQL) que permite implementar diseños "activos", con triggers y procedimientos almacenados, con una integridad referencial declarativa bastante potente.
* Good, because Permite uso de particiones para mejorar la eficiencia, de replicación y administración de bases de datos distribuidas
* Bad, because Elevado precio
* Bad, because Dificultad de configuración elevada
* Bad, because Documentación difcil de conseguir, incluso para asuntos sencillos  como la simple instalación

## Links

* https://codigosql.top/ventajas-y-desventajas-de-mysql/?expand_article=1
* https://oraclebddepn.blogspot.com/2013/05/ventajas-y-desventajas.html
* https://fp.uoc.fje.edu/blog/por-que-elegir-el-gestor-de-base-de-datos-mysql/
