# Infraestructura del servidor

## 1. Objetivo

Se implementó una máquina virtual dedicada para alojar la plataforma de mesa de servicios osTicket.

La decisión de utilizar una VM independiente se tomó después de realizar una auditoría sobre una infraestructura existente, donde se identificaron servicios Docker, MariaDB, RustDesk y múltiples puertos en uso.

Con el fin de evitar conflictos y reducir el riesgo operativo, se decidió aislar osTicket en un servidor independiente.

## 2. Plataforma de virtualización

- Plataforma: VMware ESXi
- Máquina virtual: osticket

## 3. Sistema operativo

- Sistema operativo: Ubuntu Server
- Versión: Ubuntu 24.04.4 LTS
- Arquitectura: x86_64

## 4. Recursos asignados

| Recurso | Configuración |
|---|---|
| CPU | 2 vCPU |
| RAM | 4 GB |
| Disco | 60 GB |
| Almacenamiento | LVM |

## 5. Configuración de red

| Parámetro | Valor |
|---|---|
| Hostname | osticket |
| Dirección IP | 192.168.214.216/24 |
| Gateway | 192.168.214.254 |
| DNS | 192.168.214.254 |

## 6. Acceso administrativo

Se instaló y habilitó OpenSSH Server para permitir la administración remota del servidor.

El servicio SSH fue validado y se encuentra operativo.

## 7. Validación inicial

Se realizaron comprobaciones sobre:

- Versión del sistema operativo.
- Recursos de CPU y memoria.
- Capacidad de almacenamiento.
- Configuración IP.
- Gateway.
- Resolución DNS.
- Conectividad externa.
- Estado del servicio SSH.
- Puertos en escucha.

Las comprobaciones iniciales fueron satisfactorias.

## 8. Incidente durante la configuración de red

Durante la instalación inicial se detectó una configuración incorrecta de la ruta por defecto.

La configuración inicial utilizaba:

`255.255.255.0`

como gateway.

Se corrigió utilizando el gateway correspondiente a la red:

`192.168.214.254`

Posteriormente se validó la conectividad mediante pruebas ICMP y resolución DNS.

## 9. Decisión de aislamiento

No se utilizó el servidor existente de inventario debido a que ya alojaba múltiples servicios.

Se creó una VM independiente para:

- Reducir conflictos de puertos.
- Aislar la aplicación.
- Facilitar mantenimiento.
- Facilitar backups.
- Permitir pruebas y recuperación.
- Reducir el impacto sobre servicios existentes.

## 10. Estado

Servidor preparado para comenzar el despliegue de la plataforma osTicket.

## 11. Despliegue del servidor web

Se instaló Apache2 sobre Ubuntu Server 24.04.4 LTS.

### Verificación del servicio

El servicio Apache fue validado mediante:

```bash
sudo systemctl status apache2 --no-pager

## 12. Instalación y validación de PHP

Se instaló PHP 8.3 utilizando los repositorios oficiales de Ubuntu 24.04.

Paquetes principales instalados:

- PHP 8.3
- PHP 8.3 CLI
- libapache2-mod-php8.3

La integración entre Apache y PHP fue validada mediante una página temporal `phpinfo()` accesible desde la red interna.

La prueba confirmó que Apache puede procesar archivos PHP correctamente.

Después de la validación, el archivo de diagnóstico fue eliminado para evitar exponer información del entorno del servidor.

### Resultado

PHP 8.3 quedó instalado y funcionando correctamente con Apache
