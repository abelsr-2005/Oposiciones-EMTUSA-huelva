# 🖥️ Tema 10 — Virtualización de Servidores

## 📚 Introducción

La virtualización de servidores es una tecnología fundamental en las infraestructuras informáticas modernas. Permite ejecutar múltiples sistemas operativos y aplicaciones sobre un mismo hardware físico mediante la creación de máquinas virtuales (VM). Esto mejora el aprovechamiento de los recursos, reduce costes de infraestructura y facilita la gestión y escalabilidad de los servicios.

En entornos corporativos y centros de datos, la virtualización es una pieza clave para implementar arquitecturas flexibles, sistemas de alta disponibilidad y procesos eficientes de mantenimiento.

---

## ⚙️ 1. Principios de Virtualización

La virtualización consiste en la abstracción del hardware físico mediante software, permitiendo que varios sistemas operativos funcionen simultáneamente sobre una misma máquina física denominada **host**.

Cada sistema operativo virtual se ejecuta dentro de una **máquina virtual**, que dispone de recursos virtualizados como CPU, memoria, almacenamiento y red.

Entre los principales objetivos de la virtualización se encuentran:

* Optimizar el uso del hardware
* Reducir el número de servidores físicos
* Facilitar la gestión de infraestructuras
* Mejorar la disponibilidad de los servicios
* Permitir entornos de prueba y desarrollo aislados

### Hipervisor (Virtual Machine Monitor)

El **hipervisor** o **VMM (Virtual Machine Monitor)** es el componente software encargado de crear, ejecutar y administrar las máquinas virtuales.

Sus funciones principales incluyen:

* Crear y eliminar máquinas virtuales
* Asignar recursos físicos a cada VM
* Garantizar el aislamiento entre máquinas
* Gestionar el acceso a CPU, memoria, disco y red
* Supervisar el rendimiento del sistema

---

## 🧩 2. Tipos de Hipervisores

### Hipervisor Tipo 1 (Bare Metal)

Los hipervisores de **tipo 1** se ejecutan directamente sobre el hardware físico sin necesidad de un sistema operativo anfitrión.

Características principales:

* Mayor rendimiento
* Mayor estabilidad
* Mejor nivel de seguridad
* Uso habitual en centros de datos y entornos empresariales

Ejemplos:

* VMware ESXi
* Microsoft Hyper-V
* Proxmox VE (basado en KVM)

### Hipervisor Tipo 2 (Hosted)

Los hipervisores de **tipo 2** se ejecutan sobre un sistema operativo anfitrión.

Características principales:

* Instalación sencilla
* Uso habitual en entornos de pruebas
* Adecuados para desarrollo o formación

Ejemplos:

* Oracle VirtualBox
* VMware Workstation

---

## 🖧 3. Plataformas de Virtualización

Las plataformas de virtualización permiten gestionar infraestructuras virtuales completas desde herramientas centralizadas.

### Microsoft Hyper‑V

Hyper‑V es el sistema de virtualización integrado en Windows Server. Permite crear y administrar máquinas virtuales, redes virtuales y almacenamiento virtual.

Ventajas principales:

* Integración con Active Directory
* Administración mediante PowerShell
* Compatibilidad con entornos Windows
* Integración con herramientas de Microsoft

### VMware vSphere / ESXi

VMware es una de las plataformas de virtualización empresarial más utilizadas.

Características:

* Alta escalabilidad
* Herramientas avanzadas de gestión
* Soporte de alta disponibilidad
* Migración en caliente de máquinas virtuales (vMotion)

### Oracle VirtualBox

VirtualBox es una solución de virtualización multiplataforma utilizada principalmente para desarrollo, pruebas o entornos de laboratorio.

Permite ejecutar múltiples sistemas operativos invitados sobre Windows, Linux o macOS.

### Proxmox VE

Proxmox Virtual Environment es una plataforma de virtualización **open source** basada en Debian.

Integra dos tecnologías principales:

* **KVM (Kernel-based Virtual Machine)** para virtualización completa
* **LXC (Linux Containers)** para contenedores ligeros

