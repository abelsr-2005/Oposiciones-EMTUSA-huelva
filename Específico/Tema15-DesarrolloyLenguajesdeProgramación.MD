# 💻 Tema 15 — Desarrollo y Lenguajes de Programación

## 📚 Introducción

El desarrollo de software es el proceso mediante el cual se diseñan, crean, prueban y mantienen aplicaciones informáticas. En entornos empresariales modernos, el desarrollo se apoya en plataformas y herramientas que facilitan la creación de aplicaciones robustas, seguras y escalables.

Uno de los ecosistemas más utilizados en entornos corporativos es **.NET**, desarrollado por Microsoft. Este entorno permite crear aplicaciones de escritorio, aplicaciones web, servicios y soluciones en la nube.

Para desarrollar software dentro de este ecosistema se utilizan herramientas como **Visual Studio**, lenguajes como **C#, C++, Visual Basic, JavaScript o TypeScript**, y tecnologías web como **HTML y CSS**.

---

# 🧰 1. Entorno Visual Studio y Ecosistema .NET

## 🖥️ Visual Studio como entorno de desarrollo (IDE)

**Visual Studio** es un **IDE (Integrated Development Environment)** que proporciona todas las herramientas necesarias para desarrollar software profesional.

Entre las funcionalidades principales se encuentran:

* editor avanzado de código
* autocompletado inteligente (IntelliSense)
* depuración paso a paso
* compilación automática
* gestión de proyectos y soluciones
* integración con sistemas de control de versiones

Visual Studio permite crear diferentes tipos de proyectos:

* aplicaciones de escritorio (Windows Forms, WPF)
* aplicaciones web (ASP.NET)
* APIs REST
* servicios de backend
* aplicaciones móviles (Xamarin / .NET MAUI)

En entornos corporativos también se utiliza junto con **Azure DevOps o Git** para gestión de código y trabajo colaborativo.

---

## 🌐 Ecosistema .NET

El **ecosistema .NET** es una plataforma de desarrollo que incluye varios componentes fundamentales.

### Runtime (.NET Runtime)

El **runtime** es el entorno donde se ejecutan las aplicaciones.

En .NET destaca el **CLR (Common Language Runtime)**, que se encarga de:

* ejecutar el código
* gestionar la memoria
* controlar excepciones
* aplicar seguridad
* gestionar el recolector de basura (Garbage Collector)

El **Garbage Collector** libera automáticamente memoria que ya no se utiliza, evitando fugas de memoria.

---

### Bibliotecas de clases (.NET Class Library)

.NET incluye una gran colección de bibliotecas que proporcionan funcionalidades reutilizables:

Ejemplos de funciones disponibles:

* acceso a archivos
* comunicación en red
* acceso a bases de datos
* criptografía
* interfaces gráficas

Esto permite a los desarrolladores crear aplicaciones complejas sin tener que programar todo desde cero.

---

### Compilación y ejecución

El código escrito en lenguajes como **C#** se compila inicialmente a un lenguaje intermedio llamado:

**IL (Intermediate Language)**

Posteriormente el runtime lo convierte a código máquina mediante **JIT (Just In Time Compilation)**.

Este proceso permite que el mismo programa pueda ejecutarse en diferentes sistemas compatibles con .NET.

---

## 🔤 Lenguajes soportados

Visual Studio permite trabajar con múltiples lenguajes.

Los más habituales dentro del ecosistema .NET son:

### C#

Es el lenguaje principal de .NET.

Características:

* orientado a objetos
* tipado fuerte
* muy utilizado en desarrollo empresarial

Se utiliza para:

* aplicaciones web
* APIs
* servicios backend
* aplicaciones de escritorio

---

### C++

Lenguaje de bajo nivel con alto rendimiento.

Se utiliza principalmente en:

* desarrollo de sistemas
* aplicaciones de alto rendimiento
* componentes críticos

---

### Visual Basic (.NET)

Lenguaje orientado a objetos más sencillo que C#.

Se utiliza principalmente en:

* aplicaciones empresariales heredadas
* mantenimiento de software existente

---

### Python

Lenguaje interpretado muy utilizado para:

* automatización
* scripts
* análisis de datos

---

### JavaScript

Lenguaje fundamental del desarrollo web.

Se ejecuta directamente en el navegador.

Se utiliza para:

* interacción en páginas web
* aplicaciones web dinámicas

---

### TypeScript

**TypeScript** es un superconjunto de JavaScript que añade **tipado estático**.

Ventajas:

* mejor detección de errores
* mayor mantenibilidad
* desarrollo de aplicaciones grandes

El código TypeScript se **compila a JavaScript** antes de ejecutarse.

---

## 📦 Gestión de librerías con NuGet

Las aplicaciones modernas utilizan bibliotecas externas para añadir funcionalidades.

En el ecosistema .NET estas bibliotecas se gestionan mediante **NuGet**.

NuGet permite:

* instalar paquetes externos
* actualizar dependencias
* reutilizar componentes

Ejemplo de bibliotecas comunes:

