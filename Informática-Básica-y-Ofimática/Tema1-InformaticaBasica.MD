# 💻 TEMA 1: Informática Básica y Nociones de Seguridad

## 📘 Introducción

Un sistema informático está formado por un conjunto de elementos físicos y lógicos que trabajan conjuntamente para procesar, almacenar y transmitir información. Estos elementos se agrupan principalmente en **hardware** y **software**, y su funcionamiento está coordinado por el **sistema operativo**.

Además, en cualquier sistema informático moderno es fundamental tener en cuenta los principios básicos de **seguridad informática**, que garantizan la protección de la información.

---

# 🧩 1. Conceptos Fundamentales: Hardware, Software y Firmware

## 🖥️ 1.1 Hardware

El **hardware** es el conjunto de **componentes físicos y tangibles** que forman parte de un sistema informático. Es decir, todos aquellos elementos que se pueden ver y tocar.

Entre los principales componentes del hardware se encuentran:

### 🧠 CPU (Unidad Central de Procesamiento)

La **CPU** es el componente encargado de ejecutar instrucciones y procesar datos. Se suele denominar el **"cerebro" del ordenador**.

Sus funciones principales son:

* Interpretar instrucciones de los programas.
* Realizar operaciones aritméticas y lógicas.
* Controlar el funcionamiento del resto de componentes.

### 💾 Memoria

La memoria permite **almacenar datos e instrucciones** que necesita el ordenador para funcionar.

Existen distintos tipos de memoria que se diferencian por su velocidad, capacidad y permanencia de los datos.

### 🗄️ Dispositivos de almacenamiento

Son dispositivos que permiten **guardar información de forma permanente** para poder utilizarla posteriormente.

Ejemplos:

* Discos duros
* Unidades SSD
* Memorias USB
* Tarjetas de memoria

### ⌨️ Periféricos

Los **periféricos** son dispositivos que permiten la comunicación entre el usuario y el ordenador.

Se clasifican en:

**Periféricos de entrada**

Permiten introducir información en el sistema.

Ejemplos:

* Teclado
* Ratón
* Escáner
* Micrófono

**Periféricos de salida**

Permiten mostrar la información generada por el ordenador.

Ejemplos:

* Monitor
* Impresora
* Altavoces

**Periféricos de entrada y salida**

Realizan ambas funciones.

Ejemplos:

* Pantallas táctiles
* Discos externos

---

## 🧾 1.2 Software

El **software** es el conjunto de **programas, instrucciones y datos** que permiten que el hardware funcione correctamente.

A diferencia del hardware, el software es **intangible**, ya que no tiene una forma física.

El software se clasifica en tres tipos principales.

### ⚙️ Software de sistema

Es el software encargado de **administrar y controlar el hardware del ordenador**.

Su función es servir de intermediario entre el hardware y el usuario.

Ejemplos:

* Sistemas operativos
* Controladores o drivers

### 📄 Software de aplicación

Son programas diseñados para que el usuario pueda **realizar tareas concretas**.

Ejemplos:

* Procesadores de texto
* Hojas de cálculo
* Navegadores web
* Programas de correo electrónico

### 🧑‍💻 Software de programación

Son herramientas que permiten **crear otros programas informáticos**.

Ejemplos:

* Compiladores
* Intérpretes
* Entornos de desarrollo

---

## 🔌 1.3 Firmware

El **firmware** es un tipo de software especial que se encuentra **integrado dentro del hardware**.

Se almacena en memorias **no volátiles**, por lo que permanece incluso cuando el dispositivo se apaga.

Su función es controlar el funcionamiento básico del hardware y facilitar la comunicación con el sistema operativo.

Un ejemplo típico es:

**BIOS o UEFI**, que se encarga de iniciar el ordenador y comprobar el hardware antes de que arranque el sistema operativo.

---

# 💽 2. Sistemas de Almacenamiento de Datos

Los sistemas de almacenamiento permiten **guardar información para su uso posterior**. Estos sistemas pueden clasificarse según distintos criterios, siendo uno de los más importantes la **volatilidad de la memoria**.

---

## ⚡ 2.1 Clasificación según volatilidad

### 🧠 Memoria volátil

La **memoria volátil** pierde la información cuando se interrumpe el suministro eléctrico.

Ejemplos:

