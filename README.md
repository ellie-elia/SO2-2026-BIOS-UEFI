# SO2-2026-BIOS-UEFI

Proyecto semestral de Sistemas Operativos sobre la personalización y estandarización de BIOS/UEFI para equipos de laboratorios universitarios.

## Problema

El documento del proyecto reporta que los equipos de los laboratorios de UNIFRANZ, sede Cochabamba, mantienen configuraciones BIOS/UEFI de fábrica. Describe riesgos relacionados con el arranque desde medios externos, la falta de contraseñas de administrador diferenciadas y el uso no aprovechado de Secure Boot.

## Objetivo

Diseñar e implementar una propuesta de personalización y estandarización del firmware BIOS/UEFI de los equipos del laboratorio universitario para mejorar la seguridad, gestión y control de la infraestructura.

## MVP

El MVP consiste en aplicar el perfil base BIOS/UEFI en QEMU/OVMF, verificar todos sus parámetros y generar un log del resultado. Consulta la [definición del MVP](docs/proyecto/mvp.md).

## Entregables previstos

- Diagnóstico del estado actual del firmware.
- Perfil base de parámetros BIOS/UEFI.
- Guion de despliegue automatizado.
- Mecanismo de respaldo y rollback.
- Pruebas en QEMU/OVMF y en equipos reales dados de baja, con medición frente al proceso manual.
- Manual técnico, informe final y checklist de calidad.

Los [criterios de éxito y aceptación](docs/proyecto/criterios-exito.md) describen los umbrales medibles y cómo se aceptará cada entregable.

## Fuera del alcance

- No se desarrollará un firmware UEFI desde cero.
- No se modificará el código fuente del firmware de los equipos.
- No se implementará gestión remota centralizada de firmware.
- No se cubrirán equipos fuera de los laboratorios de Ingeniería de Sistemas.
- EDK2 para el logo institucional es opcional y no forma parte del alcance obligatorio.

Consulta el [detalle del alcance](docs/proyecto/alcance.md). El rollback no forma parte del MVP, pero sí permanece como entregable previsto para el proyecto completo.

## Herramientas previstas

Ubuntu; QEMU con OVMF; VMware Workstation; herramientas de configuración de fabricantes como Dell Command | Configure (CCTK) y HP BIOS Configuration Utility (BCU); Git. EDK2 figura como componente opcional.

## Estado del proyecto al 21 de octubre de 2026

El informe de la segunda entrega, fechado el 7 de octubre de 2026, indicaba que seguían en curso la autorización institucional, el diagnóstico de los laboratorios y la preparación del entorno virtual. Las Issues #4–#7 recibieron comentarios de actualización el 21 de octubre, sin que el repositorio confirme los resultados de esas actividades.

Al 21 de octubre, las Issues [#2](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/2), [#3](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/3) y [#4](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/4) continúan abiertas para coordinar el estado y acuerdos, revisar la consistencia documental y confirmar el entorno técnico de pruebas. El repositorio no contiene una actualización posterior que confirme el resultado de la autorización, el diagnóstico o la disponibilidad final del entorno; esos estados deben confirmarse con el equipo.

Los riesgos identificados y las mitigaciones previstas están en [riesgos y acuerdos](gestion/riesgos-y-acuerdos.md).

## Integrantes

- Elia Solis Escobar — Scrum Master.
- Juan Manuel Chacon Villarroel — Documentación y control de calidad.
- Gabriel Ruben Oconor Aruquipa — Desarrollador técnico.

## Documentos del proyecto

- [Documento del proyecto](docs/proyecto/documento-proyecto-bios-uefi.pdf)
- [MVP](docs/proyecto/mvp.md)
- [Alcance y exclusiones](docs/proyecto/alcance.md)
- [Criterios de éxito y aceptación](docs/proyecto/criterios-exito.md)
- [Riesgos y acuerdos](gestion/riesgos-y-acuerdos.md)
- [Presentación del semestre](presentaciones/semestre/presentacion-bios-uefi-2026-10-07.pptx)
- [Cronograma Gantt transcrito](gestion/gantt/cronograma.csv)
- [Decisiones tecnológicas](docs/proyecto/decisiones-tecnologicas.md)
- [Dependencias del Gantt](gestion/gantt/dependencias-gantt.md)
- [Requisitos pendientes](docs/proyecto/requisitos-pendientes.md)
- [Auditoría de madurez](docs/proyecto/auditoria-madurez.md)
- [Equipo](gestion/equipo.md)
- [Contribuir](CONTRIBUTING.md)
