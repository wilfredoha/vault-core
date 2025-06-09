# Vault Core Fundamentals

Vault Core es una plataforma de core bancario moderna, nativa en la nube, diseñada por Thought Machine. Permite a los bancos construir productos financieros personalizados, operar de forma escalable y eliminar las limitaciones de los sistemas bancarios heredados.

## ¿Qué es Vault Core?

Vault Core actúa como el núcleo bancario central en la infraestructura tecnológica de un banco. Su arquitectura está basada en microservicios, contenedores (Docker) y orquestación con Kubernetes, permitiendo alta disponibilidad, resiliencia y despliegue activo-activo.

## Características principales

* **Smart Contracts**: Cada producto financiero es un contrato inteligente escrito en un subconjunto de Python, lo que otorga flexibilidad y control total al banco.
* **Universal Product Engine**: Motor de productos reutilizable para construir catálogos completos de productos sin duplicación de código.
* **Ledger en tiempo real**: Vault registra todas las publicaciones (movimientos financieros) en un libro mayor que refleja saldos al instante.
* **Integraciones abiertas**: APIs modernas (REST, gRPC, Kafka) para conectar Vault con procesadores de pagos, canales, CRMs, motores de fraude y más.
* **Plataforma cloud-agnostic**: Compatible con múltiples proveedores de nube (AWS, GCP, Azure).

## Arquitectura

Vault se divide en dos capas:

1. **Capa de plataforma**: Común a todos los clientes. Thought Machine actualiza y mantiene esta capa.
2. **Capa de configuración**: Específica del cliente, contiene sus Smart Contracts, workflows y definiciones personalizadas.

## Entidades clave

* **Productos**: Definidos mediante contratos inteligentes.
* **Cuentas**: Instancias de productos con saldos y lógica financiera.
* **Publicaciones**: Movimientos de fondos registrados en el ledger.
* **Clientes**: Representados con identificadores únicos y enlazados a sus cuentas.

## APIs principales

* **Core API**: Gestión de cuentas, productos, restricciones, simulaciones y dispositivos.
* **Postings API**: Movimiento de fondos (créditos, débitos, liquidaciones).
* **Streaming API**: Emisión de eventos en tiempo real (Kafka).
* **Data Loader API**: Migración e ingesta masiva de datos de sistemas legados.

## Ventajas frente a sistemas heredados

* Reducción de complejidad operativa.
* Eliminación de procesos por lotes.
* Flexibilidad total en la creación y evolución de productos.
* Visibilidad en tiempo real de la actividad financiera.
* Migraciones ágiles gracias a APIs automatizadas.

## Casos de uso

* Implementación de banca minorista o digital desde cero.
* Modernización de sistemas core legados.
* Lanzamiento de nuevos productos sin afectar el core existente.
* Integración con ecosistemas bancarios existentes mediante APIs y eventos.

## Recursos adicionales

* [Documentación oficial de Vault](https://www.thoughtmachine.net)
* [Curso de Smart Contracts en Vault (en línea)]
* [Materiales técnicos y esquemas de integración]

---

**© Thought Machine Group Limited – Uso confidencial.**