* Memoria RAM
* Memoria caché
* Registros del procesador

La memoria RAM se utiliza para almacenar temporalmente:

* los programas que se están ejecutando
* los datos que está utilizando el sistema

Cuando el ordenador se apaga, toda la información almacenada en la RAM desaparece.

---

### 💾 Memoria no volátil

La **memoria no volátil** conserva la información incluso cuando el dispositivo está apagado.

Ejemplos:

* ROM
* Discos duros
* SSD
* Memorias USB
* Tarjetas de memoria

---

## 🗃️ 2.2 Tipos de almacenamiento

### 💿 HDD (Hard Disk Drive)

Los **HDD** son los discos duros tradicionales.

Funcionan mediante **platos magnéticos que giran a gran velocidad** y cabezales que leen y escriben la información.

Características:

* Tienen partes mecánicas
* Son más económicos
* Tienen mayor capacidad
* Son más lentos que los SSD

---

### ⚡ SSD (Solid State Drive)

Los **SSD** utilizan memoria flash para almacenar información.

Características:

* No tienen partes móviles
* Son mucho más rápidos
* Son más resistentes a golpes
* Consumen menos energía

---

## 🧱 2.3 Jerarquía de memoria

La memoria de un ordenador se organiza en una **jerarquía basada en velocidad, coste y capacidad**.

Cuanto más cerca está de la CPU:

* mayor velocidad
* mayor coste
* menor capacidad

Orden de mayor velocidad a menor:

1. Registros de CPU
2. Memoria caché
3. Memoria RAM
4. Almacenamiento secundario (SSD o HDD)

---

# 🖥️ 3. Sistemas Operativos

Un **sistema operativo (SO)** es el software fundamental que **gestiona los recursos del hardware y permite ejecutar aplicaciones**.

Actúa como **intermediario entre el usuario, las aplicaciones y el hardware**.

Ejemplos de sistemas operativos:

* Windows
* Linux
* macOS
* Android
* iOS

---

## ⚙️ 3.1 Funciones principales del sistema operativo

### 🔄 Gestión de procesos

El sistema operativo controla la ejecución de los programas y decide **qué proceso utiliza la CPU en cada momento**.

### 🧠 Gestión de memoria

Administra la **memoria RAM**, asignando espacio a los programas y liberándolo cuando dejan de utilizarlo.

### 📁 Gestión del sistema de archivos

Organiza la información almacenada en discos mediante **archivos y carpetas**.

### 🔌 Gestión de dispositivos de entrada y salida

Coordina el funcionamiento de los dispositivos periféricos como:

* teclado
* ratón
* impresoras
* discos

---

# 🔐 4. Nociones Básicas de Seguridad Informática

La **seguridad informática** tiene como objetivo proteger la información y los sistemas frente a accesos no autorizados, modificaciones indebidas o pérdida de datos.

El modelo fundamental de seguridad se basa en la llamada **Tríada CIA**.

---

## 🕵️ 4.1 Confidencialidad

La **confidencialidad** garantiza que la información **solo pueda ser accesible por personas autorizadas**.

Se consigue mediante mecanismos como:

* contraseñas
* cifrado
* control de accesos

---

## 🧾 4.2 Integridad

La **integridad** garantiza que la información **no sea modificada o alterada sin autorización**.

Esto asegura que los datos se mantengan correctos, completos y fiables.

Ejemplos de mecanismos que protegen la integridad:

* firmas digitales
* controles de verificación
* auditorías de datos

---

## 📡 4.3 Disponibilidad

La **disponibilidad** garantiza que los sistemas y la información **estén accesibles cuando se necesiten**.

Para asegurarla se utilizan medidas como:

* copias de seguridad
* servidores redundantes
* sistemas de recuperación ante desastres

---

# 🧠 Resumen de conceptos clave

Hardware → componentes físicos del ordenador.

Software → programas que permiten utilizar el hardware.

Firmware → software integrado en el hardware.

Memoria volátil → pierde datos sin electricidad (RAM).

Memoria no volátil → conserva datos (ROM, SSD, HDD).

Jerarquía de memoria → Registros → Caché → RAM → Disco.

Sistema operativo → software que gestiona los recursos del sistema.

Seguridad informática → basada en Confidencialidad, Integridad y Disponibilidad.
