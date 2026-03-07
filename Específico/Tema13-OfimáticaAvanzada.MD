# 🧾 Tema 13 — Ofimática Avanzada

## 📚 Introducción

La ofimática avanzada en entornos corporativos se centra en el uso eficiente de herramientas de productividad, la automatización de tareas y la administración centralizada de aplicaciones y usuarios. En este contexto, **Microsoft 365** se ha consolidado como una de las plataformas más utilizadas en organizaciones públicas y privadas.

Microsoft 365 integra aplicaciones de oficina, almacenamiento en la nube, herramientas de colaboración y sistemas de administración centralizada. Esto permite mejorar la productividad, facilitar el trabajo en equipo y simplificar la gestión de infraestructuras de software en organizaciones con muchos usuarios.

---

# ☁️ 1. Uso Avanzado de Microsoft 365 y Colaboración en Línea

**Microsoft 365** es una plataforma basada en la nube que combina aplicaciones tradicionales de Office con servicios de almacenamiento y colaboración.

Entre las aplicaciones más utilizadas se encuentran:

* Microsoft Word
* Microsoft Excel
* Microsoft PowerPoint
* Microsoft Outlook
* Microsoft Teams

Estas aplicaciones pueden utilizarse tanto en **versiones de escritorio** como en **versiones web**, permitiendo acceder a los documentos desde diferentes dispositivos.

## 🤝 Colaboración en línea

Una de las características más importantes de Microsoft 365 es la **coautoría en tiempo real**, que permite a varios usuarios trabajar simultáneamente en un mismo documento.

Los archivos se almacenan normalmente en:

* **OneDrive** → almacenamiento personal en la nube
* **SharePoint** → almacenamiento compartido y colaboración empresarial

Ventajas principales:

* edición simultánea por múltiples usuarios
* control automático de versiones
* acceso remoto desde cualquier dispositivo
* historial de cambios y recuperación de versiones anteriores

Esto facilita el trabajo colaborativo en equipos distribuidos.

## 📝 Microsoft Forms

**Microsoft Forms** es una herramienta de Microsoft 365 utilizada para crear formularios, encuestas y cuestionarios.

Sus principales funciones incluyen:

* recopilación automática de respuestas
* generación de gráficos de resultados
* exportación de datos a **Microsoft Excel**
* acceso mediante enlaces o códigos QR

Se utiliza con frecuencia para:

* encuestas internas
* evaluaciones
* recopilación de información de usuarios

## 🔗 Integración entre aplicaciones

Las aplicaciones de Microsoft 365 están diseñadas para integrarse entre sí.

Ejemplos de integración:

* insertar hojas o gráficos de **Excel** dentro de documentos **Word** o presentaciones **PowerPoint**
* compartir documentos directamente desde **Teams**
* almacenar archivos automáticamente en **OneDrive o SharePoint**

Esta integración permite mantener la información sincronizada y mejorar la productividad de los usuarios.

---

# ⚙️ 2. Automatización y Macros

La **automatización de tareas** permite reducir el trabajo manual repetitivo y mejorar la eficiencia en el uso de aplicaciones ofimáticas.

En Microsoft 365 existen diferentes herramientas para automatizar procesos.

## 🧠 Macros (VBA)

Las **macros** son secuencias de instrucciones escritas en **VBA (Visual Basic for Applications)** que permiten automatizar tareas dentro de aplicaciones de Microsoft Office.

Las macros pueden:

* ejecutar procesos repetitivos
* manipular datos de forma automática
* generar informes
* realizar cálculos complejos

Se utilizan principalmente en:

* **Microsoft Excel**
* **Microsoft Word**

Las macros se ejecutan desde el propio documento o desde plantillas predefinidas.

Por motivos de seguridad, muchas organizaciones restringen o controlan su ejecución mediante políticas administrativas.

## 🔄 Power Automate

**Power Automate** es una herramienta de Microsoft que permite crear flujos de trabajo automáticos entre aplicaciones y servicios.

Permite automatizar procesos sin necesidad de programación avanzada.

Ejemplo de flujo automatizado:

