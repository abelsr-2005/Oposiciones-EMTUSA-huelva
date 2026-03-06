# Tema 9. Sistemas Operativos: Linux, Windows Server 2019 y Windows 10/11

[cite_start]Este tema aborda la administración avanzada de sistemas operativos en entornos corporativos, centrando el foco en la estabilidad, seguridad y gestión centralizada[cite: 8, 9]. [cite_start]Se consideran como versiones de referencia Windows Server 2019 y Windows 10/11.

---

## 9.1. Configuración del sistema: Gestión, Directivas y Rendimiento

[cite_start]La administración profesional requiere el control total sobre los recursos del sistema y la automatización de configuraciones[cite: 10].

### 9.1.1. Gestión de Dispositivos y Servicios
* [cite_start]**Servicios del Sistema:** En entornos Windows, se gestionan mediante el complemento `services.msc`[cite: 10]. Los estados de inicio clave son: Automático, Automático (Inicio retrasado), Manual y Deshabilitado.
* [cite_start]**Gestión de Dispositivos:** Los controladores (drivers) deben estar firmados digitalmente en versiones de 64 bits para asegurar la integridad del kernel[cite: 10].

### 9.1.2. Directivas y Actualización
* [cite_start]**Gestión de Parches:** Se utiliza **WSUS** (Windows Server Update Services) para centralizar, aprobar y desplegar actualizaciones de seguridad en la infraestructura[cite: 10].
* [cite_start]**Directivas de Grupo (GPO):** Permiten la configuración masiva de equipos y usuarios[cite: 10]. [cite_start]El orden de aplicación es **LSDOU**: Local, Sitio, Dominio y Unidad Organizativa (esta última prevalece)[cite: 13].

### 9.1.3. Monitorización del Rendimiento
* [cite_start]**Monitor de Rendimiento (Perfmon):** Utiliza "contadores" para analizar en tiempo real el uso de CPU, memoria, disco y red[cite: 10].
* [cite_start]**Visor de Eventos:** Herramienta diagnóstica crítica dividida en registros de Aplicación, Seguridad (auditoría), Instalación y Sistema[cite: 10].

---

## 9.2. Administración Remota y Gestión de Incidencias

[cite_start]La capacidad de respuesta técnica depende del uso de protocolos de acceso remoto seguros y eficientes[cite: 11].

* [cite_start]**RDP (Remote Desktop Protocol):** Protocolo de Microsoft que opera en el puerto **TCP 3389**[cite: 11]. Se recomienda el uso de **NLA** (Network Level Authentication) para mitigar ataques de fuerza bruta.
* [cite_start]**PowerShell Remoting:** Basado en el protocolo **WinRM**[cite: 11]. Utiliza por defecto los puertos **5985 (HTTP)** y **5986 (HTTPS)**.
* [cite_start]**SSH (Secure Shell):** Protocolo estándar para la administración remota de Linux y disponible en versiones modernas de Windows Server[cite: 11]. Utiliza el puerto **TCP 22** y ofrece cifrado robusto.

---

## 9.3. Administración de Cuentas, Grupos y Permisos

[cite_start]El control de acceso se rige por políticas de seguridad estrictas y auditorías recurrentes[cite: 12].

### 9.3.1. Control de Privilegios y Acceso
* [cite_start]**Principio de Menor Privilegio:** Los usuarios solo deben poseer los permisos estrictamente necesarios para sus funciones[cite: 12].
* [cite_start]**Permisos NTFS:** Se aplican tanto en acceso local como en red[cite: 12]. Son acumulativos, pero la **Denegación explícita siempre prevalece**.
* [cite_start]**Permisos de Compartición:** Solo actúan cuando se accede al recurso a través de la red[cite: 12]. El permiso efectivo final es el **más restrictivo** entre la suma de NTFS y Compartición.

### 9.3.2. Auditoría
* [cite_start]Es esencial configurar directivas de auditoría para registrar intentos de inicio de sesión fallidos y acceso no autorizado a archivos sensibles en el log de **Seguridad**[cite: 12].

---

## 9.4. Gestión de Redes, Almacenamiento, Cifrado y Seguridad

[cite_start]Protección integral del sistema y gestión eficiente de recursos físicos y lógicos[cite: 15].

* [cite_start]**Gestión de Red e Impresión:** Configuración de interfaces, pilas TCP/IP y colas de impresión centralizadas[cite: 15].
* [cite_start]**Almacenamiento:** Implementación de cuotas de disco, gestión de sistemas de archivos (NTFS/ReFS) y volúmenes lógicos[cite: 15].
* [cite_start]**Cifrado (BitLocker):** Proporciona cifrado de unidad completa para proteger datos contra el robo físico del hardware[cite: 15].
* [cite_start]**Seguridad del Sistema:** Endurecimiento (*Hardening*) mediante el firewall del sistema y la desactivación de servicios no esenciales[cite: 15].

---

## 🛠️ Herramientas de Administración (Ejemplos Reales)

### PowerShell (Windows)
```powershell
# Verificar si el servicio de WinRM está activo para administración remota
Get-Service WinRM

# Obtener los últimos 5 errores del log de Sistema
Get-EventLog -LogName System -EntryType Error -Newest 5

# Forzar la actualización de GPOs en el equipo local
gpupdate /force
´´´