Ofrece una interfaz web de administración centralizada y herramientas para clustering y alta disponibilidad.

---

## 🧰 4. Gestión y Mantenimiento de Máquinas Virtuales

La administración de máquinas virtuales implica controlar todo su ciclo de vida: creación, configuración, mantenimiento y eliminación.

### Creación y configuración

Al crear una máquina virtual se definen los recursos que tendrá disponibles:

* **vCPU**: número de procesadores virtuales
* **vRAM**: memoria asignada
* **Disco virtual**: almacenamiento de la VM
* **Adaptadores de red virtuales**

La memoria puede configurarse de distintas formas:

* **Memoria estática**: asignación fija
* **Memoria dinámica**: el hipervisor ajusta el uso según la carga

### Snapshots o instantáneas

Un **snapshot** guarda el estado completo de una máquina virtual en un momento determinado.

Incluye:

* Estado del disco
* Estado de la memoria
* Configuración de hardware virtual

Se utilizan habitualmente para:

* Pruebas de actualizaciones
* Cambios de configuración
* Puntos de recuperación rápidos

No sustituyen a las copias de seguridad tradicionales.

### Clonación y plantillas

Las herramientas de virtualización permiten replicar máquinas virtuales de forma rápida.

Tipos:

* **Clonación**: copia exacta de una máquina virtual existente
* **Plantillas (Templates)**: imagen base utilizada para crear múltiples VMs

Esto facilita el despliegue rápido de servidores en entornos corporativos.

---

## 🌐 5. Redes Virtuales

Las máquinas virtuales se conectan a redes mediante **switches virtuales (vSwitch)** administrados por el hipervisor.

Tipos de redes virtuales más comunes:

* **Bridged / External**: conecta la VM directamente a la red física
* **Host‑Only**: comunicación entre host y máquinas virtuales
* **Internal**: comunicación únicamente entre máquinas virtuales

Los entornos empresariales también permiten:

* segmentación mediante VLAN
* control del tráfico
* aislamiento de redes virtuales

---

## 💾 6. Almacenamiento Virtual

Las máquinas virtuales utilizan archivos que simulan discos duros.

Formatos habituales:

* **VHD / VHDX** — Hyper‑V
* **VMDK** — VMware
* **QCOW2 / RAW** — KVM y Proxmox

En infraestructuras profesionales se utiliza almacenamiento compartido para permitir la movilidad de las máquinas virtuales entre hosts.

Tecnologías habituales:

* **SAN (Storage Area Network)** mediante iSCSI o Fibre Channel
* **NAS (Network Attached Storage)** mediante NFS o SMB

Este almacenamiento compartido es esencial para implementar alta disponibilidad.

---

## 🔁 7. Alta Disponibilidad (High Availability)

La alta disponibilidad permite que los servicios continúen funcionando incluso si se produce un fallo en un servidor físico.

Esto se consigue mediante la combinación de varios hosts físicos que trabajan conjuntamente.

### Migración en caliente

La migración en caliente permite mover una máquina virtual de un host físico a otro **sin detener el servicio**.

Ejemplos:

* Live Migration (Hyper‑V)
* vMotion (VMware)

Ventajas:

* mantenimiento sin interrupciones
* balanceo de carga
* redistribución de recursos

### Clúster de virtualización

Un **cluster** está formado por varios servidores físicos conectados a almacenamiento compartido.

Si un nodo falla:

* las máquinas virtuales se reinician automáticamente
* se ejecutan en otro nodo del cluster

Esto garantiza la continuidad de los servicios críticos.

---

## 🛠️ Herramientas de Administración

### Administración mediante PowerShell (Hyper‑V)

Ejemplos de comandos:

```powershell
# Listar máquinas virtuales
Get-VM

# Crear snapshot de una máquina virtual
Checkpoint-VM -Name "Servidor_Web" -SnapshotName "Antes_de_Update"

# Ver switches virtuales
Get-VMSwitch
```

PowerShell permite automatizar la administración de infraestructuras virtuales, facilitando tareas repetitivas y la gestión centralizada del entorno.