Correo recibido en Outlook
↓
Guardar archivo adjunto
↓
Almacenarlo automáticamente en SharePoint

Ventajas:

* integración con numerosos servicios
* automatización de procesos empresariales
* reducción de tareas manuales

## 📊 Excel Avanzado — Power Query

**Power Query** es una herramienta de Excel utilizada para importar, transformar y preparar datos.

Se utiliza en procesos conocidos como **ETL (Extract, Transform, Load)**.

Funciones principales:

* importar datos desde bases de datos, archivos o servicios web
* limpiar y transformar información
* combinar datos de diferentes fuentes
* cargar los datos procesados en Excel

Esto permite trabajar con grandes volúmenes de datos sin necesidad de programación compleja.

---

# 👥 3. Administración Centralizada de Usuarios y Licencias

En entornos corporativos, la gestión de usuarios y licencias se realiza de forma centralizada mediante herramientas de administración.

Esto permite controlar el acceso a aplicaciones, asignar licencias y gestionar configuraciones de seguridad.

## 🖥️ Centro de Administración de Microsoft 365

El **Centro de Administración de Microsoft 365** es el portal principal para gestionar la plataforma.

Desde este portal se pueden realizar tareas como:

* crear y administrar usuarios
* asignar o retirar licencias
* gestionar grupos
* administrar dispositivos
* configurar políticas de seguridad

Este sistema permite a los administradores gestionar grandes entornos empresariales desde una única interfaz.

## 👨‍👩‍👧 Grupos de Seguridad y Grupos de Microsoft 365

Los **grupos** permiten administrar permisos de forma eficiente para múltiples usuarios.

Tipos de grupos:

**Grupos de seguridad**

* utilizados para asignar permisos
* integrados con Active Directory

**Grupos de Microsoft 365**

* orientados a la colaboración
* incluyen herramientas como correo, calendario y almacenamiento compartido

La utilización de grupos simplifica la administración de accesos y licencias.

## 💻 Activación en Equipos Compartidos (SCA)

La **Shared Computer Activation (SCA)** permite utilizar Microsoft 365 en equipos utilizados por varios usuarios.

Ejemplos de uso:

* servidores **Remote Desktop Services (RDS)**
* aulas informáticas
* entornos de trabajo compartidos

Cada usuario inicia sesión con su cuenta y activa temporalmente las aplicaciones con su propia licencia.

---

# 🛠️ 4. Instalación, Configuración y Políticas de Actualización

En organizaciones grandes, Microsoft 365 se despliega mediante herramientas de instalación centralizada para facilitar la administración y el mantenimiento.

## 📦 Office Deployment Tool (ODT)

La **Office Deployment Tool (ODT)** es una herramienta de línea de comandos utilizada para instalar y configurar Microsoft 365.

Utiliza un archivo de configuración llamado:

```
configuration.xml
```

Este archivo permite definir:

* qué aplicaciones instalar
* idioma del sistema
* arquitectura (32 o 64 bits)
* canal de actualización
* ubicación de descarga de archivos

Esto permite desplegar Office de forma automatizada en múltiples equipos.

## 🔄 Canales de actualización

Microsoft 365 utiliza diferentes canales de actualización que determinan la frecuencia con la que se reciben nuevas versiones y mejoras.

| Canal           | Características                              |
| --------------- | -------------------------------------------- |
| Canal mensual   | Recibe nuevas funciones con mayor frecuencia |
| Canal semestral | Mayor estabilidad y pruebas previas          |

Las organizaciones suelen utilizar el **canal semestral** para garantizar estabilidad en entornos corporativos.

## 🧩 Políticas de Grupo (GPO) para Office

Las **GPO (Group Policy Objects)** permiten administrar configuraciones de Microsoft Office desde un servidor de dominio.

Estas políticas se aplican utilizando **plantillas administrativas ADMX**.

Ejemplos de configuraciones posibles:

* deshabilitar macros por motivos de seguridad
* bloquear complementos no autorizados
* controlar actualizaciones automáticas
* configurar opciones de privacidad

El uso de GPO permite aplicar políticas de forma centralizada en todos los equipos de la organización.
