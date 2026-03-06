# TEMA 3: El explorador de Windows y Herramientas del sistema

> **Objetivo del examen:** Dominar el Explorador de Windows, la gestión de carpetas y archivos, las operaciones de búsqueda, las herramientas "Este equipo" y "Acceso Rápido", y los Accesorios y Herramientas del sistema.

## 3.1. El Explorador de Windows (File Explorer)
* **Definición:** Herramienta principal de gestión de archivos de Windows que proporciona la interfaz gráfica para interactuar con los sistemas de archivos.
* **Atajo crítico:** Se invoca nativamente con `Windows + E`.
* **Estructura gráfica:** Cinta de opciones (Ribbon), Panel de navegación izquierdo, Barra de direcciones, Caja de búsqueda y Panel de detalles/vista previa.

### ⚠️ Alerta de Trampa (Comportamiento por defecto)
En Windows 10/11, la ejecución del atajo `Windows + E` no abre "Este equipo" por defecto. El comportamiento predeterminado, y la respuesta correcta en un test oficial, es que abre la vista de **"Acceso rápido"**.

## 3.2. Gestión de carpetas y archivos
* **Archivos:** Unidades lógicas de almacenamiento. Identificados por nombre y extensión (ej. `.sys`, `.docx`), lo que define la asociación lógica de ejecución del sistema operativo.
* **Carpetas (Directorios):** Contenedores lógicos para la estructuración y jerarquización.
* **Ruta (Path):** Dirección absoluta o relativa de un objeto dentro del árbol de directorios.

### ⚠️ Alerta de Trampa (Operaciones de borrado y renombrado)
* **Renombrar:** El atajo nativo y estándar para editar el nombre de un elemento seleccionado es **F2**.
* **Borrado Lógico vs Físico:** Pulsar la tecla `Supr` envía el elemento a la Papelera de reciclaje (borrado lógico, los datos siguen en disco). Pulsar **`Shift + Supr`** puentea la Papelera y libera los clústeres en el sistema de archivos (borrado definitivo e inmediato).

## 3.3. Herramientas "Este equipo" y "Acceso Rápido"
* **Este equipo:** Interfaz que reemplaza al antiguo "Mi PC". Enumera las unidades de almacenamiento físico, particiones lógicas, unidades ópticas y recursos de red mapeados, además de las carpetas de perfil del usuario.
* **Acceso Rápido:** Reemplaza a la antigua sección de "Favoritos". Ancla carpetas fijas y recopila dinámicamente el historial de archivos abiertos recientemente y los directorios frecuentados.

## 3.4. Operaciones de búsqueda
La caja de búsqueda del explorador soporta sintaxis avanzada mediante **caracteres comodín (Wildcards)**. Su dominio es vital para las preguntas prácticas de test:
* **Asterisco (*):** Sustituye cadenas de texto de cualquier longitud (incluyendo cero caracteres). Ej: `*.log` filtra y muestra cualquier archivo con esa extensión exacta.
* **Interrogación (?):** Sustituye **exclusiva y estrictamente a un único carácter**. Ej: `red?.txt` encontrará "red1.txt" o "redA.txt", pero ignorará "redes.txt".

## 3.5. Accesorios y Herramientas del sistema
* **Accesorios básicos:** Bloc de notas (editor de texto plano, sin formato), WordPad (editor de texto enriquecido básico) y la herramienta Recortes (Snipping Tool).
* **Herramientas de Administración:**
    * **cleanmgr.exe (Liberador de espacio en disco):** Purga archivos temporales, cachés de actualizaciones y vacía la papelera.
    * **dfrgui.exe (Optimización de unidades):** En discos magnéticos (HDD) desfragmenta clústeres contiguos. En discos de estado sólido (SSD) no desfragmenta, sino que ejecuta el comando TRIM para optimizar las celdas de memoria.
    * **msinfo32.exe (Información del sistema):** Interfaz gráfica avanzada para auditar componentes de hardware, IRQs y entorno de software.
