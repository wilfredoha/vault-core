# Vault Core

Vault Core es la solución de core bancario de nueva generación desarrollada por Thought Machine. Es una plataforma nativa de la nube que permite a los bancos diseñar, implementar y operar productos financieros personalizados utilizando Smart Contracts y microservicios escalables.

* Arquitectura basada en contenedores y Kubernetes.
* Disponible en múltiples nubes (cloud agnostic).
* Diseñada para reemplazar sistemas bancarios heredados.

## Plataformas bancarias heredadas

Los sistemas core tradicionales presentan múltiples desafíos técnicos y operativos:

* Gran cantidad de datos duplicados en distintos sistemas.
* Procesos por lotes diarios o semanales que impiden el análisis en tiempo real.
* Requieren conciliaciones constantes entre sistemas.
* Difíciles de escalar o personalizar sin intervención del proveedor.
* Las migraciones son costosas y propensas a errores.

## Vault Core Product Engine

El motor de productos (Product Engine) permite a los bancos definir productos financieros mediante contratos inteligentes:

* **Smart Contracts** escritos en un subconjunto seguro de Python.
* Cada producto es un contrato independiente, reusable y configurable.
* Soporte para gestión de jerarquías de productos y catálogos personalizados.
* Permite una rápida evolución del portafolio sin impacto en el core.

## Vault Core Ledger

El libro mayor de Vault registra cada movimiento financiero de forma inmutable y en tiempo real.

* Registra las publicaciones (movimientos entre cuentas).
* Soporta múltiples monedas y tipos de activos.
* Fuente única de verdad contable.
* Proporciona datos consistentes para auditorías, contabilidad y reportes.

## Desarrollo de productos bancarios en Vault

Vault Core permite construir productos desde cero o replicar productos existentes con facilidad.

* Cada cuenta es una instancia de un Smart Contract.
* Configuración independiente de cronogramas y parámetros por producto.
* Admite reglas personalizadas: intereses, comisiones, límites, etc.
* Integra simulación, pruebas y versionado en la gestión de productos.

## Vault Core Integrations

Vault permite integrarse con sistemas internos y externos de forma uniforme:

* API de publicaciones para cualquier integración (tarjetas, pagos, etc.).
* Soporte para eventos en tiempo real usando Kafka.
* Permite conectar CRMs, procesadores de pagos, esquemas de tarjetas, etc.
* Soporte para orquestación mediante flujos de trabajo opcionales.

## Data Reporting and Analysis

Vault no analiza los datos directamente, pero los expone en tiempo real para ser consumidos externamente.

* Transmisión en tiempo real de eventos: publicaciones, saldos, estados.
* Compatible con lagos de datos, almacenes contables y dashboards.
* Permite realizar conciliaciones automáticas y reportes regulatorios.
* Los eventos pueden ser suscritos por sistemas de BI o contabilidad.

---

[Anterior](https://github.com/wilfredoha/vault-core/tree/main) [Siguiente]()