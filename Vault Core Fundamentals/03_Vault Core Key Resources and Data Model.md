# Vault Core - Recursos Clave y Modelo de Datos

Vault Core es una plataforma bancaria de nueva generación que utiliza una arquitectura orientada a recursos. Esta arquitectura permite representar todas las entidades mediante operaciones CRUD, proporcionando trazabilidad, escalabilidad y control total sobre la información financiera.

## Introducción

Este documento presenta los fundamentos del modelo de datos y los recursos clave en Vault Core. Está diseñado para analistas de negocio, ingenieros, arquitectos y equipos de confiabilidad (SREs).

## Arquitectura orientada a recursos de Vault

* Todas las operaciones en Vault se realizan sobre recursos (objetos).
* Soporta operaciones CRUD: Crear, Leer, Actualizar y Borrar.
* Vault mantiene versiones inmutables; las actualizaciones generan nuevas versiones.
* La base de datos es **append-only**, garantizando integridad histórica.

## Recursos de cuenta clave

Vault Core administra múltiples recursos críticos:

* **Clientes**: identificadores únicos, sin almacenar PII directamente.
* **Cuentas**: cada cuenta está respaldada por un Smart Contract.
* **Dispositivos de pago**: tarjetas, IBANs, emails u otros identificadores.
* **Saldos**: definidos por activo, moneda, dirección y fase.
* **Publicaciones**: movimientos financieros atómicos, inmutables.
* **Cuentas internas**: utilizadas por el banco, sin lógica de contrato.

## Entidades de Smart Contract

* **Producto**: definición general del producto financiero.
* **Versión del producto**: representa una versión específica del contrato.
* **Cuenta**: instanciación del producto para un cliente específico.

Cada cuenta viva apunta a una versión de producto activa.

## Modelo de datos de cuentas

Una cuenta se relaciona con:

* Un cliente (o múltiples).
* Una versión de producto.
* Parámetros de instancia y metadatos.
* Dispositivos de pago y sus enlaces.
* Saldos en tiempo real.
* Publicaciones (débitos/créditos).
* Actualizaciones (cambios de versión o parámetros).

## Entidades de auditoría

* **Registros de auditoría**: detallan todas las solicitudes a la API.
* **Registros de acciones**: describen los cambios realizados en los recursos.
* Ambos son inmutables y publicados vía Kafka.
* Se recomienda almacenar estos registros externamente para auditoría a largo plazo.
* Se aplican políticas para limitar la visibilidad de usuarios a ciertos recursos.

---

**Vault Core ofrece una estructura robusta, modular y segura para la gestión de datos financieros complejos**, permitiendo flexibilidad, control y cumplimiento regulatorio.

---

[Anterior](https://github.com/wilfredoha/vault-core/blob/main/Vault%20Core%20Fundamentals/02_Vault%20Core%20Introduction.md) [Siguiente]()

[Inicio](https://github.com/wilfredoha/vault-core/tree/main)