* bibliotecas para acceso a bases de datos
* bibliotecas de seguridad
* bibliotecas de generación de APIs

Esto acelera el desarrollo y evita reinventar soluciones existentes.

---

# 🏗️ 2. Arquitectura y Estructuras de Programación

## 🧩 Arquitectura Cliente-Servidor

El modelo **cliente-servidor** es uno de los más utilizados en aplicaciones modernas.

En este modelo existen dos componentes principales:

| Componente | Función                                       |
| ---------- | --------------------------------------------- |
| Cliente    | interfaz que solicita información             |
| Servidor   | procesa las solicitudes y devuelve resultados |

Ejemplo típico:

1. Un navegador (cliente) solicita una página web
2. El servidor procesa la petición
3. El servidor envía la respuesta al cliente

Este modelo se utiliza en:

* aplicaciones web
* sistemas distribuidos
* servicios en la nube

---

## 🧱 Arquitecturas comunes de software

En aplicaciones empresariales suele utilizarse arquitectura **por capas**.

Capas habituales:

| Capa              | Función                         |
| ----------------- | ------------------------------- |
| Presentación      | interfaz de usuario             |
| Lógica de negocio | procesamiento de datos          |
| Acceso a datos    | comunicación con bases de datos |

Esta separación facilita:

* mantenimiento del software
* escalabilidad
* reutilización de código

---

## 🔁 Estructuras de control

Las estructuras de programación permiten controlar el flujo de ejecución del programa.

### Condicionales

Permiten ejecutar código dependiendo de una condición.

Ejemplo en C#:

```csharp
if (edad >= 18)
{
    Console.WriteLine("Mayor de edad");
}
```

También se utilizan estructuras como:

* if / else
* switch

---

### Bucles

Permiten repetir instrucciones múltiples veces.

Ejemplo:

```csharp
for(int i=0; i<10; i++)
{
    Console.WriteLine(i);
}
```

Tipos comunes de bucles:

* for
* while
* foreach

---

## 🔐 Tipado en lenguajes de programación

El tipado define cómo se gestionan los tipos de datos.

| Tipo de lenguaje | Característica                       |
| ---------------- | ------------------------------------ |
| Tipado fuerte    | detecta errores en compilación       |
| Tipado dinámico  | los tipos se determinan en ejecución |

Ejemplos:

* **C# → tipado fuerte**
* **JavaScript → tipado dinámico**

El tipado fuerte ayuda a detectar errores antes de ejecutar el programa.

---

# 🌐 3. Desarrollo Web: HTML y CSS

El desarrollo web suele dividirse en dos grandes áreas.

| Parte    | Función                      |
| -------- | ---------------------------- |
| Frontend | interfaz visible del usuario |
| Backend  | lógica del servidor          |

HTML y CSS forman la base del **frontend**.

---

## 🧾 HTML (HyperText Markup Language)

HTML es el lenguaje de marcado utilizado para definir la estructura de una página web.

Permite crear elementos como:

* títulos
* párrafos
* enlaces
* imágenes
* formularios

Ejemplo básico:

```html
<h1>Hola mundo</h1>
<p>Primer párrafo de una página web.</p>
```

Los documentos HTML están formados por **etiquetas (tags)** que estructuran el contenido.

---

## 🎨 CSS (Cascading Style Sheets)

CSS define la apariencia visual de una página web.

Permite controlar:

* colores
* fuentes
* tamaños
* disposición de elementos

Ejemplo:

```css
h1 {
  color: blue;
}
```

CSS permite separar completamente el diseño del contenido.

---

## 📱 Diseño responsivo

El diseño responsivo permite que una página web se adapte automáticamente a distintos tamaños de pantalla.

Esto se consigue mediante:

* **layouts flexibles**
* **media queries**
* frameworks como Bootstrap

Gracias a esto una web puede visualizarse correctamente en:

* móviles
* tablets
* ordenadores

---

# ♿ 4. Accesibilidad y Compatibilidad

Las aplicaciones web profesionales deben garantizar accesibilidad para todos los usuarios.

## ♿ Accesibilidad web

La accesibilidad permite que personas con discapacidades puedan utilizar aplicaciones web.

Ejemplos de buenas prácticas:

* uso de atributos **ALT en imágenes**
* navegación mediante teclado
* contraste adecuado de colores

Estas prácticas están definidas por estándares **WCAG (Web Content Accessibility Guidelines)**.

---

## 🌍 Compatibilidad entre navegadores

Las aplicaciones web deben funcionar correctamente en distintos navegadores.

Navegadores más utilizados:

* Chrome
* Edge
* Firefox
* Safari

Para garantizar compatibilidad se siguen estándares del **W3C (World Wide Web Consortium)**.

---

## 🔧 Herramientas de desarrollo del navegador

Los navegadores incluyen herramientas de desarrollo accesibles con:

```
F12
```

Estas herramientas permiten:

* inspeccionar el DOM
* analizar tráfico de red
* depurar JavaScript
* revisar rendimiento

Son fundamentales para diagnosticar problemas en aplicaciones web.
