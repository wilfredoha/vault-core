# Introducción a Vault Core

Vault Core es una plataforma bancaria central nativa en la nube, desarrollada por Thought Machine, diseñada para resolver los desafíos de las arquitecturas heredadas mediante una arquitectura de microservicios, contenedores y escalabilidad activa-activa.

## Plataformas bancarias heredadas

* Requieren sincronización compleja de datos.
* Utilizan procesos por lotes que dificultan la disponibilidad en tiempo real.
* Presentan riesgos en migraciones y personalización limitada de productos.
* Dificultan la integración ágil con nuevos servicios y canales.

## Vault Core Product Engine

* Motor central que permite diseñar y operar productos financieros.
* Usa Smart Contracts escritos en Python, que definen la lógica del producto.
* Permite reutilizar contratos entre múltiples productos y escenarios.

## Vault Core Ledger

* Registra todos los movimientos financieros (publicaciones) en tiempo real.
* Permite cálculos y análisis inmediatos, ideal para auditoría y reportes.
* Compatible con múltiples tipos de activos y monedas.

## Desarrollo de productos bancarios en Vault Core

* Cada producto es una instancia de un Smart Contract.
* Admite cronogramas personalizados por producto.
* Se eliminan los cronogramas fijos y se habilita la innovación rápida.

## Integraciones en Vault Core

* Integración uniforme con procesadores de pagos mediante una única API.
* Soporte para eventos en tiempo real vía Kafka.
* Arquitectura preparada para migraciones por API en tiempo real.

## Reportes y análisis de datos

* Vault transmite datos financieros, contables y de eventos en tiempo real.
* Los clientes capturan y transforman los datos en sus propios data lakes o almacenes GL.
* Permite generar informes contables, regulatorios y de negocio actualizados al instante.
