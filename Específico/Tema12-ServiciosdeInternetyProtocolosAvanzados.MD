# 🌍 Tema 12 — Servicios de Internet y Protocolos Avanzados

## 📚 Introducción

Los servicios de Internet se basan en un conjunto de **protocolos de comunicación estandarizados** que permiten el intercambio de información entre dispositivos conectados a una red. Estos protocolos definen cómo se envían, reciben y procesan los datos entre clientes y servidores.

La mayoría de los servicios de Internet siguen una **arquitectura cliente-servidor**, donde un cliente (por ejemplo, un navegador web) solicita información a un servidor, que procesa la petición y devuelve una respuesta.

Entre los protocolos más importantes utilizados en Internet se encuentran **TCP/IP, HTTP/HTTPS, FTP/SFTP y los protocolos de correo electrónico como SMTP, POP3 e IMAP**.

---

# 🧩 1. Modelo TCP/IP

El **modelo TCP/IP** es el modelo de referencia utilizado en Internet para describir cómo se organizan los protocolos de red. Define cómo los datos se encapsulan, transmiten y reciben entre dispositivos conectados.

Este modelo está compuesto por **cuatro capas principales**, cada una con funciones específicas.

| Capa         | Función                                                |
| ------------ | ------------------------------------------------------ |
| Aplicación   | Protocolos utilizados por las aplicaciones del usuario |
| Transporte   | Comunicación extremo a extremo entre dispositivos      |
| Internet     | Direccionamiento y enrutamiento de paquetes            |
| Acceso a red | Comunicación con el hardware de red                    |

Este modelo se basa en el principio de **encapsulación**, donde cada capa añade información al paquete de datos para permitir su correcta transmisión.

---

## 🧑‍💻 Capa de Aplicación

La **capa de aplicación** es la más cercana al usuario final y proporciona servicios de red a las aplicaciones.

Algunos de los protocolos más importantes de esta capa son:

* **HTTP / HTTPS** → navegación web
* **FTP / SFTP** → transferencia de archivos
* **SMTP / POP3 / IMAP** → correo electrónico
* **DNS** → resolución de nombres de dominio

Las aplicaciones como navegadores web, clientes de correo o herramientas de transferencia de archivos utilizan estos protocolos para comunicarse con servidores remotos.

---

## 🚚 Capa de Transporte

La **capa de transporte** se encarga de garantizar la comunicación entre el origen y el destino de los datos.

Los dos protocolos principales son **TCP y UDP**.

### TCP (Transmission Control Protocol)

TCP es un protocolo **orientado a conexión**, diseñado para garantizar la entrega fiable de datos.

Características principales:

* Establecimiento de conexión previa
* Control de errores
* Control de flujo
* Confirmación de recepción de paquetes

TCP se utiliza en servicios donde la fiabilidad es crítica, como:

* navegación web
* correo electrónico
* transferencia de archivos

### UDP (User Datagram Protocol)

UDP es un protocolo **no orientado a conexión**, más simple y rápido que TCP.

Características:

* No establece conexión previa
* No garantiza la entrega de paquetes
* Menor sobrecarga de control

Se utiliza en aplicaciones donde la **velocidad es prioritaria**, como:

* streaming
* VoIP
* videojuegos en red

---

## 🌐 Capa de Internet

La **capa de Internet** se encarga del direccionamiento y del encaminamiento de los paquetes entre redes diferentes.

El protocolo principal de esta capa es:

* **IP (Internet Protocol)**

Las funciones de esta capa incluyen:

* asignar direcciones IP a los dispositivos
* fragmentar paquetes si es necesario
* determinar la ruta que seguirá el tráfico

Los routers operan principalmente en esta capa.

---

## 🔌 Capa de Acceso a Red

La capa de **acceso a red** gestiona la transmisión de datos entre el sistema y el medio físico de la red.

Incluye tecnologías como:

* **Ethernet**
* **WiFi**
* **ARP**

Esta capa se corresponde aproximadamente con las capas **física y de enlace de datos del modelo OSI**.

---

# 🌐 2. Protocolos Web: HTTP y HTTPS

Los protocolos web permiten la comunicación entre **navegadores web y servidores web**.

Cuando un usuario introduce una dirección en el navegador, este envía una solicitud al servidor utilizando el protocolo HTTP o HTTPS.

---

## 📄 HTTP (HyperText Transfer Protocol)

HTTP es el protocolo utilizado para transferir documentos web como páginas HTML, imágenes o archivos.

Características:

* Protocolo **sin estado (stateless)**
* Basado en el modelo cliente-servidor
* Comunicación no cifrada

Puerto utilizado:

```
TCP 80
```

Al ser un protocolo sin estado, cada petición se procesa de forma independiente.

---

## 🔒 HTTPS (HTTP Secure)

HTTPS es la versión segura de HTTP.

Características:

* Utiliza cifrado mediante **SSL/TLS**
* Protege la confidencialidad de los datos
* Garantiza la integridad de la información

Puerto utilizado:

```
TCP 443
```

