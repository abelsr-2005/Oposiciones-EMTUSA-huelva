# Tema 10. Active Directory: Estructura, Roles FSMO, OU, Replicación y GPO

Active Directory Domain Services (AD DS) es el servicio de directorio centralizado para la gestión de identidades y recursos en la infraestructura corporativa de EMTUSA. Se basa en un modelo multimaestro con excepciones específicas para garantizar la integridad de la base de datos.

---

## 10.1. Estructura de Active Directory
La organización de AD se divide en componentes lógicos y físicos para facilitar la escalabilidad y administración.

### 10.1.1. Componentes Lógicos
* **Bosque (Forest):** El contenedor de seguridad de nivel superior que agrupa uno o más árboles de dominios.
* **Dominio:** Unidad administrativa fundamental que comparte una base de datos de directorio común.
* **Unidad Organizativa (OU):** Contenedor lógico utilizado para organizar objetos (usuarios, equipos, grupos) dentro de un dominio, facilitar la delegación de control y vincular GPOs.
* **Objetos:** Instancias individuales como usuarios, grupos, equipos o impresoras definidos en el esquema.

### 10.1.2. Componentes Físicos
* **Controladores de Dominio (DC):** Servidores que alojan una copia de la base de datos de AD (`ntds.dit`).
* **Sitios:** Representan la topología de la red física (subredes IP) y se utilizan para optimizar el tráfico de replicación.

---

## 10.2. Roles FSMO (Flexible Single Master Operations)
Existen cinco funciones específicas que, para evitar conflictos, solo pueden ser ejecutadas por un único controlador de dominio a la vez:

1. **Schema Master (Maestro de Esquema):** Único por bosque. Gestiona las modificaciones en la estructura de clases y atributos de AD.
2. **Domain Naming Master (Maestro de Nombres de Dominio):** Único por bosque. Controla la adición o eliminación de dominios en el bosque.
3. **PDC Emulator (Emulador de PDC):** Único por dominio. Actúa como servidor de tiempo, gestiona bloqueos de cuenta y cambios de contraseña.
4. **RID Master (Maestro de RID):** Único por dominio. Asigna secuencias de identificadores relativos a los DCs para la creación de nuevos objetos.
5. **Infrastructure Master (Maestro de Infraestructura):** Único por dominio. Sincroniza referencias de objetos entre dominios distintos.

---

## 10.3. Directivas de Grupo (GPO) y Replicación
Mecanismos para la gestión centralizada de configuraciones y la consistencia de los datos.

* **GPO (Group Policy Objects):** Conjunto de reglas que definen la configuración de usuarios y equipos. 
* **Orden de Aplicación (LSDOU):** Local -> Sitio (Site) -> Dominio -> Unidad Organizativa (OU). La configuración más específica (OU) prevalece sobre la general.
* **Replicación:** Proceso de sincronización de la base de datos entre DCs. En Windows Server 2019, la replicación de `SYSVOL` se realiza mediante **DFSR**.
* **Integración DNS:** AD depende de DNS para localizar servicios mediante registros **SRV**.

---

## 🛠️ Administración Técnica (Ejemplos)

### Verificación de Roles FSMO
```powershell
# Usando PowerShell para ver roles a nivel de dominio y bosque
Get-ADDomain | Select-Object InfrastructureMaster, RIDMaster, PDCEmulator
Get-ADForest | Select-Object SchemaMaster, DomainNamingMaster

# Forzar la actualización de directivas en un equipo cliente
gpupdate /force

# Generar informe de directivas resultantes (RSOP)
gpresult /R
```
