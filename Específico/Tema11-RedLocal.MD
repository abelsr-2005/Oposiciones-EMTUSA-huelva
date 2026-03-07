# 🌐 Tema 11 — Red Local (LAN)

## 📚 Introducción

Una **red de área local (LAN, Local Area Network)** es un conjunto de dispositivos conectados entre sí dentro de un área geográfica limitada, como una oficina, edificio o campus. Las redes LAN permiten compartir recursos, acceder a servicios corporativos y facilitar la comunicación entre equipos informáticos.

En entornos empresariales, las LAN se basan en tecnologías Ethernet y utilizan dispositivos como **switches, routers y puntos de acceso**, además de servicios de red como DHCP o DNS. La correcta planificación de la red, el direccionamiento IP y la segmentación mediante VLAN son elementos fundamentales para garantizar rendimiento, seguridad y escalabilidad.

---

## 🧩 1. Topologías de Red

La **topología de red** describe la forma en que los dispositivos se conectan entre sí dentro de una red. Puede analizarse desde dos perspectivas:

* **Topología física**: disposición real del cableado y dispositivos.
* **Topología lógica**: forma en que circulan los datos por la red.

Las topologías determinan la **fiabilidad, escalabilidad y facilidad de administración** de la red.

### ⭐ Topología en Estrella

Es la topología predominante en redes LAN modernas.

Características principales:

* Todos los dispositivos se conectan a un **dispositivo central**, normalmente un switch.
* Si falla un cable, solo se ve afectado el equipo conectado a ese enlace.
* Facilita la administración, monitorización y ampliación de la red.

Ventajas:

* Alta fiabilidad
* Fácil diagnóstico de fallos
* Escalabilidad

Inconveniente principal:

* Dependencia del dispositivo central.

### 🌳 Topología en Árbol

La topología en árbol es una extensión de la topología en estrella organizada de forma **jerárquica**.

Características:

* Los switches se organizan en distintos niveles (núcleo, distribución y acceso).
* Permite ampliar la red añadiendo nuevos nodos sin modificar la estructura principal.
* Muy utilizada en redes empresariales y campus universitarios.

Este modelo suele corresponder con la arquitectura de red **core-distribution-access**.

### 🔗 Topología en Malla

En una topología de malla cada dispositivo está conectado con varios dispositivos de la red.

Características:

* Alta **redundancia de enlaces**.
* Gran tolerancia a fallos.
* Mayor complejidad de implementación.

Puede existir:

* **Malla completa**: todos los nodos conectados entre sí.
* **Malla parcial**: solo algunos enlaces redundantes.

Se utiliza especialmente en:

* redes críticas
* infraestructuras de backbone
* redes inalámbricas malladas.

---

## 🧮 2. Direccionamiento IPv4 e IPv6

El **direccionamiento IP** permite identificar de manera única cada dispositivo conectado a una red basada en el protocolo IP.

Las direcciones IP se utilizan para **localizar dispositivos y dirigir los paquetes de datos** entre origen y destino.

### 🌍 IPv4 (Internet Protocol version 4)

IPv4 es la versión histórica del protocolo IP y sigue siendo ampliamente utilizada.

Características:

* Longitud de **32 bits**.
* Representación decimal separada por puntos.
* Compuesta por **4 octetos** (0–255).

Ejemplo:

```
192.168.1.10
```

Una dirección IPv4 se divide en dos partes:

* **Identificador de red**
* **Identificador de host**

#### Direcciones privadas (RFC 1918)

Las direcciones privadas se utilizan en redes internas y no son enrutable directamente en Internet.

| Clase | Rango                         |
| ----- | ----------------------------- |
| A     | 10.0.0.0 – 10.255.255.255     |
| B     | 172.16.0.0 – 172.31.255.255   |
| C     | 192.168.0.0 – 192.168.255.255 |

Para acceder a Internet desde estas redes se utiliza normalmente **NAT (Network Address Translation)**.

#### Máscara de subred

La **máscara de subred** determina qué parte de la dirección IP pertenece a la red y qué parte identifica al host.

Ejemplo:

```
IP: 192.168.1.10
Máscara: 255.255.255.0
```

También puede expresarse en **notación CIDR**:

```
192.168.1.10/24
```

La subnetting permite dividir una red grande en subredes más pequeñas para mejorar la organización y el control del tráfico.

