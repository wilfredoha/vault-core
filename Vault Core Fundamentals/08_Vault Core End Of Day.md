# Vault Core - Fin del Día (End of Day)

Este documento presenta una introducción al concepto de Fin del Día (EoD) en Vault Core, incluyendo su propósito, desafíos comunes y un ejemplo práctico de procesamiento diario.

## Introducción

Vault Core permite definir y ejecutar procesos de Fin del Día (EoD) como parte de las operaciones bancarias diarias. Esto permite consolidar saldos, aplicar intereses, generar reportes y avanzar la contabilidad a un nuevo día hábil.

EoD es crítico para bancos que deben mantener precisión contable en entornos que operan 24/7.

---

## ¿Qué es el EoD?

* Es un conjunto de eventos que se ejecutan diariamente después del cierre operativo.
* Sirve para consolidar información financiera y actualizar la posición de efectivo del banco.
* Puede incluir:
  * Devengo y aplicación de intereses.
  * Inicio o vencimiento de cuentas a plazo.
  * Generación de informes financieros y contables.
  * Cálculo de saldos finales y, si es necesario, saldos iniciales del siguiente día.
* Los eventos deben limitarse a los necesarios para mantener el saldo inicial consistente.

---

## Desafíos del EoD en entornos 24/7

1. Volumen de transacciones alto y constante.
2. Procesamiento sin ventana fija de cierre.
3. Conciliación con múltiples sistemas y zonas horarias.
4. Mantener coherencia en datos en movimiento.

### Enfoques comunes:

* **Cerrar el core por corto tiempo** para ejecutar EoD.
* **Amortiguar pagos** en un sistema auxiliar temporal.
* **Nunca cerrar el core** (complejo, pero ideal en disponibilidad continua).

---

## Ejemplo de EoD en Vault Core

Un banco define tres programas diarios:

* **Acumular intereses**: todos los días a las 23:00.
* **Aplicar intereses**: una vez al mes a las 23:30.
* **Informes de EoD**: tras completar los anteriores.

### Detalles:

* Cada actividad está definida como una programación dentro de un grupo de procesamiento.
* Si una falla, las siguientes no se ejecutan.
* La finalización exitosa genera una etiqueta Kafka que notifica a los sistemas posteriores.

---

## Grupos de Procesamiento

* Permiten agrupar cuentas y cronogramas.
* Pueden **pausar** procesos si hay fallos o publicaciones tardías.
* Permiten definir la **zona horaria operativa**.
* Mejora la resiliencia del EoD ante problemas ascendentes.

---

## Resumen

* EoD es clave para la contabilidad bancaria diaria.
* Vault Core lo permite mediante cronogramas, smart contracts y eventos.
* Grupos de procesamiento facilitan la ejecución ordenada y controlada.
* Una arquitectura pensada para 24/7 requiere precisión, flexibilidad y sincronización.

---

[Anterior](https://github.com/wilfredoha/vault-core/blob/main/Vault%20Core%20Fundamentals/07_Vault%20Core%20Smart%20Contracts.md)

[Inicio](https://github.com/wilfredoha/vault-core/tree/main)