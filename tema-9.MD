# Tema 9 — Sistemas Operativos

### Linux, Windows Server 2019 y Windows 10/11

> Apuntes de administración de sistemas operativos en entornos corporativos.

---

## 1. Configuración del sistema: Gestión, Directivas y Rendimiento

La administración de sistemas requiere controlar los recursos del sistema y automatizar configuraciones para garantizar **estabilidad, seguridad y eficiencia** en el funcionamiento de los equipos.

---

### 1.1 Gestión de Dispositivos y Servicios

#### Servicios del sistema

En sistemas Windows los servicios se administran mediante la herramienta:

```
services.msc
```

Tipos de inicio principales:

* **Automático** → el servicio se inicia al arrancar el sistema
* **Automático (inicio retrasado)** → se inicia después del arranque
* **Manual** → solo se inicia cuando una aplicación lo requiere
* **Deshabilitado** → el servicio no puede iniciarse

#### Gestión de dispositivos

Los **drivers** permiten que el sistema operativo se comunique con el hardware.

En sistemas **Windows de 64 bits** los controladores deben estar **firmados digitalmente** para proteger la integridad del kernel.

---

### 1.2 Directivas y Actualización

#### Gestión de parches

Las actualizaciones del sistema pueden centralizarse mediante:

**WSUS — Windows Server Update Services**

Permite:

* descargar actualizaciones
* aprobar parches
* desplegar actualizaciones en toda la red

#### Directivas de grupo (GPO)

Las **GPO (Group Policy Objects)** permiten aplicar configuraciones masivas a usuarios y equipos dentro de un dominio.

Orden de aplicación de directivas (**LSDOU**):

1. **Local**
2. **Site (Sitio)**
3. **Domain (Dominio)**
4. **OU (Unidad Organizativa)**

La **última aplicada tiene prioridad**.

---

### 1.3 Monitorización del Rendimiento

#### Monitor de rendimiento (Perfmon)

Permite analizar el uso de recursos mediante **contadores de rendimiento**:

* CPU
* memoria
* disco
* red

#### Visor de eventos

Herramienta esencial para diagnosticar problemas.

Registros principales:

* **Aplicación**
* **Seguridad**
* **Instalación**
* **Sistema**

---

## 2. Administración Remota y Gestión de Incidencias

La administración remota permite gestionar sistemas sin acceso físico al equipo.

---

### RDP (Remote Desktop Protocol)

Protocolo de Microsoft para acceso remoto gráfico.

**Puerto:**

```
TCP 3389
```

Se recomienda habilitar **NLA (Network Level Authentication)** para mejorar la seguridad.

---

### PowerShell Remoting

Permite administrar equipos mediante comandos de PowerShell.

Basado en **WinRM**.

Puertos utilizados:

```
5985 → HTTP
5986 → HTTPS
```

---

### SSH (Secure Shell)

Protocolo estándar para administración remota en Linux y también disponible en Windows.

**Puerto:**

```
TCP 22
```

Proporciona comunicaciones **cifradas y seguras**.

---

## 3. Administración de Cuentas, Grupos y Permisos

La gestión de usuarios y permisos es fundamental para garantizar la **seguridad del sistema**.

---

### 3.1 Control de Privilegios y Acceso

#### Principio de menor privilegio

Los usuarios deben tener **solo los permisos necesarios** para realizar su trabajo.

---

#### Permisos NTFS

Se aplican en accesos:

* locales
* por red

Características:

* son **acumulativos**
* una **denegación explícita siempre prevalece**

---

#### Permisos de compartición

Solo se aplican cuando el acceso se realiza **desde la red**.

El permiso final es el **más restrictivo** entre:

* permisos NTFS
* permisos de compartición

---

### 3.2 Auditoría

Las políticas de auditoría permiten registrar eventos de seguridad como:

* intentos de inicio de sesión fallidos
* accesos a archivos sensibles
* cambios en configuraciones críticas

Los registros se almacenan en:

```
Visor de eventos → Registro de Seguridad
```

---

## 4. Gestión de Redes, Almacenamiento, Cifrado y Seguridad

La administración del sistema incluye la gestión de recursos físicos y la protección de los datos.

---

### Gestión de red e impresión

Incluye:

* configuración de interfaces de red
* pila TCP/IP
* gestión de impresoras
* colas de impresión centralizadas

---

### Almacenamiento

Gestión de:

* sistemas de archivos **NTFS**
* sistemas de archivos **ReFS**
* volúmenes lógicos
* **cuotas de disco**

---

### Cifrado con BitLocker

**BitLocker** proporciona cifrado completo de unidades para proteger los datos frente a:

* robo
* pérdida del equipo

---

### Seguridad del sistema

El **hardening** consiste en reforzar la seguridad del sistema mediante:

* activar el firewall
* deshabilitar servicios innecesarios
* aplicar actualizaciones
* limitar accesos administrativos

---

## 🛠️ Herramientas de Administración (Ejemplos Reales)

### PowerShell (Windows)

```powershell
# Verificar si el servicio de WinRM está activo
Get-Service WinRM

# Obtener los últimos 5 errores del sistema
Get-EventLog -LogName System -EntryType Error -Newest 5

# Forzar actualización de directivas de grupo
gpupdate /force
```

---

### Bash (Linux)

```bash
# Monitorizar procesos en tiempo real
top

# Cambiar permisos de un archivo
chmod 644 archivo.txt

# Estado del servicio SSH
systemctl status ssh
```