### 🌐 IPv6 (Internet Protocol version 6)

IPv6 se desarrolló para solucionar el agotamiento de direcciones IPv4.

Características principales:

* Longitud de **128 bits**.
* Representación hexadecimal.
* Gran espacio de direcciones disponible.

Ejemplo:

```
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```

IPv6 incluye mejoras importantes:

* Autoconfiguración automática (**SLAAC**)
* Mejor soporte para movilidad
* Seguridad integrada mediante **IPsec**
* Simplificación del encabezado del protocolo

---

## 🧱 3. VLAN (Virtual Local Area Network)

Una **VLAN** permite dividir una red física en múltiples redes lógicas independientes.

Esto se utiliza para segmentar el tráfico de red y mejorar tanto la seguridad como el rendimiento.

Ejemplo de segmentación:

* VLAN 10 → Administración
* VLAN 20 → Usuarios
* VLAN 30 → Servidores

Los dispositivos dentro de una misma VLAN se comportan como si estuvieran en la misma red física.

### 🔖 Estándar IEEE 802.1Q

El estándar **IEEE 802.1Q** define el mecanismo de etiquetado de tramas Ethernet para identificar a qué VLAN pertenece cada paquete.

Tipos de enlaces:

* **Access** → conecta dispositivos finales a una VLAN específica.
* **Trunk** → transporta tráfico de múltiples VLAN entre switches o hacia routers.

### Ventajas de las VLAN

* Segmentación lógica de la red
* Reducción del tráfico broadcast
* Mayor seguridad
* Mejora del rendimiento
* Flexibilidad en la administración

---

## 📡 4. DHCP (Dynamic Host Configuration Protocol)

El **DHCP** es un protocolo que permite asignar automáticamente parámetros de red a los dispositivos cuando se conectan a una red.

Entre los parámetros que puede proporcionar se encuentran:

* Dirección IP
* Máscara de subred
* Puerta de enlace
* Servidores DNS
* Tiempo de concesión (lease time)

El uso de DHCP simplifica la administración de redes grandes evitando la configuración manual de cada dispositivo.

### 🔄 Proceso DORA

El proceso de asignación de dirección IP sigue cuatro fases:

1. **Discover** → el cliente busca servidores DHCP.
2. **Offer** → el servidor ofrece una dirección IP disponible.
3. **Request** → el cliente solicita la dirección ofrecida.
4. **Acknowledge** → el servidor confirma la concesión.

Este proceso permite la asignación dinámica de direcciones dentro de un rango configurado.

---

## 🖧 5. Administración y Diagnóstico de Red

La administración de redes LAN implica la configuración, monitorización y mantenimiento de los dispositivos de red para garantizar la conectividad y el rendimiento.

### 🔌 Switch (Capa 2 del modelo OSI)

Un **switch** es un dispositivo de red que opera principalmente en la **capa 2 (enlace de datos)** del modelo OSI.

Funciones principales:

* Conectar dispositivos dentro de una red local
* Aprender direcciones MAC
* Enviar tramas solo al puerto de destino
* Reducir colisiones de red

Los switches gestionables permiten además:

* configuración de VLAN
* control de tráfico
* monitorización del estado de la red

### 🧭 Router (Capa 3 del modelo OSI)

Un **router** opera en la **capa 3 (red)** del modelo OSI.

Funciones principales:

* Interconectar diferentes redes
* Determinar la mejor ruta para los paquetes
* Gestionar el tráfico entre redes

También puede proporcionar servicios adicionales como:

* NAT
* DHCP
* filtrado mediante listas de control de acceso (ACL)

---

## 🛠️ Herramientas de Diagnóstico de Red

Las herramientas de diagnóstico permiten detectar problemas de conectividad, latencia o resolución de nombres.

### Comandos básicos de red

```bash
# Comprobar conectividad
ping 8.8.8.8

# Mostrar la ruta que sigue un paquete
tracert 8.8.8.8

# Ver configuración IP
ipconfig

# Consultar resolución DNS
nslookup google.com

# Mostrar conexiones de red activas
netstat
```

Otras herramientas habituales en administración de redes incluyen:

* **Wireshark** para análisis de tráfico
* **Nmap** para escaneo de red
* **iperf** para pruebas de rendimiento

Estas herramientas permiten diagnosticar problemas de red y analizar el comportamiento del tráfico en entornos corporativos.
