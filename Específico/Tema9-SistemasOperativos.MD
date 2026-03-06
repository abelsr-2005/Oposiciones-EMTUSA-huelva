# 🖥️ Tema 9 — Sistemas Operativos

## 🧩 Linux, Windows Server 2019 y Windows 10/11

Los sistemas operativos constituyen el núcleo del funcionamiento de cualquier infraestructura informática. En entornos corporativos, sistemas como **Linux**, **Windows Server 2019** y **Windows 10/11** permiten gestionar recursos de hardware, usuarios, aplicaciones y servicios de red de forma centralizada.

La administración de estos sistemas implica la configuración eficiente del sistema, la gestión de usuarios y permisos, la monitorización del rendimiento, la administración remota y la implementación de medidas de seguridad que garanticen la disponibilidad y protección de los recursos de la organización.

---

## ⚙️ Configuración del sistema: gestión, directivas y rendimiento

La correcta configuración del sistema operativo es esencial para garantizar estabilidad, seguridad y rendimiento. En entornos empresariales esta administración se realiza mediante herramientas centralizadas que permiten controlar dispositivos, servicios, actualizaciones y políticas de configuración.

### 🔧 Gestión de dispositivos y servicios

Los **servicios del sistema** son procesos que se ejecutan en segundo plano y que proporcionan funciones esenciales al sistema operativo o a las aplicaciones instaladas.

En sistemas Windows, estos servicios se administran mediante la consola de servicios, accesible a través de:

```
services.msc
```

Desde esta herramienta es posible iniciar, detener, reiniciar o modificar el tipo de inicio de cada servicio.

Los tipos de inicio principales son:

* **Automático**: el servicio se inicia durante el arranque del sistema.
* **Automático (inicio retrasado)**: el servicio se inicia unos momentos después del arranque para reducir la carga inicial del sistema.
* **Manual**: el servicio solo se ejecuta cuando una aplicación o el administrador lo solicita.
* **Deshabilitado**: el servicio no puede iniciarse mientras se mantenga esta configuración.

La gestión de **dispositivos de hardware** se realiza mediante controladores o *drivers*, que actúan como intermediarios entre el sistema operativo y el hardware. En sistemas Windows de 64 bits, los controladores deben estar **firmados digitalmente**, lo que garantiza que proceden de una fuente confiable y que no han sido modificados.

---

### 🧾 Directivas y actualización del sistema

En infraestructuras corporativas es fundamental mantener todos los equipos actualizados y configurados de forma homogénea.

#### Gestión de actualizaciones

Las actualizaciones de seguridad y mantenimiento pueden gestionarse de forma centralizada mediante **Windows Server Update Services (WSUS)**. Este servicio permite a los administradores descargar actualizaciones desde Microsoft y distribuirlas posteriormente a los equipos de la red.

Entre sus funciones principales destacan:

* Descargar actualizaciones del sistema operativo y otros productos Microsoft.
* Aprobar o rechazar parches antes de su instalación.
* Programar despliegues de actualizaciones en equipos de la red.
* Reducir el consumo de ancho de banda al centralizar las descargas.

#### Directivas de grupo (GPO)

Las **Group Policy Objects (GPO)** permiten aplicar configuraciones de forma centralizada a usuarios y equipos dentro de un dominio de Active Directory. Gracias a estas directivas es posible establecer políticas de seguridad, restricciones de software, configuraciones del sistema o scripts de inicio.

Las directivas se aplican siguiendo el orden conocido como **LSDOU**:

1. Local
2. Site (Sitio)
3. Domain (Dominio)
4. OU (Unidad Organizativa)

En caso de conflicto entre configuraciones, la última directiva aplicada tiene prioridad.

---

### 📊 Monitorización del rendimiento

La monitorización del sistema permite detectar cuellos de botella, analizar el uso de recursos y diagnosticar problemas antes de que afecten al funcionamiento de los servicios.

#### Monitor de rendimiento

El **Monitor de rendimiento (Performance Monitor o Perfmon)** permite analizar el comportamiento del sistema mediante contadores de rendimiento que miden diferentes recursos, como por ejemplo:

* Uso de CPU
* Consumo de memoria
* Actividad del disco
* Tráfico de red

Estos contadores permiten generar gráficos en tiempo real o recopilar datos históricos para análisis posteriores.

#### Visor de eventos

El **Visor de eventos** es una herramienta fundamental para la administración y diagnóstico del sistema. Registra eventos generados por el sistema operativo, las aplicaciones y los servicios.

Los registros más importantes son:

* **Aplicación**: eventos generados por programas instalados.
* **Seguridad**: auditorías relacionadas con accesos y eventos de seguridad.
* **Instalación**: eventos relacionados con instalaciones de software.
* **Sistema**: eventos generados por el propio sistema operativo.

---

## 🌐 Administración remota y gestión de incidencias

La administración remota permite gestionar servidores y estaciones de trabajo sin necesidad de acceso físico. Esta capacidad es esencial en entornos empresariales donde se administran numerosos equipos distribuidos en diferentes ubicaciones.

### 🖥️ Remote Desktop Protocol (RDP)

**RDP** es el protocolo de acceso remoto desarrollado por Microsoft que permite controlar gráficamente un equipo a través de la red.

Utiliza por defecto el puerto:

```
TCP 3389
```

Para mejorar la seguridad se recomienda utilizar **Network Level Authentication (NLA)**, que obliga a que el usuario se autentique antes de establecer la sesión remota.

---

### 💻 PowerShell Remoting

**PowerShell Remoting** permite administrar sistemas Windows mediante comandos remotos. Se basa en el protocolo **WinRM (Windows Remote Management)** y facilita la automatización de tareas administrativas en múltiples equipos.

Puertos utilizados:

```
5985 → HTTP
5986 → HTTPS
```

Gracias a esta tecnología es posible ejecutar scripts, gestionar servicios, consultar registros o modificar configuraciones de forma remota.

---

### 🔐 SSH (Secure Shell)

**SSH** es el protocolo estándar para administración remota segura en sistemas Linux y también está disponible en versiones modernas de Windows.

Puerto utilizado:

```
TCP 22
```

SSH proporciona autenticación segura y comunicaciones cifradas, lo que evita que las credenciales o los datos transmitidos puedan ser interceptados en la red.

---

## 👥 Administración de cuentas, grupos y permisos

La gestión de usuarios y permisos es uno de los pilares de la seguridad en sistemas operativos corporativos. Permite controlar quién puede acceder a los recursos y qué acciones puede realizar cada usuario.

### 🔑 Control de privilegios y acceso

#### Principio de menor privilegio

El **principio de menor privilegio** establece que los usuarios deben disponer únicamente de los permisos necesarios para realizar su trabajo. Esto reduce el riesgo de errores, accesos indebidos y posibles ataques internos.

---

#### Permisos NTFS

Los sistemas Windows utilizan el sistema de archivos **NTFS**, que permite establecer permisos detallados sobre archivos y carpetas.

Características principales:

* Se aplican tanto a accesos locales como a accesos a través de red.
* Los permisos son acumulativos cuando un usuario pertenece a varios grupos.
* Una **denegación explícita** siempre prevalece sobre cualquier permiso concedido.

---

#### Permisos de compartición

Cuando un recurso se comparte en red, entran en juego los **permisos de compartición**.

En estos casos el permiso efectivo será el **más restrictivo** entre:

* los permisos NTFS
* los permisos de compartición

Esta combinación permite establecer controles de acceso más precisos.

---

### 📋 Auditoría de seguridad

Las políticas de auditoría permiten registrar eventos relevantes para la seguridad del sistema, como por ejemplo:

* intentos de inicio de sesión fallidos
* accesos a archivos sensibles
* cambios en configuraciones críticas

Estos eventos se registran en el **Registro de Seguridad** del Visor de eventos, lo que permite a los administradores detectar comportamientos sospechosos o investigar incidentes.

---

## 💾 Gestión de redes, almacenamiento, cifrado y seguridad

La administración de sistemas operativos también incluye la gestión de recursos de red, almacenamiento y mecanismos de protección de datos.

### 🌍 Gestión de red e impresión

Los sistemas operativos permiten configurar y administrar diferentes componentes de red, como:

* interfaces de red
* configuración de la pila TCP/IP
* direcciones IP y DNS
* servicios de impresión en red
* colas de impresión centralizadas

En entornos corporativos es habitual utilizar servidores de impresión que gestionan las impresoras compartidas para toda la organización.

---

### 🗄️ Gestión del almacenamiento

Los sistemas Windows utilizan principalmente los sistemas de archivos **NTFS** y **ReFS** para gestionar el almacenamiento.

Entre las funciones de administración del almacenamiento destacan:

* creación de particiones y volúmenes
* gestión de discos dinámicos
* establecimiento de **cuotas de disco**
* control del uso del espacio por usuario

Estas herramientas permiten optimizar el uso del almacenamiento y evitar que un único usuario consuma todos los recursos disponibles.

---

### 🔒 Cifrado con BitLocker

**BitLocker** es una tecnología de cifrado de disco completo incluida en Windows que protege los datos almacenados en el equipo.

Su objetivo es evitar el acceso no autorizado a la información en caso de robo o pérdida del dispositivo. El cifrado puede integrarse con módulos **TPM (Trusted Platform Module)** para reforzar la seguridad del arranque.

---

### 🛡️ Seguridad del sistema

El **hardening del sistema** consiste en aplicar configuraciones que reduzcan la superficie de ataque del sistema operativo.

Entre las medidas más habituales se encuentran:

* habilitar y configurar el firewall del sistema
* deshabilitar servicios innecesarios
* aplicar actualizaciones de seguridad periódicamente
* limitar el uso de cuentas administrativas
* monitorizar los registros de eventos

Estas prácticas contribuyen a mejorar la seguridad global de la infraestructura informática.

---

## 🧪 Herramientas de administración (ejemplos prácticos)

### 💻 PowerShell en Windows

```powershell
# Comprobar si el servicio WinRM está activo
Get-Service WinRM

# Obtener los últimos cinco errores registrados en el sistema
Get-EventLog -LogName System -EntryType Error -Newest 5

# Forzar la actualización de directivas de grupo
gpupdate /force
```

---

### 🐧 Bash en Linux

```bash
# Monitorizar procesos en tiempo real
top

# Cambiar permisos de un archivo
chmod 644 archivo.txt

# Comprobar el estado del servicio SSH
systemctl status ssh
```
