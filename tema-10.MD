# Tema 10 — Virtualización de Servidores

### Infraestructura virtual y alta disponibilidad

> Apuntes sobre virtualización de servidores, plataformas de virtualización y gestión de infraestructuras virtuales.

---

## 1. Principios de Virtualización

La **virtualización** es una tecnología que permite crear recursos **virtuales (lógicos)** a partir de recursos **físicos**, como servidores, redes o almacenamiento.

Gracias a la virtualización es posible ejecutar **varios sistemas operativos en un mismo servidor físico**, optimizando el uso del hardware.

---

### Hipervisor (VMM)

El **hipervisor** o **Virtual Machine Monitor (VMM)** es el software encargado de gestionar las máquinas virtuales.

Funciones principales:

* crear máquinas virtuales
* asignar recursos del host
* aislar cada máquina virtual
* controlar CPU, memoria, disco y red

---

### Tipos de Hipervisores

#### Tipo 1 (Bare-Metal)

Se ejecutan **directamente sobre el hardware físico**.

Características:

* mayor rendimiento
* mayor seguridad
* utilizados en centros de datos

Ejemplos:

* **VMware ESXi**
* **Microsoft Hyper-V**
* **Proxmox VE (KVM)**

---

#### Tipo 2 (Hosted)

Se ejecutan **sobre un sistema operativo anfitrión**.

Características:

* instalación sencilla
* utilizados en laboratorios y desarrollo

Ejemplos:

* **Oracle VirtualBox**
* **VMware Workstation**

---

## 2. Plataformas de Virtualización

Las plataformas de virtualización permiten administrar múltiples máquinas virtuales desde una infraestructura centralizada.

| Plataforma                | Desarrollador | Características                                   |
| ------------------------- | ------------- | ------------------------------------------------- |
| **Hyper-V**               | Microsoft     | Integración con Windows Server y Active Directory |
| **VMware vSphere / ESXi** | VMware        | Estándar empresarial con alta escalabilidad       |
| **VirtualBox**            | Oracle        | Hipervisor tipo 2 para desarrollo y pruebas       |
| **Proxmox VE**            | Proxmox       | Plataforma open source basada en Debian           |

Proxmox integra dos tecnologías principales:

* **KVM** → virtualización completa de máquinas
* **LXC** → contenedores ligeros

---

## 3. Gestión y Mantenimiento de Máquinas Virtuales

La gestión de máquinas virtuales implica controlar su **ciclo de vida completo**.

---

### Creación y configuración

Al crear una máquina virtual se definen varios recursos:

* **vCPU** (CPU virtual)
* **vRAM** (memoria asignada)
* **disco virtual**
* **adaptadores de red virtuales**

La memoria puede configurarse como:

* **estática**
* **dinámica**

---

### Snapshots (Instantáneas)

Un **snapshot** captura el estado completo de una máquina virtual en un momento determinado.

Incluye:

* estado del disco
* estado de la memoria
* configuración de la VM

Se utiliza normalmente:

* antes de actualizaciones
* antes de cambios críticos

⚠️ No debe utilizarse como sistema permanente de copia de seguridad.

---

### Clonación y plantillas

Permiten desplegar máquinas virtuales rápidamente.

Tipos:

* **Clonación** → copia exacta de una VM
* **Plantillas (Templates)** → imagen base para crear múltiples VMs

Esto facilita el despliegue masivo de servidores.

---

## 4. Redes y Almacenamiento Virtual

Las infraestructuras virtuales utilizan redes y sistemas de almacenamiento virtualizados.

---

### Redes virtuales

Las máquinas virtuales se conectan mediante **switches virtuales (vSwitch)**.

Tipos de red:

| Tipo                   | Descripción                       |
| ---------------------- | --------------------------------- |
| **Bridged / External** | conexión con la red física        |
| **Host-Only**          | comunicación entre host y VM      |
| **Internal**           | comunicación únicamente entre VMs |

---

### Almacenamiento virtual

Las máquinas virtuales utilizan **discos virtuales**.

Formatos más comunes:

* **VHD / VHDX** → Hyper-V
* **VMDK** → VMware
* **RAW / QCOW2** → KVM / Proxmox

En entornos empresariales se emplea **almacenamiento compartido**:

* **SAN** → iSCSI / Fibre Channel
* **NAS** → NFS / SMB

Esto permite mover máquinas virtuales entre hosts físicos.

---

## 5. Alta Disponibilidad (HA)

La **alta disponibilidad** garantiza que los servicios sigan funcionando incluso si falla un servidor físico.

---

### Live Migration / vMotion

Permite mover una máquina virtual **de un host físico a otro sin detenerla**.

Ventajas:

* mantenimiento sin interrupciones
* balanceo de carga entre servidores

---

### Failover Cluster

Un **cluster de virtualización** está formado por varios servidores físicos.

Si un nodo falla:

* las máquinas virtuales se reinician automáticamente
* se ejecutan en otro nodo del cluster

Requisito importante:

* **almacenamiento compartido** entre nodos

---

## 🛠️ Herramientas de Administración

### Hyper-V (PowerShell)

```powershell
# Listar todas las máquinas virtuales
Get-VM

# Crear snapshot de una VM
Checkpoint-VM -Name "Servidor_Web" -SnapshotName "Antes_de_Update"

# Ver switches virtuales
Get-VMSwitch
```
