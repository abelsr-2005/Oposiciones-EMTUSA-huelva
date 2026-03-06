# Tema 11 — Red Local (LAN)

### Fundamentos de redes locales, direccionamiento y administración

> Apuntes sobre topologías de red, direccionamiento IP, VLAN y herramientas de diagnóstico de redes LAN.

---

## 📑 Índice

* [1. Topologías de red](#1-topologías-de-red)
* [2. Direccionamiento IPv4 e IPv6](#2-direccionamiento-ipv4-e-ipv6)
* [3. VLAN](#3-vlan-virtual-local-area-network)
* [4. DHCP](#4-dhcp-dynamic-host-configuration-protocol)
* [5. Administración y diagnóstico de red](#5-administración-y-diagnóstico-de-red)

---

## 1. Topologías de Red

La **topología de red** define la forma en que los dispositivos están conectados dentro de una red, tanto a nivel **físico** como **lógico**.

---

### Topología en Estrella

Es la topología más utilizada en redes LAN modernas.

Características:

* todos los dispositivos se conectan a un **dispositivo central** (normalmente un switch)
* si falla un cable, solo afecta al nodo conectado
* facilita la administración de la red

---

### Topología en Árbol

Es una extensión de la topología en estrella.

Características:

* los switches se conectan de forma **jerárquica**
* permite ampliar la red fácilmente
* muy común en redes empresariales

---

### Topología en Malla

En una topología de malla cada nodo está conectado con varios nodos de la red.

Características:

* **alta redundancia**
* mayor tolerancia a fallos
* mayor coste de cableado e implementación

Se utiliza principalmente en **infraestructuras críticas o redes inalámbricas malladas**.

---

## 2. Direccionamiento IPv4 e IPv6

El **direccionamiento IP** permite identificar de forma única cada dispositivo conectado a una red.

---

### IPv4 (Internet Protocol version 4)

Características principales:

* longitud de **32 bits**
* dividido en **4 octetos**

Ejemplo:

```
192.168.1.10
```

---

#### Direcciones privadas (RFC 1918)

No son enrutable en Internet y se utilizan en redes internas.

| Clase   | Rango                         |
| ------- | ----------------------------- |
| Clase A | 10.0.0.0 – 10.255.255.255     |
| Clase B | 172.16.0.0 – 172.31.255.255   |
| Clase C | 192.168.0.0 – 192.168.255.255 |

---

#### Máscara de subred

La **máscara de subred** determina qué parte de la dirección IP corresponde a:

* **red**
* **host**

Ejemplo:

```
IP: 192.168.1.10
Máscara: 255.255.255.0
```

---

### IPv6 (Internet Protocol version 6)

Características principales:

* longitud de **128 bits**
* representación **hexadecimal**
* espacio de direcciones mucho mayor que IPv4

Ejemplo:

```
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```

---

#### Características destacadas

* soporte nativo de **IPsec**
* **autoconfiguración automática (SLAAC)**
* eliminación del problema de agotamiento de direcciones

---

## 3. VLAN (Virtual Local Area Network)

Las **VLAN** permiten dividir una red física en varias **redes lógicas independientes**.

Objetivos:

* mejorar la seguridad
* reducir tráfico broadcast
* facilitar la administración de la red

---

### Estándar IEEE 802.1Q

Define el sistema de **etiquetado (tagging)** que identifica a qué VLAN pertenece cada paquete.

Se utiliza en enlaces:

* **Trunk** → transporte de varias VLAN entre switches

---

### Ventajas de las VLAN

* separación de tráfico de usuarios y administración
* mejora de la seguridad
* optimización del ancho de banda
* mayor flexibilidad en la red

---

## 4. DHCP (Dynamic Host Configuration Protocol)

El **DHCP** es un servicio que asigna automáticamente parámetros de red a los dispositivos.

Parámetros asignados:

* dirección IP
* máscara de subred
* puerta de enlace
* servidor DNS

---

### Proceso DORA

Proceso utilizado para la asignación de direcciones IP.

1. **Discover** → el cliente busca servidores DHCP
2. **Offer** → el servidor ofrece una dirección IP
3. **Request** → el cliente solicita la IP ofrecida
4. **Acknowledge** → el servidor confirma la concesión

---

## 5. Administración y Diagnóstico de Red

La administración de redes implica gestionar dispositivos activos y diagnosticar problemas de conectividad.

---

### Dispositivos de red

#### Switch (Nivel 2)

Dispositivo que:

* opera en la **capa 2 del modelo OSI**
* utiliza **direcciones MAC**
* envía datos solo al puerto de destino

---

#### Router (Nivel 3)

Dispositivo que:

* opera en la **capa 3 del modelo OSI**
* conecta diferentes redes
* utiliza **direcciones IP** para enrutar paquetes

---

## 🛠️ Herramientas de Diagnóstico

### Comandos comunes de red

```bash
# Comprobar conectividad básica
ping 8.8.8.8

# Mostrar la ruta que sigue un paquete
tracert 8.8.8.8

# Ver configuración IP
ipconfig

# Consultar resolución DNS
nslookup google.com

# Mostrar c
```
