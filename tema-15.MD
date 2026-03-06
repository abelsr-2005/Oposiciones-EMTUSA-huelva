# Tema 15 — Desarrollo y Lenguajes de Programación

### Entorno .NET, desarrollo web y fundamentos de programación

> Apuntes sobre el entorno Visual Studio, arquitectura de software, desarrollo web y principios de accesibilidad.

---

# 1. Entorno Visual Studio y Ecosistema .NET

**Visual Studio** es uno de los entornos de desarrollo integrados (**IDE**) más utilizados para crear aplicaciones profesionales en el ecosistema Microsoft.

Permite desarrollar aplicaciones de:

* escritorio
* web
* servicios
* aplicaciones móviles

---

## Multilenguaje

Visual Studio permite trabajar con múltiples lenguajes de programación.

Lenguajes soportados:

* **C#**
* **C++**
* **Visual Basic**
* **Python**
* **JavaScript**
* **TypeScript**

Esto facilita el desarrollo de diferentes tipos de aplicaciones dentro del mismo entorno.

---

## Arquitectura .NET

El ecosistema **.NET** proporciona:

* un entorno de ejecución (**Runtime**)
* bibliotecas de clases
* herramientas de desarrollo

Esto permite crear aplicaciones:

* de escritorio
* web
* móviles
* servicios en la nube

---

## Gestión de librerías

Las aplicaciones pueden ampliarse mediante bibliotecas externas.

Estas bibliotecas permiten:

* reutilizar código
* añadir funcionalidades
* mantener el software actualizado

En .NET normalmente se gestionan mediante sistemas de paquetes como **NuGet**.

---

# 2. Arquitectura y Estructuras de Programación

El desarrollo de software suele organizarse mediante **modelos de arquitectura** que separan responsabilidades.

---

## Arquitectura Cliente-Servidor

En este modelo existen dos componentes principales:

| Componente | Función                             |
| ---------- | ----------------------------------- |
| Cliente    | Interfaz que realiza peticiones     |
| Servidor   | Procesa datos y devuelve respuestas |

Este modelo se utiliza ampliamente en:

* aplicaciones web
* sistemas distribuidos
* servicios en la nube

---

## Estructuras de programación

Las estructuras de programación controlan el flujo de ejecución del programa.

### Control de flujo

Permite tomar decisiones dentro del programa.

Ejemplos:

```
if
switch
```

---

### Bucles

Permiten repetir instrucciones múltiples veces.

Ejemplos:

```
for
while
```

---

## Tipado en lenguajes

Los lenguajes de programación pueden diferenciarse por su sistema de tipos.

| Lenguaje   | Tipo de tipado  |
| ---------- | --------------- |
| C#         | Tipado fuerte   |
| JavaScript | Tipado dinámico |

En un lenguaje de **tipado fuerte**, los errores de tipo se detectan en compilación.

---

## TypeScript

**TypeScript** es un superconjunto de JavaScript.

Características:

* añade **tipado estático**
* mejora la detección de errores
* facilita el desarrollo de aplicaciones web complejas

El código TypeScript se **compila a JavaScript** para ejecutarse en el navegador.

---

# 3. Desarrollo Web: HTML y CSS

El desarrollo web se divide normalmente en dos partes:

* **Frontend** → interfaz visible para el usuario
* **Backend** → lógica del servidor

HTML y CSS forman la base del **frontend**.

---

## HTML (HyperText Markup Language)

HTML es el lenguaje de marcado que define la **estructura de una página web**.

Permite crear elementos como:

* títulos
* párrafos
* imágenes
* enlaces
* tablas

Ejemplo básico:

```html
<h1>Hola mundo</h1>
<p>Primer párrafo de una página web.</p>
```

---

## CSS (Cascading Style Sheets)

CSS define el **aspecto visual** de una página web.

Permite configurar:

* colores
* fuentes
* tamaños
* distribución de elementos

Ejemplo:

```css
h1 {
  color: blue;
}
```

---

## Separación de conceptos

Una buena práctica en desarrollo web consiste en separar:

| Componente | Función                  |
| ---------- | ------------------------ |
| HTML       | estructura del contenido |
| CSS        | diseño visual            |

Esto mejora el mantenimiento del código.

---

# 4. Accesibilidad y Compatibilidad

El desarrollo web profesional debe garantizar que las aplicaciones sean **utilizables por cualquier persona y en cualquier dispositivo**.

---

## Accesibilidad (WAI-ARIA)

Las prácticas de accesibilidad permiten que personas con discapacidades puedan navegar por una página web.

Ejemplo:

* uso de **atributos ALT en imágenes**

Esto permite que los **lectores de pantalla** describan el contenido visual.

---

## Compatibilidad entre navegadores

Las páginas web deben funcionar correctamente en diferentes navegadores.

Navegadores más comunes:

* Chrome
* Edge
* Firefox
* Safari

Para garantizar la compatibilidad se utilizan **estándares definidos por el W3C**.

---

## Diseño responsivo

El **diseño responsivo** permite que la interfaz se adapte automáticamente al tamaño de la pantalla.

Dispositivos soportados:

* teléfonos móviles
* tablets
* ordenadores

Esto se consigue principalmente mediante:

* CSS flexible
* media queries
