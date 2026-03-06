# 📁 TEMA 3: El Explorador de Windows y Herramientas del sistema

## 📘 Introducción

El **Explorador de Windows** (File Explorer) es la herramienta principal que permite al usuario gestionar archivos, carpetas y unidades de almacenamiento dentro del sistema operativo Windows. A través de esta aplicación se pueden organizar documentos, copiar o mover información, buscar archivos y acceder a diferentes herramientas del sistema.

Dominar el Explorador de Windows es fundamental para trabajar de forma eficiente con el ordenador y administrar correctamente la información almacenada.

---

# 🧭 3.1 El Explorador de Windows (File Explorer)

El **Explorador de Windows** es la aplicación que proporciona la interfaz gráfica para interactuar con el sistema de archivos del ordenador.

Permite realizar tareas como:

* navegar entre carpetas
* abrir archivos
* copiar, mover o eliminar documentos
* gestionar unidades de almacenamiento

### ⌨️ Atajo de teclado

El Explorador de Windows puede abrirse rápidamente mediante el atajo:

**Windows + E**

Este es uno de los atajos más utilizados en el sistema operativo.

### 🧱 Estructura de la ventana del Explorador

El Explorador de Windows está compuesto por diferentes elementos que facilitan la navegación y gestión de archivos:

**Cinta de opciones (Ribbon)**
Contiene herramientas y comandos para realizar acciones como copiar, mover, eliminar o cambiar la vista de los archivos.

**Panel de navegación**
Se encuentra en la parte izquierda y permite acceder rápidamente a ubicaciones como Acceso rápido, Este equipo o unidades de almacenamiento.

**Barra de direcciones**
Muestra la ruta de la carpeta actual y permite navegar entre directorios.

**Caja de búsqueda**
Permite localizar archivos o carpetas dentro de la ubicación actual.

**Panel de vista previa o detalles**
Muestra información adicional sobre el archivo seleccionado.

### ⚠️ Punto importante para examen

En **Windows 10 y Windows 11**, al pulsar **Windows + E**, el Explorador se abre por defecto en la vista de **Acceso rápido**, no en "Este equipo".

---

# 📂 3.2 Gestión de carpetas y archivos

## 📄 Archivos

Un **archivo** es una unidad lógica de almacenamiento que contiene información.

Cada archivo se identifica mediante:

* un **nombre**
* una **extensión**

La extensión indica el tipo de archivo y el programa con el que suele abrirse.

Ejemplos:

* .docx → documento de Word
* .xlsx → hoja de cálculo de Excel
* .txt → archivo de texto
* .jpg → imagen

---

## 📁 Carpetas

Las **carpetas**, también llamadas **directorios**, son contenedores que permiten organizar archivos y otras carpetas.

Gracias a ellas se crea una estructura jerárquica que facilita la organización de la información.

Por ejemplo:

Documentos → Trabajo → Informes

---

## 🧭 Ruta (Path)

La **ruta** es la dirección que indica la ubicación de un archivo o carpeta dentro del sistema de archivos.

Puede ser:

**Ruta absoluta**
Indica la ubicación completa desde la raíz del sistema.

Ejemplo:

C:\Usuarios\Usuario\Documentos\Informe.docx

**Ruta relativa**
Indica la ubicación en relación con la carpeta actual.

---

## ⌨️ Operaciones básicas con archivos

El Explorador permite realizar diversas operaciones sobre archivos y carpetas.

### Renombrar

Para cambiar el nombre de un archivo o carpeta se puede:

* hacer clic derecho → Renombrar
* pulsar la tecla **F2**

La tecla **F2** es el método más rápido y suele aparecer en preguntas de examen.

---

### Eliminar archivos

Existen dos formas principales de eliminar archivos.

**Eliminación normal**
Pulsar la tecla **Supr** envía el archivo a la **Papelera de reciclaje**.

Esto significa que el archivo todavía puede recuperarse.

**Eliminación permanente**
Pulsar **Shift + Supr** elimina el archivo directamente sin pasar por la papelera.

En este caso la recuperación es mucho más difícil.

---

# ⭐ 3.3 Herramientas "Este equipo" y "Acceso rápido"

## 🖥️ Este equipo

**Este equipo** es una sección del Explorador que muestra los principales recursos del ordenador.

Incluye:

* discos duros
* unidades SSD
* unidades externas
* unidades de red
* carpetas del usuario

Antiguamente esta sección se conocía como **"Mi PC"** o **"Mi equipo"**.

---

## ⚡ Acceso rápido

**Acceso rápido** es una sección del Explorador que muestra:

* carpetas ancladas por el usuario
* carpetas usadas con frecuencia
* archivos abiertos recientemente

Su objetivo es permitir acceder rápidamente a las ubicaciones más utilizadas.

---

# 🔎 3.4 Operaciones de búsqueda

El Explorador de Windows permite buscar archivos utilizando el cuadro de búsqueda situado en la esquina superior derecha.

La búsqueda puede realizarse utilizando **caracteres comodín**, también llamados *wildcards*.

---

## ⭐ Asterisco (*)

El **asterisco** sustituye a cualquier número de caracteres.

Ejemplo:

*.txt

Mostrará todos los archivos con extensión .txt.

También puede utilizarse dentro del nombre del archivo.

Ejemplo:

informe*

Mostrará archivos como:

* informe
* informe1
* informe_final

---

## ❓ Interrogación (?)

El **signo de interrogación** sustituye exactamente **un solo carácter**.

Ejemplo:

file?.txt

Encontrará archivos como:

* file1.txt
* fileA.txt

Pero no encontrará:

* file10.txt

---

# 🛠️ 3.5 Accesorios y herramientas del sistema

Windows incluye diversas herramientas integradas que ayudan a realizar tareas básicas de administración y mantenimiento del sistema.

---

## 📝 Accesorios básicos

### Bloc de notas

Editor de texto simple que permite crear y editar **archivos de texto plano** sin formato.

### WordPad

Editor de texto más avanzado que el Bloc de notas, con soporte para **formato básico de texto**.

### Herramienta Recortes

Permite capturar partes de la pantalla para crear **capturas de pantalla**.

---

## ⚙️ Herramientas de administración del sistema

### 🧹 Liberador de espacio en disco (cleanmgr.exe)

Herramienta que permite liberar espacio eliminando archivos innecesarios como:

* archivos temporales
* caché de actualizaciones
* contenido de la papelera de reciclaje

---

### 💽 Optimización de unidades (dfrgui.exe)

Herramienta utilizada para optimizar el almacenamiento.

En discos **HDD** realiza **desfragmentación**.

En discos **SSD** ejecuta el comando **TRIM**, que optimiza la gestión de la memoria sin realizar desfragmentación.

---

### 📊 Información del sistema (msinfo32.exe)

Herramienta que muestra información detallada sobre el sistema, como:

* componentes de hardware
* recursos del sistema
* controladores
* entorno de software

---

# 🧠 Resumen de conceptos clave

Explorador de Windows → herramienta para gestionar archivos y carpetas.

Windows + E → atajo para abrir el Explorador.

Archivo → unidad de almacenamiento con nombre y extensión.

Carpeta → contenedor para organizar archivos.

F2 → renombrar archivo o carpeta.

Supr → envía archivo a la papelera.

Shift + Supr → eliminación permanente.

Este equipo → muestra unidades y recursos del ordenador.

Acceso rápido → muestra archivos recientes y carpetas frecuentes.

Asterisco (*) → sustituye varios caracteres en búsquedas.

Interrogación (?) → sustituye un único carácter.
