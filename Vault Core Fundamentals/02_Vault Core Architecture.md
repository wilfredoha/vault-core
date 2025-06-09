# Vault Core - Arquitectura y Fundamentos

Vault Core es una plataforma bancaria central moderna, nativa en la nube, diseñada por Thought Machine. Su objetivo es reemplazar los sistemas core heredados con una arquitectura basada en microservicios, contenedores y eventos en tiempo real. 

## Introducción

Vault Core permite a los bancos construir, operar y escalar productos financieros con mayor flexibilidad, control y eficiencia, gracias al uso de contratos inteligentes escritos en un subconjunto seguro de Python.

## Plataformas core heredadas: Limitaciones

* Arquitecturas complejas con múltiples sistemas sincronizados por lotes.
* Alto riesgo de inconsistencias de datos.
* Lotes diarios limitan el acceso a datos en tiempo real.
* Personalización costosa y dependiente del proveedor.

## Visión general de Vault Core

* **Smart Contracts**: lógica financiera personalizada.
* **Ledger en tiempo real**: registra y refleja todas las transacciones.
* **Arquitectura distribuida**: contenedores + Kubernetes.
* **Capas diferenciadas**:
  * Plataforma (base común para todos los clientes).
  * Configuración (personalizada por cada banco).

## Banca en Vault Core

* Cada producto bancario es una instancia de un contrato inteligente.
* Las cuentas representan versiones ejecutables de productos.
* Vault maneja publicaciones (movimientos financieros) y saldos.
* Clientes representados con identificadores únicos (sin PII en Vault).

## APIs de Vault Core

* **API Principal**: gestión de cuentas, productos, roles, simulaciones, dispositivos.
* **API de Publicaciones**: procesamiento de débitos, créditos, liquidaciones.
* **API de Streaming**: eventos en tiempo real (cuentas, saldos, contratos).
* **API de Data Loader**: carga masiva para migraciones, vía Kafka.

## Operations Dashboard

* Interfaz gráfica para back-office.
* Permite ejecutar flujos de trabajo manuales y automatizados.
* Control de acceso por roles.
* Gestión de productos y definición de flujos de trabajo.

## Datos de configuración en Vault

* Administrados mediante:
  * Operations Dashboard.
  * API principal.
  * Utilidades CLI para CI/CD.
* Incluyen:
  * Smart Contracts.
  * Parámetros globales.
  * Definiciones YAML de flujos de trabajo.

---

**Vault Core redefine el core bancario moderno**, permitiendo la creación ágil de productos, integración con cualquier sistema externo y una operación basada en eventos en tiempo real. 

---

[Anterior](https://github.com/wilfredoha/vault-core/blob/main/Vault%20Core%20Fundamentals/01_Vault%20Core%20Introduction.md) [Siguiente]()

[Inicio](https://github.com/wilfredoha/vault-core/tree/main)
