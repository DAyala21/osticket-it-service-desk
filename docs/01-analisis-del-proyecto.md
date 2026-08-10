# Análisis del Proyecto — Mesa de Servicios IT

## 1. Descripción del proyecto

Este proyecto tiene como objetivo implementar una mesa de servicios IT basada en osTicket para centralizar, organizar y realizar seguimiento a las solicitudes de soporte tecnológico de la organización.

Actualmente, las solicitudes de soporte se reciben principalmente mediante canales informales como WhatsApp, lo que dificulta realizar seguimiento, establecer prioridades, mantener un historial de atención y obtener indicadores sobre la operación del área de IT.

La solución propuesta permitirá centralizar las solicitudes mediante un sistema de tickets, facilitando la gestión y trazabilidad de los incidentes y requerimientos.

---

## 2. Situación actual

La organización cuenta aproximadamente con 220 usuarios que pueden requerir soporte tecnológico.

Actualmente, la atención de soporte se realiza principalmente mediante WhatsApp y comunicación directa con el analista IT.

El área cuenta principalmente con un analista encargado de la atención de soporte. En determinadas situaciones, un integrante del área de desarrollo presta apoyo para resolver algunos requerimientos, aunque su función principal no corresponde a la atención de soporte IT.

### Flujo actual

```text
Usuario
   │
   ▼
WhatsApp / comunicación directa
   │
   ▼
Analista IT
   │
   ├── Diagnóstico
   ├── Solución
   └── Seguimiento manual
```

---

## 3. Problemas identificados

El modelo actual presenta las siguientes dificultades:

* Solicitudes distribuidas principalmente mediante WhatsApp.
* Falta de un registro centralizado de incidentes y requerimientos.
* Dificultad para realizar seguimiento a solicitudes pendientes.
* Falta de clasificación y priorización formal.
* Ausencia de indicadores operativos de soporte.
* Dificultad para determinar tiempos de respuesta y solución.
* Dependencia de conversaciones individuales para consultar el historial de una solicitud.
* Posibilidad de que solicitudes importantes queden sin seguimiento.
* Dependencia ocasional de personal de otras áreas para atender requerimientos de soporte.

---

## 4. Tipos de solicitudes identificadas

Entre las solicitudes habituales se encuentran:

### Conectividad

* Sin acceso a Internet.
* Problemas de conexión a la red.
* Problemas de Wi-Fi.
* Problemas de acceso a servicios internos.

### Impresión y escaneo

* Impresoras que no imprimen.
* Problemas de conexión con impresoras.
* Errores de impresión.
* Problemas con escáneres.
* Instalación o configuración de dispositivos.

### Equipos

* Computadores con fallas.
* Problemas con periféricos.
* Configuración de estaciones de trabajo.
* Instalación de software.

### Cuentas y accesos

* Problemas de inicio de sesión.
* Bloqueo de cuentas.
* Restablecimiento de contraseñas.
* Solicitudes de permisos y acceso.

### Aplicaciones y servicios

* Problemas con aplicaciones corporativas.
* Microsoft 365.
* Outlook.
* Teams.
* Otros servicios utilizados por los usuarios.

---

## 5. Objetivo general

Implementar una mesa de servicios IT basada en osTicket que permita centralizar, clasificar, priorizar, asignar, atender y realizar seguimiento a las solicitudes de soporte tecnológico de la organización.

---

## 6. Objetivos específicos

* Centralizar las solicitudes de soporte mediante un sistema de tickets.
* Reducir progresivamente la dependencia de WhatsApp como canal principal de soporte.
* Establecer categorías y prioridades para los incidentes y requerimientos.
* Mantener un historial de cada solicitud atendida.
* Facilitar el seguimiento de solicitudes pendientes.
* Definir tiempos objetivo de atención y resolución.
* Generar indicadores para medir el desempeño del servicio de soporte.
* Identificar problemas recurrentes mediante el análisis de tickets.
* Mejorar la trazabilidad de las actividades realizadas por IT.
* Documentar el proceso de implementación y administración de la plataforma.

---

## 7. Alcance inicial

La primera fase del proyecto estará orientada a la implementación de una mesa de servicios para la atención de aproximadamente 220 usuarios.

El alcance inicial contempla:

* Instalación de osTicket.
* Implementación sobre Ubuntu Server 24.04.
* Configuración del servidor web y base de datos.
* Configuración de usuarios y agentes.
* Creación de departamentos.
* Creación de categorías de soporte.
* Configuración de prioridades.
* Configuración de SLA.
* Configuración de correo electrónico.
* Creación de plantillas de respuesta.
* Pruebas funcionales.
* Implementación piloto.
* Documentación técnica.
* Generación de indicadores de soporte.

---

## 8. Resultado esperado

Al finalizar la implementación se espera disponer de una plataforma centralizada que permita gestionar las solicitudes de soporte desde su creación hasta su cierre.

El flujo esperado será:

```text
Usuario
   │
   ▼
Solicitud de soporte
   │
   ▼
Creación del ticket
   │
   ▼
Clasificación
   │
   ▼
Priorización
   │
   ▼
Asignación
   │
   ▼
Diagnóstico y atención
   │
   ▼
Solución
   │
   ▼
Cierre
   │
   ▼
Registro histórico e indicadores
```

La implementación permitirá disponer de información que actualmente no se encuentra centralizada, como cantidad de tickets, categorías con mayor incidencia, tiempos de respuesta, tiempos de resolución y solicitudes pendientes.

---

## 9. Tecnologías

* Ubuntu Server 24.04 LTS
* osTicket
* Apache
* PHP
* MariaDB
* Git
* GitHub
* VMware ESXi
* HTTPS

---

## 10. Estado del proyecto

🟡 **En desarrollo — Fase de análisis y planificación**