Actualmente, la mayoría de los servicios web utilizan HTTPS para evitar ataques como **interceptación de tráfico (man-in-the-middle)**.

---

## 📜 Certificados SSL/TLS

Los certificados digitales permiten verificar la identidad de un servidor web.

Garantizan:

* **Confidencialidad** → datos cifrados
* **Integridad** → los datos no se modifican
* **Autenticidad** → el servidor es quien dice ser

Los certificados son emitidos por **Autoridades de Certificación (CA)**.

---

# 📁 3. Transferencia de Archivos: FTP y SFTP

Los protocolos de transferencia de archivos permiten enviar y recibir archivos entre sistemas remotos.

---

## 📂 FTP (File Transfer Protocol)

FTP es un protocolo tradicional utilizado para transferir archivos entre cliente y servidor.

Características:

* Comunicación **no cifrada**
* Utiliza dos canales de comunicación

Puertos:

```
21 → canal de control
20 → canal de datos
```

Debido a la falta de cifrado, FTP se considera inseguro para redes públicas.

---

## 🔐 SFTP (SSH File Transfer Protocol)

SFTP es una alternativa segura para la transferencia de archivos.

Características:

* Basado en el protocolo **SSH**
* Comunicación cifrada
* Utiliza un único canal de comunicación

Puerto utilizado:

```
TCP 22
```

SFTP se utiliza ampliamente en entornos corporativos para transferencias seguras.

---

# 📧 4. Protocolos de Correo Electrónico

Los sistemas de correo electrónico utilizan varios protocolos para enviar y recibir mensajes.

---

## ✉️ SMTP (Simple Mail Transfer Protocol)

SMTP es el protocolo utilizado para **enviar correos electrónicos** entre servidores de correo.

Puertos habituales:

```
25 → envío estándar
587 → envío autenticado con TLS
```

---

## 📥 POP3 (Post Office Protocol v3)

POP3 permite descargar los mensajes desde el servidor al cliente.

Puertos:

```
110 → estándar
995 → POP3 seguro (SSL)
```

Características:

* descarga local del correo
* normalmente elimina el mensaje del servidor

---

## 📬 IMAP (Internet Message Access Protocol)

IMAP permite acceder al correo directamente desde el servidor.

Puertos:

```
143 → estándar
993 → IMAP seguro (SSL)
```

Características:

* sincronización entre dispositivos
* los correos permanecen almacenados en el servidor

---

# 🖥️ 5. Arquitectura Cliente‑Servidor y Navegadores

La mayoría de servicios de Internet utilizan el modelo **cliente-servidor**.

## 🔄 Modelo Cliente‑Servidor

Funcionamiento general:

1. El **cliente** envía una petición.
2. El **servidor** procesa la solicitud.
3. El servidor devuelve una **respuesta**.

Ejemplos de servidores web populares:

* **Apache HTTP Server**
* **Microsoft IIS**
* **Nginx**

Este modelo permite centralizar los servicios y facilitar la administración de los recursos.

---

## 🧰 Herramientas de Desarrollo del Navegador

Los navegadores modernos incluyen herramientas de desarrollo accesibles mediante:

```
F12
```

Estas herramientas permiten:

* inspeccionar el **DOM**
* analizar tráfico de red
* depurar **JavaScript**
* revisar cookies y almacenamiento local
* comprobar certificados y seguridad

---

## 🔐 Seguridad en Navegadores

Los navegadores implementan múltiples mecanismos de seguridad:

* gestión de **cookies**
* **Content Security Policy (CSP)**
* **HSTS (HTTP Strict Transport Security)**
* aislamiento de procesos

Estos mecanismos ayudan a proteger al usuario frente a ataques web.

---

# 🛠️ Herramientas de Administración y Diagnóstico

Las herramientas de diagnóstico permiten analizar el comportamiento de los servicios web y verificar la conectividad.

```bash
# Ver cabeceras HTTP de un servidor
curl -I https://www.google.es

# Inspeccionar certificado SSL/TLS
openssl s_client -connect servidor:443

# Ver conexiones activas en puerto HTTPS (Windows)
netstat -an | findstr ":443"
```

Estas herramientas son utilizadas por administradores de sistemas para verificar configuraciones, detectar errores y comprobar el funcionamiento de servicios de red.

---

# 🧠 Conceptos Clave para Examen

## Diferencia FTP vs SFTP

| Protocolo | Seguridad            | Puerto  |
| --------- | -------------------- | ------- |
| FTP       | Sin cifrado          | 21 / 20 |
| SFTP      | Cifrado mediante SSH | 22      |

## HTTP es un protocolo sin estado

Cada petición HTTP es independiente.

Para mantener sesiones se utilizan mecanismos como:

* cookies
* tokens de sesión
* almacenamiento local

## Handshake TCP

El establecimiento de conexión TCP se realiza mediante el **three‑way handshake**:

1. **SYN** → el cliente solicita la conexión
2. **SYN‑ACK** → el servidor responde
3. **ACK** → el cliente confirma

Este proceso garantiza que ambos extremos están preparados para iniciar la comunicación.
