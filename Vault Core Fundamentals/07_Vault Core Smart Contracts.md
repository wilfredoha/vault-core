# Vault Core Smart Contracts: Introducción

## ¿Qué es un Smart Contract?
Un **Smart Contract** en Vault es código Python que define la lógica financiera de un producto bancario (cuenta, préstamo, etc.).

### Características clave
* **Transparente**: lógica visible y auditable.  
* **Autónomo**: ejecuta acciones automáticamente.  
* **Parametrizable**: configurable con parámetros.  
* **Flexible**: se puede actualizar bajo demanda.  
* **Configuración como código**: escrito como un módulo en Python.  

---

## ¿Cuáles son los beneficios comerciales?
* Desacopla al banco del proveedor: más independencia.  
* Permite hiperpersonalización de productos.  
* Reduce el tiempo de lanzamiento (go to market).  
* Mejora la trazabilidad y estandarización.  
* Todos los productos se ejecutan sobre una única plataforma central.  

---

## Ganchos (Hooks) en los Smart Contracts
Los hooks son funciones que ejecutan lógica al ocurrir ciertos eventos.

### Tipos de hooks:
* `activation_hook`  
* `deactivation_hook`  
* `pre_posting_hook` / `post_posting_hook`  
* `scheduled_event_hook`  
* `pre_parameter_change_hook` / `post_parameter_change_hook`  
* `conversion_hook`  

### Decoradores útiles:
* `@fetch_account_data` para recuperar saldos, parámetros, publicaciones  
* `@requires(parametros=True)` para indicar que se usan parámetros  

---

## Estructura básica de un Smart Contract

Un contrato incluye:
* **Metadatos**: versión, nombre, resumen, tipo (activo/pasivo)  
* **Parámetros**: definidos y esperados  
* **Eventos programados**  
* **Data fetchers**: recuperadores de datos  
* **Hooks**: funciones que contienen la lógica  

### Ejemplo de encabezado:
* `API = "4.0.0"`  
* `version = "1.0.0"`  
* `display_name = "Cuenta Corriente"`  

---

## Parámetros, series temporales y banderas

### Parámetros
* Tipos: `String`, `Decimal`, `Enum`, `DateTime`, `Account`  
* Niveles:  
  * `Global` (toda la bóveda)  
  * `Template` (todos los clientes de un producto)  
  * `Instance` (único por cuenta)  
  * `Derivados` (calculados)

### Series temporales
* Permiten acceder a valores históricos de parámetros, saldos o flags.  
* Ejemplo: ver el saldo al cierre de ayer o la tasa histórica.  

### Banderas
* Booleanas, para activar o desactivar comportamientos.  
* Usos: morosidad, feriados de pago, cliente inactivo, beneficios.

---

## Pruebas de Smart Contracts

Vault Core admite 3 tipos de pruebas:

* **Unitarias**: prueba individual de funciones.  
* **Simulación**: interacción completa en un entorno virtual.  
* **Sistema**: ejecución del contrato en un entorno real de Vault.  

Las pruebas verifican:
* Publicaciones aceptadas/rechazadas correctamente  
* Eventos ejecutados correctamente  
* Cálculo correcto de parámetros derivados  

---

## Conclusión

Con Smart Contracts en Vault Core puedes:
* Diseñar productos personalizados como código  
* Controlar completamente la lógica de negocio  
* Parametrizar sin modificar código  
* Validar funcionalidad mediante pruebas  

Para más información, consulta la documentación oficial de Vault.

---

[Anterior](https://github.com/wilfredoha/vault-core/blob/main/Vault%20Core%20Fundamentals/06_Vault%20Core%20Data%20Streaming.md) [Siguiente](https://github.com/wilfredoha/vault-core/blob/main/Vault%20Core%20Fundamentals/08_Vault%20Core%20End%20Of%20Day.md)

[Inicio](https://github.com/wilfredoha/vault-core/tree/main)