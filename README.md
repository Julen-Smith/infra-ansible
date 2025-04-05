# infra-ansible
Repositorio personal de orquestación para la infraestructura de mis labs.

Inventariado de maquinas

- 1x Ampere 4-OCPU 24GB como bastión.
- 3x Discord bots en los micro de GPC 
- x1 VPS 416200 Sin asignación de rol, posible redistribución lateral en servicios mas economicos
- 3x Aws micros

# vps controller changelog checklist

Seguridad basica del sistema

Bloqueo de usuarios root

Bloqueo de puertos

Fail2Ban

Algun monitor liviano o externalizar prometheus en otra maquina e internalizar senders.

Autoupdates

Configuración del kernel

Auditorias de sistema

Limitación de consultas a BBDD a localhost o host conocidos preautorizados y con certificados

Configuración de backups

# General para después de la arquitectura

- El servidor de secretos es el unico que se va a desplegar fuera del stack ansible.

- Solo aceptara conexiones desde la GPC o bien desde mi equipo personal. Tiene bloqueados cualquier intento por contraseña.