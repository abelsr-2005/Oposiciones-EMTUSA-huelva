# Tema 14 — Microsoft SQL Server

### Administración, seguridad y automatización en bases de datos

> Apuntes sobre instalación, gestión de usuarios, diseño de objetos y automatización en Microsoft SQL Server.

---

# 1. Instalación, Configuración y Conexiones Remotas

La instalación correcta del motor de base de datos es fundamental para garantizar el **rendimiento, la seguridad y la accesibilidad** de las aplicaciones.

---

## Instalación y configuración

Durante la instalación de **Microsoft SQL Server** se deben configurar distintos parámetros importantes:

* memoria utilizada por el motor
* ubicación del almacenamiento
* configuración regional y **colación de caracteres**

Estas configuraciones influyen directamente en el rendimiento y compatibilidad de la base de datos.

---

## Conexiones remotas

Para permitir el acceso desde otros equipos de la red es necesario habilitar las **conexiones remotas**.

Configuraciones necesarias:

* habilitar el protocolo **TCP/IP**
* permitir conexiones externas al servidor
* abrir el puerto correspondiente en el firewall

---

## Puerto por defecto

SQL Server escucha normalmente en el puerto:

```
TCP 1433
```

Este puerto permite que aplicaciones y herramientas de administración se conecten al servidor.

---

# 2. Administración de Usuarios, Roles y Permisos

La seguridad en SQL Server se gestiona mediante una **estructura jerárquica de identidades y permisos**.

---

## Logins y usuarios

En SQL Server existen dos niveles de identidad:

| Nivel   | Descripción                                      |
| ------- | ------------------------------------------------ |
| Login   | Identidad a nivel de instancia de SQL Server     |
| Usuario | Identidad dentro de una base de datos específica |

Un **login** se asocia a un **usuario** dentro de cada base de datos.

---

## Roles y permisos

Los **roles** agrupan permisos para simplificar la administración.

Ejemplos de roles predefinidos:

| Rol           | Función                                |
| ------------- | -------------------------------------- |
| db_datareader | Permite leer datos de todas las tablas |
| db_datawriter | Permite modificar datos                |
| db_owner      | Control total sobre la base de datos   |

Esto permite asignar privilegios sin tener que configurar permisos individuales para cada usuario.

---

# 3. Diseño y Gestión de Objetos

Los **objetos de base de datos** son estructuras lógicas que permiten almacenar y manipular información.

---

## Tablas

Las **tablas** son los objetos principales donde se almacenan los datos.

Características:

* organizadas en **filas y columnas**
* cada fila representa un registro
* cada columna representa un atributo

---

## Vistas

Una **vista** es una consulta almacenada que se presenta como una tabla virtual.

Ventajas:

* simplificar consultas complejas
* mejorar la seguridad ocultando datos sensibles

---

## Funciones definidas por el usuario (UDF)

Las **User Defined Functions (UDF)** son rutinas que:

* aceptan parámetros
* ejecutan operaciones
* devuelven un resultado

Se utilizan para reutilizar lógica dentro de consultas.

---

# 4. Procedimientos, Triggers y Optimización

SQL Server permite programar lógica directamente dentro del servidor.

---

## Procedimientos almacenados

Un **procedimiento almacenado** es un conjunto de instrucciones **T-SQL** que se ejecutan como una única unidad.

Ventajas:

* reutilización de código
* mejora del rendimiento
* mayor seguridad

---

## Triggers (Disparadores)

Los **triggers** son procedimientos que se ejecutan automáticamente cuando ocurre un evento en una tabla.

Eventos más comunes:

* INSERT
* UPDATE
* DELETE

Se utilizan para:

* auditoría
* validación de datos
* automatización de procesos

---

## Funciones de tabla

Son funciones que devuelven un **conjunto de resultados en formato tabla**.

Se pueden utilizar dentro de consultas SQL.

---

## Optimización de consultas

La optimización busca mejorar el rendimiento de las consultas.

Técnicas comunes:

* uso de **índices**
* optimización de consultas T-SQL
* análisis de planes de ejecución

---

# 5. Integración y Automatización (SSIS)

SQL Server incluye herramientas para la **integración y automatización de procesos de datos**.

---

## SSIS (SQL Server Integration Services)

SSIS permite crear procesos **ETL (Extract, Transform, Load)**.

Funciones principales:

* extracción de datos
* transformación de información
* carga en bases de datos o almacenes de datos

Los procesos se implementan mediante **paquetes SSIS**.

---

## Automatización con SQL Server Agent

El **SQL Server Agent** permite programar tareas automáticas.

Ejemplos de tareas:

* ejecución de paquetes SSIS
* copias de seguridad programadas
* mantenimiento de bases de datos

Esto permite automatizar procesos recurrentes dentro del servidor de bases de datos.
