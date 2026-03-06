# Tema 16 — Seguridad Informática

### Copias de seguridad, protección perimetral y normativa de seguridad

> Apuntes sobre políticas de backup, cortafuegos, protección antimalware y normativa aplicable en seguridad informática.

---

# 1. Políticas de Copias de Seguridad y Recuperación

Las **copias de seguridad (backups)** constituyen la última línea de defensa frente a pérdida de datos, fallos del sistema o desastres.

Una política de backup adecuada garantiza:

* disponibilidad de la información
* recuperación ante fallos
* continuidad del servicio

---

## Tipos de copias de seguridad

### Copia completa (Full)

Copia todos los datos seleccionados.

Características:

* restauración rápida
* mayor tiempo de creación
* mayor consumo de almacenamiento

---

### Copia incremental

Copia únicamente los datos modificados desde la **última copia realizada**.

Características:

* menor uso de almacenamiento
* proceso de backup rápido
* restauración más compleja

---

### Copia diferencial

Copia los datos modificados desde la **última copia completa**.

Características:

* restauración más sencilla que la incremental
* mayor tamaño de backup con el tiempo

---

## Recuperación ante desastres (Disaster Recovery)

La **recuperación ante desastres** incluye políticas y procedimientos para restaurar sistemas tras incidentes graves.

Ejemplos de incidentes:

* fallo de servidores
* pérdida de datos
* ataques informáticos
* desastres físicos

---

## Conceptos RPO y RTO

| Concepto                           | Significado                                 |
| ---------------------------------- | ------------------------------------------- |
| **RPO (Recovery Point Objective)** | Tiempo máximo de pérdida de datos aceptable |
| **RTO (Recovery Time Objective)**  | Tiempo máximo para restaurar el servicio    |

Estos indicadores definen los objetivos de recuperación de una organización.

---

# 2. Cortafuegos y Protección Perimetral

Un **cortafuegos (firewall)** es un sistema que controla el tráfico de red mediante reglas de seguridad.

Su función principal es **permitir o bloquear comunicaciones** según políticas definidas.

---

## Configuración de reglas

Las reglas del firewall se basan en distintos parámetros:

* dirección de origen
* dirección de destino
* protocolo
* puerto

Esto permite controlar el acceso a los servicios de red.

---

## Política por defecto

En entornos seguros se aplica la política:

```
Default Deny
```

Esto significa que:

* todo el tráfico está bloqueado
* solo se permite el tráfico autorizado explícitamente

---

## Protección perimetral

La protección perimetral crea una barrera entre:

* la **red interna segura**
* las **redes externas no confiables**

Se implementa mediante:

* firewalls
* sistemas de detección de intrusos
* segmentación de red

---

## DMZ (Zona Desmilitarizada)

La **DMZ** es un segmento de red intermedio donde se ubican los servicios accesibles desde Internet.

Ejemplos de servidores en DMZ:

* servidores web
* servidores de correo
* servidores FTP

Esto evita que un compromiso externo afecte directamente a la red interna.

---

# 3. Protección Antimalware y Gestión Centralizada

La protección antimalware permite detectar, bloquear y eliminar software malicioso.

---

## Tipos de detección

### Detección basada en firmas

Identifica malware conocido comparando archivos con una base de datos de firmas.

Requiere:

* actualizaciones constantes

---

### Detección heurística o por comportamiento

Detecta amenazas analizando comportamientos sospechosos del sistema.

Ventajas:

* permite identificar amenazas desconocidas
* detecta malware nuevo

---

## Administración centralizada

Las soluciones empresariales utilizan **consolas de gestión centralizadas**.

Permiten:

* desplegar actualizaciones
* monitorizar amenazas
* gestionar alertas
* aplicar políticas de seguridad

Todo ello desde un único punto de control.

---

## Mitigación y respuesta

Cuando se detecta una amenaza se aplican protocolos de respuesta.

Pasos habituales:

* aislar el equipo infectado
* eliminar el malware
* restaurar sistemas afectados
* verificar integridad de datos

---

# 4. Referencias Normativas Aplicables

La seguridad informática en organismos públicos debe cumplir marcos normativos específicos.

---

## RGPD (Reglamento General de Protección de Datos)

Normativa europea que regula la **protección de datos personales**.

Objetivos principales:

* proteger la privacidad
* controlar el tratamiento de datos
* garantizar derechos de los ciudadanos

---

## ENS (Esquema Nacional de Seguridad)

El **ENS** establece los requisitos de seguridad para los sistemas de información en administraciones públicas.

Define:

* principios de seguridad
* medidas organizativas
* controles técnicos

Es obligatorio para organismos públicos.

---

# 🛠️ Buenas Prácticas y Administración

## Regla 3-2-1 de backups

Una estrategia recomendada de copias de seguridad consiste en:

* mantener **3 copias de los datos**
* almacenarlas en **2 soportes diferentes**
* guardar **1 copia fuera del sitio físico (off-site)**

Esto protege frente a desastres físicos o fallos de infraestructura.

---

## Comandos de seguridad (PowerShell)

```powershell
# Listar reglas del firewall de Windows
Get-NetFirewallRule

# Crear regla para bloquear tráfico entrante en un puerto
New-NetFirewallRule -DisplayName "Bloquear Puerto" -Direction Inbound -LocalPort 80 -Action Block -Protocol TCP
```

---

# 💡 Conceptos Clave para el Examen

## Regla de oro del firewall

```
Lo que no está explícitamente permitido, está prohibido.
```

---

## Diferencia entre copia incremental y diferencial

| Tipo        | Dependencia                                 |
| ----------- | ------------------------------------------- |
| Incremental | depende de la copia anterior                |
| Diferencial | depende siempre de la última copia completa |

---

## ENS

El **Esquema Nacional de Seguridad** es obligatorio para organismos públicos.

---

## Actualización centralizada

La gestión centralizada es clave para una protección antimalware eficaz en entornos corporativos.
