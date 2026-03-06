# Tema 12 — Servicios de Internet y Protocolos Avanzados

### Protocolos de Internet, arquitectura cliente-servidor y seguridad en comunicaciones

> Apuntes sobre el modelo TCP/IP, protocolos web, transferencia de archivos, correo electrónico y herramientas de diagnóstico.

---

# 1. Modelo TCP/IP

El **modelo TCP/IP** es el conjunto de protocolos que permite la comunicación en **Internet y redes locales**.

Se organiza en **cuatro capas funcionales**.

| Capa         | Función                                     |
| ------------ | ------------------------------------------- |
| Aplicación   | Protocolos utilizados por el usuario        |
| Transporte   | Transferencia de datos entre dispositivos   |
| Internet     | Direccionamiento y enrutamiento de paquetes |
| Acceso a red | Interfaz con el hardware de red             |

---

## Capa de Aplicación

En esta capa operan los protocolos que utilizan directamente las aplicaciones.

Ejemplos:

* HTTP
* FTP
* SMTP
* DNS

---

## Capa de Transporte

Encargada de la transferencia de datos entre dispositivos.

Protocolos principales:

### TCP (Transmission Control Protocol)

Características:

* orientado a conexión
* fiable
* control de errores
* control de flujo

---

### UDP (User Datagram Protocol)

Características:

* no orientado a conexión
* más rápido
* menor control de errores

Se utiliza en servicios donde la velocidad es prioritaria.

---

## Capa de Internet

Encargada del **direccionamiento y encaminamiento de paquetes**.

Protocolo principal:

* **IP (Internet Protocol)**

---

## Capa de Acceso a Red

Gestiona la comunicación con el **hardware físico de red**.

Incluye tecnologías como:

* Ethernet
* WiFi

---

# 2. Protocolos Web: HTTP y HTTPS

Los protocolos web permiten la transferencia de información entre navegadores y servidores web.

---

## HTTP (HyperText Transfer Protocol)

Características:

* protocolo de transferencia de hipertexto
* comunicación **no cifrada**

Puerto utilizado:

```
TCP 80
```

---

## HTTPS (HTTP Secure)

Versión segura de HTTP.

Características:

* utiliza **SSL/TLS** para cifrar la comunicación
* protege la confidencialidad e integridad de los datos

Puerto utilizado:

```
TCP 443
```

---

### Certificados SSL/TLS

Los certificados digitales permiten verificar la identidad de un servidor.

Garantizan:

* confidencialidad
* integridad
* autenticidad

---

# 3. Transferencia de Archivos: FTP y SFTP

Estos protocolos permiten transferir archivos entre sistemas.

---

## FTP (File Transfer Protocol)

Características:

* utiliza **dos puertos**
* comunicación **no cifrada**

Puertos utilizados:

```
21 → canal de control
20 → canal de datos
```

---

## SFTP (SSH File Transfer Protocol)

Protocolo seguro de transferencia de archivos.

Características:

* basado en **SSH**
* cifra comandos y datos

Puerto utilizado:

```
TCP 22
```

---

# 4. Protocolos de Correo Electrónico

Los sistemas de correo electrónico utilizan diferentes protocolos para envío y recepción de mensajes.

---

## SMTP (Simple Mail Transfer Protocol)

Utilizado para **enviar correos electrónicos** entre servidores.

Puertos:

```
25 → estándar
587 → autenticación / TLS
```

---

## POP3 (Post Office Protocol)

Permite descargar los mensajes desde el servidor al cliente local.

Puertos:

```
110 → estándar
995 → SSL
```

Características:

* los correos suelen eliminarse del servidor tras descargarse

---

## IMAP (Internet Message Access Protocol)

Permite sincronizar el correo en múltiples dispositivos.

Puertos:

```
143 → estándar
993 → SSL
```

Características:

* los mensajes permanecen en el servidor
* sincronización entre dispositivos

---

# 5. Arquitectura Cliente-Servidor y Navegadores

La mayoría de servicios de Internet utilizan el modelo **cliente-servidor**.

---

## Modelo Cliente-Servidor

Funcionamiento:

* el **cliente** realiza una petición
* el **servidor** procesa la solicitud
* el servidor devuelve una respuesta

Ejemplos de servidores web:

* Apache
* IIS
* Nginx

---

## Herramientas de Desarrollo del Navegador

Los navegadores incluyen herramientas de desarrollo accesibles con:

```
F12
```

Permiten:

* inspeccionar el DOM
* depurar JavaScript
* analizar tráfico de red
* revisar certificados de seguridad

---

## Gestión de Seguridad en Navegadores

Incluye diferentes mecanismos de seguridad:

* gestión de **cookies**
* **Content Security Policy (CSP)**
* **HSTS** para forzar conexiones HTTPS

---

# 🛠️ Herramientas de Administración Técnica y Comandos

### Verificación de conectividad y certificados

```bash
# Ver cabeceras HTTP de un servidor
curl -I https://www.google.es

# Inspeccionar certificado SSL/TLS
openssl s_client -connect servidor:443

# Ver conexiones activas en puerto HTTPS (Windows)
netstat -an | findstr ":443"
```

---

# 💡 Conceptos Clave para el Examen

### Diferencia FTP vs SFTP

| Protocolo | Seguridad            | Puerto  |
| --------- | -------------------- | ------- |
| FTP       | No cifrado           | 21 / 20 |
| SFTP      | Cifrado mediante SSH | 22      |

---

### HTTP es un protocolo sin estado

HTTP es **stateless**, lo que significa que cada petición es independiente.

Para mantener sesiones se utilizan:

* cookies
* tokens de sesión

---

### Handshake TCP

Proceso de **tres pasos** para establecer una conexión TCP.

1. SYN
2. SYN-ACK
3. ACK
