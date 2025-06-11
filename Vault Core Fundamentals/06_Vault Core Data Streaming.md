# Vault Core - Transmisión de Datos (Data Streaming)

Este documento presenta las capacidades de transmisión de datos en Vault Core, una de las características clave de su arquitectura moderna basada en eventos.

## Introducción

Vault Core permite exponer información del sistema casi en tiempo real a través de eventos transmitidos por Kafka. Esto habilita múltiples casos de uso como conciliación, monitoreo de riesgo, analítica, personalización y más.

---

## Descripción general de las API de Streaming

* Vault cuenta con **API RESTful** (interacción sincrónica) y **API de Streaming** (interacción asincrónica).
* La API de Streaming está basada en **Apache Kafka**.
* Cada tipo de evento (cuentas, publicaciones, saldos, contratos, clientes) se transmite desde un tema dedicado.
* Todos los componentes de Vault exponen su cambio de estado mediante mecanismos de push.

## Beneficios de las API de Streaming

* **Acceso en tiempo casi real** a mutaciones de datos.
* **Entrega garantizada al menos una vez**.
* **Escalabilidad horizontal** vía Kafka.
* **Elimina procesos por lotes** y reduce carga operativa del core.
* **Desacopla la base de datos del modelo de eventos**, facilitando nuevas integraciones.
* **Acceso granular** a un modelo de datos extensible.

## Tipos de datos transmitidos

* **Hechos**: creación de recursos (nueva cuenta, nueva publicación, etc.).
* **Mutaciones**: actualizaciones de recursos (cambio de estado, parámetros, saldo, etc.).

## Casos de uso comunes

### 1. Personalización y fidelización del cliente

* Alertas predictivas.
* Retos/gamificación.
* Categorización en tiempo real.
* Reglas tipo "si-entonces" para automatizaciones.

### 2. Gestión de liquidez en tiempo real

* Seguimiento granular de liquidez.
* Fuente única de verdad para datos financieros.
* Núcleo 24/7 en múltiples entidades.
* Asignación dinámica de reservas vía APIs.

### 3. Productos personalizados en tiempo real

* Adaptación dinámica de contratos según comportamiento.
* Segmentación y targeting usando datos en vivo.
* Simulación de precios y condiciones contextuales.

---

## Resumen

Vault Core ofrece una plataforma bancaria moderna que expone datos operativos y financieros casi en tiempo real. Sus API de transmisión permiten a los bancos crear soluciones más ágiles, automatizadas y centradas en el cliente, con una infraestructura preparada para el futuro.

---

[Anterior](https://github.com/wilfredoha/vault-core/blob/main/Vault%20Core%20Fundamentals/05_Vault%20Core%20Product%20and%20Integration%20Libraries.md) [Siguiente](https://github.com/wilfredoha/vault-core/blob/main/Vault%20Core%20Fundamentals/07_Vault%20Core%20Smart%20Contracts.md)

[Inicio](https://github.com/wilfredoha/vault-core/tree/main)