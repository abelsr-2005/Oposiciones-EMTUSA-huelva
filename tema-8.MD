# TEMA 8: Internet, Navegadores y Redes sociales

> **Objetivo del examen:** Dominar los conceptos fundamentales de Internet, el uso y configuración de navegadores, la seguridad en la navegación y el ecosistema de las redes sociales desde una perspectiva profesional y técnica.

## 8.1. Conceptos fundamentales de Internet
* **Definición:** Red global descentralizada de redes interconectadas que utilizan la familia de protocolos TCP/IP.
* **Protocolos y servicios críticos (Visión IT):**
    * **HTTP / HTTPS:** Protocolos de transferencia de hipertexto. La versión segura (HTTPS) utiliza cifrado TLS/SSL sobre el puerto 443.
    * **DNS (Domain Name System):** Servicio de resolución de nombres que traduce FQDN (nombres de dominio) en direcciones IP.
    * **URL (Uniform Resource Locator):** Sintaxis estándar para identificar recursos. Estructura: `protocolo://dominio:puerto/ruta?parámetros`.
    * **WWW (World Wide Web):** Servicio de consulta de hipertexto que funciona sobre Internet (no son sinónimos).

## 8.2. Navegadores: Microsoft Edge y Google Chrome
* **Motor de renderizado:** Ambos navegadores comparten actualmente la base **Chromium**, lo que estandariza la interpretación de HTML5, CSS3 y motores de JavaScript (V8).
* **Gestión de datos locales:**
    * **Caché:** Almacenamiento de elementos estáticos (imágenes, scripts) para optimizar el tiempo de carga (ancho de banda).
    * **Cookies:** Archivos de datos enviados por el servidor para mantenimiento de sesiones, personalización y seguimiento.
    * **Historial:** Registro cronológico de URLs visitadas en el dispositivo local.
* **Modo Incógnito / InPrivate:** Evita el almacenamiento local de historial, cookies y datos de formularios, pero no garantiza el anonimato ante el ISP o administradores de red corporativa.

## 8.3. Seguridad y Certificados Digitales
* **Certificado SSL/TLS:** Documento digital que valida la identidad de un servidor y permite el cifrado de la comunicación.
* **Entidad de Certificación (CA):** Tercero de confianza (como la FNMT) que emite y revoca certificados.
* **Firma Electrónica:** Mecanismo criptográfico que garantiza la integridad del mensaje, la autenticidad del emisor y el no repudio.

## 8.4. Redes Sociales y Seguridad
* **Plataformas Profesionales:**
    * **X (Twitter):** Comunicación institucional inmediata.
    * **LinkedIn:** Networking y entorno estrictamente profesional.
    * **Instagram/Facebook:** Canales visuales y de comunidad.
* **Riesgos de Seguridad:**
    * **Phishing:** Suplantación de identidad para robo de credenciales.
    * **Ingeniería Social:** Manipulación de usuarios para obtener información sensible.
    * **Malware:** Distribución de código malicioso mediante enlaces acortados o perfiles falsos.

### ⚠️ Alerta de Trampa (Navegación y Privacidad)
Pregunta recurrente en test: ¿Qué ocurre con las descargas en modo incógnito? 
**Respuesta:** El historial de navegación se borra al cerrar la ventana, pero los archivos descargados manualmente y los marcadores creados por el usuario **permanecen en el equipo**.
