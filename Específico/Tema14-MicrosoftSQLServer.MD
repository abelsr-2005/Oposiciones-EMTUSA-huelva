# 🗄️ Tema 14 — Microsoft SQL Server

## 📚 Introducción

**Microsoft SQL Server** es un sistema gestor de bases de datos relacional (RDBMS) desarrollado por Microsoft. Está diseñado para almacenar, gestionar y procesar grandes volúmenes de información de forma segura y eficiente.

Se utiliza ampliamente en entornos empresariales para soportar aplicaciones corporativas, sistemas de información, servicios web y herramientas de análisis de datos. SQL Server incluye múltiples componentes que permiten no solo gestionar datos, sino también automatizar tareas, integrar información de diferentes fuentes y optimizar el rendimiento de las consultas.

Entre las herramientas más utilizadas se encuentran:

* **SQL Server Management Studio (SSMS)** para administración
* **SQL Server Agent** para automatización
* **SQL Server Integration Services (SSIS)** para integración de datos

---

# ⚙️ 1. Instalación, Configuración y Conexiones Remotas

La instalación adecuada del servidor de base de datos es esencial para garantizar **seguridad, rendimiento y disponibilidad** de las aplicaciones que dependen de él.

## 🧩 Instalación y configuración

Durante la instalación de **Microsoft SQL Server** se configuran varios componentes fundamentales:

* Motor de base de datos (Database Engine)
* Servicios de integración
* Servicios de análisis
* Herramientas de administración

Entre los parámetros importantes de configuración destacan:

* **Asignación de memoria al motor de base de datos**
* **Ubicación de archivos de datos y logs**
* **Configuración de la colación (collation)**

La **colación** define reglas de comparación de texto, como ordenación alfabética y sensibilidad a mayúsculas o acentos.

Una configuración adecuada mejora el rendimiento y evita problemas de compatibilidad con aplicaciones.

## 🌐 Conexiones remotas

Para permitir el acceso desde otros equipos es necesario habilitar las **conexiones remotas al servidor SQL**.

Las configuraciones principales incluyen:

* habilitar el protocolo **TCP/IP** desde SQL Server Configuration Manager
* permitir conexiones remotas en la configuración del servidor
* configurar correctamente el **firewall del sistema operativo**

Estas configuraciones permiten que aplicaciones externas puedan conectarse al servidor.

## 🔌 Puerto por defecto

El puerto de red utilizado habitualmente por SQL Server es:

```
TCP 1433
```

Este puerto es utilizado por clientes y herramientas administrativas para establecer conexión con la base de datos.

---

# 👥 2. Administración de Usuarios, Roles y Permisos

SQL Server dispone de un sistema de seguridad basado en **autenticación y autorización** que permite controlar el acceso a los datos.

## 🔐 Logins y usuarios

Existen dos niveles principales de identidad:

| Nivel   | Descripción                                    |
| ------- | ---------------------------------------------- |
| Login   | Identidad a nivel de instancia de SQL Server   |
| Usuario | Identidad dentro de una base de datos concreta |

Un **login** permite acceder al servidor SQL, mientras que el **usuario** define los permisos dentro de cada base de datos.

SQL Server admite dos tipos de autenticación:

* **Autenticación de Windows** (integrada con Active Directory)
* **Autenticación SQL Server** (usuario y contraseña propios)

## 🧩 Roles y permisos

Para simplificar la administración, SQL Server utiliza **roles**, que agrupan permisos.

Ejemplos de roles de base de datos:

| Rol           | Función                                      |
| ------------- | -------------------------------------------- |
| db_datareader | Permite leer datos de todas las tablas       |
| db_datawriter | Permite insertar, modificar y eliminar datos |
| db_owner      | Control total sobre la base de datos         |

La asignación de roles permite administrar permisos de forma más eficiente.

---

# 🧱 3. Diseño y Gestión de Objetos

Los **objetos de base de datos** son estructuras que permiten almacenar y manipular datos dentro del sistema.

## 📊 Tablas

Las **tablas** son el elemento principal de almacenamiento de datos en una base de datos relacional.

Características:

* organizadas en **filas (registros)** y **columnas (campos)**
* cada columna tiene un tipo de dato específico
* pueden incluir **claves primarias y foráneas**

Las claves permiten establecer relaciones entre diferentes tablas.

## 👁️ Vistas

Una **vista** es una consulta almacenada que se presenta como una tabla virtual.

Ventajas:

* simplificar consultas complejas
* ocultar información sensible
* reutilizar consultas frecuentes

Las vistas no almacenan datos propios, sino que muestran información de las tablas subyacentes.

## 🔧 Funciones definidas por el usuario (UDF)

Las **User Defined Functions (UDF)** permiten encapsular lógica reutilizable dentro de la base de datos.

Características:

* pueden recibir parámetros
* devuelven un valor o una tabla
* se utilizan dentro de consultas SQL

Las UDF ayudan a organizar y reutilizar lógica de negocio.

---

# 🧠 4. Procedimientos, Triggers y Optimización

SQL Server permite implementar lógica directamente en el servidor mediante objetos programables.

## 📜 Procedimientos almacenados

Un **procedimiento almacenado** es un conjunto de instrucciones **T-SQL** almacenadas en la base de datos.

Ventajas:

* reutilización de código
* mejor rendimiento
* reducción del tráfico entre aplicación y servidor

Los procedimientos almacenados se ejecutan mediante comandos como:

```sql
EXEC NombreProcedimiento
```

## ⚡ Triggers (Disparadores)

Los **triggers** son procedimientos que se ejecutan automáticamente cuando ocurre un evento sobre una tabla.

Eventos más comunes:

* INSERT
* UPDATE
* DELETE

Se utilizan para:

* auditoría de cambios
* validación de datos
* automatización de procesos

## 📑 Funciones de tabla

Las funciones de tabla devuelven un conjunto de resultados con formato de tabla.

Pueden utilizarse dentro de consultas como si fueran tablas normales.

## 🚀 Optimización de consultas

La optimización busca mejorar el rendimiento de las consultas SQL.

Técnicas habituales:

* creación de **índices**
* revisión de consultas T-SQL
* análisis de **planes de ejecución**
* normalización de bases de datos

Estas técnicas ayudan a reducir tiempos de respuesta y mejorar el rendimiento del sistema.

---

# 🔄 5. Integración y Automatización (SSIS)

SQL Server incluye herramientas orientadas a la **integración de datos y automatización de procesos**.

## 🔗 SQL Server Integration Services (SSIS)

**SSIS** es una plataforma utilizada para realizar procesos **ETL (Extract, Transform, Load)**.

Permite:

* extraer datos desde múltiples fuentes
* transformar y limpiar información
* cargar datos en bases de datos o almacenes de datos

Los procesos se implementan mediante **paquetes SSIS** que pueden ejecutarse manualmente o de forma automática.

## ⏱️ Automatización con SQL Server Agent

El **SQL Server Agent** es un servicio que permite programar tareas automáticas dentro del servidor.

Ejemplos de tareas automatizadas:

* copias de seguridad programadas
* ejecución de paquetes SSIS
* mantenimiento de índices
* ejecución de scripts de administración

Esto permite automatizar operaciones periódicas y garantizar el mantenimiento adecuado del sistema de bases de datos.
