# Tema 13 — Ofimática Avanzada

### Microsoft 365, automatización y administración corporativa

> Apuntes sobre herramientas avanzadas de Microsoft 365, automatización de tareas, administración de licencias y despliegue de Office en entornos empresariales.

---

## 📑 Índice

* [1. Uso avanzado de Microsoft 365](#1-uso-avanzado-de-microsoft-365-y-colaboración-en-línea)
* [2. Automatización y macros](#2-automatización-y-macros)
* [3. Administración de usuarios y licencias](#3-administración-centralizada-de-usuarios-y-licencias)
* [4. Instalación y políticas de actualización](#4-instalación-configuración-y-políticas-de-actualización)

---

# 1. Uso Avanzado de Microsoft 365 y Colaboración en Línea

**Microsoft 365** es una plataforma de productividad basada en la nube que integra aplicaciones de oficina, almacenamiento y herramientas de colaboración.

Permite trabajar de forma colaborativa desde cualquier dispositivo conectado a Internet.

---

## Colaboración en línea

Microsoft 365 permite la **coautoría en tiempo real** en documentos compartidos.

Aplicaciones compatibles:

* Word
* Excel
* PowerPoint

Los archivos se almacenan normalmente en:

* **OneDrive**
* **SharePoint**

Ventajas:

* edición simultánea
* control de versiones
* acceso remoto

---

## Microsoft Forms

**Microsoft Forms** es una herramienta para crear:

* formularios
* encuestas
* cuestionarios

Características:

* recopilación automática de respuestas
* exportación directa a **Excel**
* visualización de resultados en tiempo real

---

## Integración entre aplicaciones

Las aplicaciones de Microsoft 365 pueden integrarse entre sí.

Ejemplos:

* insertar gráficos de **Excel** en **Word** o **PowerPoint**
* vincular datos para que se actualicen automáticamente

Esto permite mantener la información sincronizada entre documentos.

---

# 2. Automatización y Macros

La **automatización** permite reducir tareas repetitivas y minimizar errores humanos.

---

## Macros (VBA)

Las **macros** son scripts escritos en **Visual Basic for Applications (VBA)**.

Permiten:

* automatizar procesos
* ejecutar tareas complejas
* manipular datos automáticamente

Se utilizan principalmente en la versión de escritorio de **Microsoft Office**.

---

## Power Automate

**Power Automate** es una herramienta de automatización incluida en Microsoft 365.

Permite crear **flujos de trabajo automáticos entre aplicaciones**.

Ejemplo de flujo:

```
Correo recibido en Outlook
↓
Guardar archivo adjunto automáticamente
↓
Almacenarlo en SharePoint
```

Ventajas:

* integración entre servicios
* automatización sin programación avanzada

---

## Excel Avanzado — Power Query

**Power Query** permite realizar procesos de **ETL (Extract, Transform, Load)**.

Funciones principales:

* importar datos de múltiples fuentes
* limpiar y transformar datos
* cargar los datos en Excel

Todo esto sin necesidad de programación compleja.

---

# 3. Administración Centralizada de Usuarios y Licencias

En entornos corporativos la administración se realiza de forma **centralizada**, no equipo por equipo.

---

## Centro de Administración de Microsoft 365

Portal web que permite gestionar:

* usuarios
* licencias
* grupos
* configuraciones de seguridad

Funciones principales:

* creación de usuarios
* asignación de licencias
* gestión de dispositivos

---

## Grupos de Seguridad y Microsoft 365

Los **grupos** permiten administrar permisos de forma masiva.

Tipos de grupos:

* **Grupos de seguridad** → control de permisos
* **Grupos de Microsoft 365** → colaboración entre usuarios

Ventaja principal:

* aplicar permisos o licencias a varios usuarios a la vez

---

## Activación en Equipos Compartidos (SCA)

La **Shared Computer Activation (SCA)** permite utilizar Microsoft 365 en equipos compartidos.

Uso típico:

* servidores **Remote Desktop Services (RDS)**
* entornos con múltiples usuarios

Cada usuario inicia sesión con su propia licencia.

---

# 4. Instalación, Configuración y Políticas de Actualización

La instalación de Microsoft 365 en entornos corporativos se realiza mediante herramientas de despliegue centralizado.

---

## Herramienta de implementación de Office (ODT)

La **Office Deployment Tool (ODT)** permite instalar Office mediante línea de comandos.

Utiliza un archivo:

```
configuration.xml
```

Permite configurar:

* aplicaciones que se instalarán
* idioma
* arquitectura (32 o 64 bits)
* canal de actualización

---

## Canales de actualización

Los canales definen la frecuencia con la que se reciben actualizaciones.

| Canal           | Características                                 |
| --------------- | ----------------------------------------------- |
| Canal mensual   | Actualizaciones frecuentes con nuevas funciones |
| Canal semestral | Mayor estabilidad, recomendado para empresas    |

---

## Políticas de Grupo (GPO) para Office

Las **GPO (Group Policy Objects)** permiten administrar configuraciones de Office desde el servidor.

Se utilizan **plantillas administrativas ADMX**.

Ejemplos de configuraciones:

* deshabilitar macros por seguridad
* bloquear complementos
* controlar actualizaciones

Esto permite aplicar políticas de seguridad de forma centralizada en toda la organización.
