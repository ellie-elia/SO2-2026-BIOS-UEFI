# SO2-2026-BIOS-UEFI

Proyecto semestral de Sistemas Operativos sobre la personalización y estandarización de BIOS/UEFI para equipos de laboratorios universitarios.

## Problema

El documento del proyecto reporta que los equipos de los laboratorios de UNIFRANZ, sede Cochabamba, mantienen configuraciones BIOS/UEFI de fábrica. Describe riesgos relacionados con el arranque desde medios externos, la falta de contraseñas de administrador diferenciadas y el uso no aprovechado de Secure Boot.

## Objetivo

Diseñar e implementar una propuesta de personalización y estandarización del firmware BIOS/UEFI de los equipos del laboratorio universitario para mejorar la seguridad, gestión y control de la infraestructura.

## Entregables previstos

- Diagnóstico del estado actual del firmware.
- Perfil base de parámetros BIOS/UEFI.
- Guion de despliegue automatizado.
- Mecanismo de respaldo y rollback.
- Pruebas en QEMU/OVMF y en equipos reales dados de baja, con medición frente al proceso manual.
- Manual técnico, informe final y checklist de calidad.

## Herramientas previstas

Ubuntu; QEMU con OVMF; VMware Workstation; herramientas de configuración de fabricantes como Dell Command | Configure (CCTK) y HP BIOS Configuration Utility (BCU); Git. EDK2 figura como componente opcional.

## Estado reportado al 7 de octubre de 2026

Según el documento de la segunda entrega, se habían definido los roles, el problema, los objetivos, la selección tecnológica y el presupuesto, y existía un borrador del perfil base. Seguían en curso la autorización institucional, el diagnóstico de los laboratorios y la preparación del entorno virtual de pruebas. Este estado corresponde al informe de esa fecha.

## Integrantes

- Elia Solis Escobar — Scrum Master.
- Juan Manuel Chacon Villarroel — Documentacion y control de calidad.
- Gabriel Ruben Oconor Aruquipa — Desarrollador Tecnico.

## Documentos del proyecto

- [Documento del proyecto](docs/proyecto/documento-proyecto-bios-uefi.pdf)
- [Presentación del semestre](presentaciones/semestre/presentacion-bios-uefi-2026-10-07.pptx)
- [Cronograma Gantt transcrito](gestion/gantt/cronograma.csv)
- [Equipo](gestion/equipo.md)
- [Contribuir](CONTRIBUTING.md)
