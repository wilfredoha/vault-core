# Vault Core - Principios Financieros y Tipos de Publicaciones

Vault Core define un modelo contable robusto basado en principios financieros clave como la contabilidad por partida doble, la flexibilidad en los tipos de publicaciones, y una arquitectura de saldos adaptable. Esta guía ofrece una visión general de estos fundamentos.

## ¿Qué es un Registro Financiero en Vault Core?

Un registro financiero en Vault está compuesto por tres elementos:

* **Publicaciones**: representan un débito o crédito. Son inmutables y se almacenan en el libro mayor.
* **Saldos**: el resultado neto de todas las publicaciones asociadas a una cuenta.
* **Cuentas**: agrupaciones de saldos divididas en direcciones, definidas por contratos inteligentes.

## Tipos de Publicaciones

Vault define múltiples tipos de publicaciones para modelar procesos financieros:

* **Autorización**: reserva fondos sin comprometerlos aún.
* **Ajuste de autorización**: incrementa el monto previamente autorizado.
* **Liquidación**: compromete los fondos reservados.
* **Liberación**: revierte una autorización parcial o total.
* **Transferencia**: mueve fondos entre cuentas.
* **Acuerdo duro**: liquidación directa sin autorización previa.
* **Instrucción personalizada**: movimiento flexible entre cuentas/fases/direcciones.

## Saldos en Vault Core

* Cada saldo se define por: **activo**, **denominación**, **dirección** y **fase**.
* Las fases son: **pendiente entrante**, **comprometido** y **pendiente saliente**.
* Soporta múltiples monedas y activos (por ejemplo: puntos de fidelidad).
* El saldo neto depende del tipo de cuenta (activo/pasivo).

## Contabilidad de Doble Entrada

* Toda publicación en Vault sigue el principio contable de doble entrada.
* Cada débito debe estar equilibrado con uno o más créditos del mismo valor.
* Garantiza integridad contable tanto en cuentas de cliente como en cuentas internas.

## Valoración Temporal y Retroactividad (Value Dating / Backdating)

* Las publicaciones pueden tener tres marcas de tiempo:
  * **insertion_timestamp**: cuándo fue registrada en el libro mayor (establecido por Vault).
  * **value_timestamp**: cuándo debe afectar el saldo (puede ser retroactivo).
  * **booking_timestamp**: cuándo se "reserva" (puede coincidir con value o insertion).
* Vault recalcula saldos históricos si se aplica una publicación retroactiva.
* Se recomienda usar la API de simulación para verificar efectos antes de aplicar correcciones.

---

**Vault Core proporciona una infraestructura contable moderna**, flexible y compatible con las necesidades complejas de productos financieros innovadores.

---

[Anterior](https://github.com/wilfredoha/vault-core/blob/main/Vault%20Core%20Fundamentals/03_Vault%20Core%20Key%20Resources%20and%20Data%20Model.md) [Siguiente](https://github.com/wilfredoha/vault-core/blob/main/Vault%20Core%20Fundamentals/05_Vault%20Core%20Product%20and%20Integration%20Libraries.md)

[Inicio](https://github.com/wilfredoha/vault-core/tree/main)