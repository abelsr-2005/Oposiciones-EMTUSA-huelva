# TEMA 6: Bases de datos: Access 365

> **Objetivo del examen:** Dominar las funciones y utilidades de Access 365, la creación y gestión de tablas, la ejecución de consultas, el diseño de formularios y la generación de informes.

## 6.1. Principales funciones y utilidades
* **Definición:** Microsoft Access es un Sistema de Gestión de Bases de Datos Relacionales (SGBDR) diseñado para organizar, almacenar y recuperar información de manera eficiente.
* **Extensiones de archivo (Perspectiva IT):**
    * .accdb: Formato estándar predeterminado de Access 365.
    * .mdb: Formato heredado (versiones 2003 y anteriores).
* **Objetos fundamentales:** La arquitectura de Access se basa en cuatro objetos principales: Tablas, Consultas, Formularios e Informes.

## 6.2. Tablas
* **Estructura:** Es el objeto donde se almacenan físicamente los datos. Se organiza en **Campos** (columnas que definen el tipo de dato) y **Registros** (filas que contienen los datos individuales).
* **Clave Principal (Primary Key):** Campo que identifica de forma única cada registro. Es obligatorio para garantizar que no existan duplicados y es la base de las relaciones.
* **Tipos de datos comunes:** Texto corto (hasta 255 caracteres), Texto largo, Número, Fecha/Hora, Moneda y Autonumeración.

## 6.3. Consultas (Queries)
* Permiten extraer y manipular los datos almacenados en las tablas según criterios específicos.
* **Tipos de consultas:**
    * **De selección:** Extraen información para su visualización.
    * **De acción:** Modifican los datos (Actualización, Eliminación, Anexar o Creación de tablas).
    * **De parámetros:** Solicitan al usuario un valor de entrada antes de ejecutarse para filtrar los resultados.

## 6.4. Formularios e Informes
* **Formularios:** Objetos de interfaz diseñados para la introducción, edición y visualización de datos de manera amigable para el usuario.
* **Informes:** Objetos diseñados específicamente para la presentación, resumen y exportación/impresión de la información. A diferencia de los formularios, no permiten la edición de datos.

## 6.5. Relaciones e Integridad Referencial
* **Relaciones:** Vinculación entre tablas mediante campos comunes (Clave Principal en tabla origen y Clave Foránea en tabla destino).
* **Integridad Referencial:** Es la regla de oro de las bases de datos. Garantiza la coherencia de los datos al impedir:
    1. Eliminar un registro de una tabla primaria si tiene registros relacionados en otra tabla.
    2. Cambiar un valor de clave principal si existen registros que dependen de él.
    3. Introducir datos en una clave foránea que no existan previamente en la clave principal de la tabla relacionada.

### ⚠️ Alerta de Trampa (Lógica de Almacenamiento)
Pregunta clásica de examen: ¿En qué objeto se guardan los datos? Los datos **solo se almacenan en las Tablas**. Las consultas, formularios e informes son meras herramientas para manipular o visualizar dicha información, pero no contienen datos per se.
