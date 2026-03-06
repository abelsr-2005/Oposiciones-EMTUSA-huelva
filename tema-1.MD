# TEMA 1: Informática Básica y Nociones de Seguridad

> **Objetivo del examen:** Dominar conceptos fundamentales sobre el hardware y el software, sistemas de almacenamiento de datos, sistemas operativos y nociones básicas de seguridad informática.

---

## 1.1. Conceptos Fundamentales: Hardware y Software

* **Hardware:** Sustrato físico del equipo (CPU, memoria, periféricos).
* **Software:** Componente lógico e intangible.
* **Firmware:** Software de bajo nivel incrustado en hardware no volátil (ej. BIOS/UEFI). Actúa como puente directo entre el hardware y el sistema operativo.

### ⚠️ Trampas de Examen (Tipologías de Software)
En las preguntas tipo test es crucial no confundir las capas lógicas:
1. **Software de Sistema:** Sistema Operativo, controladores (drivers). Su fin es gestionar el hardware.
2. **Software de Aplicación:** Programas para el usuario final (Word, Excel, navegadores).
3. **Software de Programación:** Entornos y herramientas para crear otro software (Compiladores, Visual Studio).

---

## 1.2. Sistemas de Almacenamiento de Datos

### 1.2.1. Clasificación por Volatilidad
* **Volátil:** Pierde la información sin suministro eléctrico. (Ej. Memoria RAM, Caché, Registros de CPU).
* **No Volátil:** Retiene la información sin energía. (Ej. Memoria ROM, HDD magnéticos, SSD/NVMe basados en NAND Flash).

### 1.2.2. Jerarquía de Memoria
A medida que la memoria está más cerca de la CPU:
* **Mayor** velocidad y coste.
* **Menor** capacidad de almacenamiento.
* *Orden (de mayor a menor velocidad):* Registros -> Caché L1/L2/L3 -> RAM -> Almacenamiento Secundario (SSD/HDD).

### ⚠️ Trampas de Examen (Almacenamiento)
* **RAM vs ROM:** Asumir que la ROM es volátil es un error crítico. La ROM (Read-Only Memory) es **no volátil**.
* **SSD vs HDD:** Los SSD **no tienen partes mecánicas ni móviles**, eliminan el tiempo de búsqueda mecánica físico de los HDD magnéticos.

---

## 1.3. Sistemas Operativos (SO)

* **Definición de examen:** Es el *software* (no hardware) base encargado de administrar y gestionar los recursos del hardware, actuando como intermediario y proporcionando servicios a los programas de aplicación.
* **Funciones Centrales:** Gestión de procesos (CPU), gestión de memoria principal, gestión de almacenamiento y gestión de Entrada/Salida (E/S).

### ⚠️ Trampas de Examen (Funciones del SO)
* **El SO no ejecuta aplicaciones:** El SO *gestiona los recursos* para que la CPU pueda ejecutar las instrucciones de las aplicaciones. 

---

## 1.4. Nociones Básicas de Seguridad Informática

La seguridad base se sustenta en la **Tríada CIA**:

1. **Confidencialidad:** Garantiza que la información solo sea accesible (leída) por personal autorizado.
2. **Integridad:** Garantiza que la información no sea modificada ni alterada por personal no autorizado.
3. **Disponibilidad:** Garantiza que los sistemas y datos estén accesibles cuando se requieran.

### ⚠️ Trampas de Examen (Seguridad)
* **Confidencialidad vs Integridad:** Es el fallo más común en los test. Si el enunciado habla de "evitar que los datos sean alterados", la respuesta correcta siempre es **Integridad**, no Confidencialidad.
