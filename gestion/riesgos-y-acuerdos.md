# Riesgos y acuerdos

Registro de riesgos principales y del plan de continuidad del equipo. Las mitigaciones describen acciones previstas; no implican que los controles o mecanismos ya estén implementados.

## Riesgos principales

| Riesgo | Probabilidad | Impacto | Mitigación |
|---|---|---|---|
| No obtener autorización institucional para acceder a equipos de baja | Media | Alto | Realizar las pruebas en entornos virtuales (QEMU/OVMF, VMware). Si no se consiguen equipos reales, validar el proyecto completamente en virtual. |
| Incompatibilidad de la herramienta del fabricante con los equipos reales del laboratorio | Media | Alto | Identificar marca y modelo antes de desarrollar. Tener preparadas alternativas: CCTK para Dell, BCU para HP y AMI BIOS Configuration Tool para otros. |
| El script inutiliza un equipo durante las pruebas | Baja | Crítico | Implementar el mecanismo de rollback para respaldar la configuración original antes de aplicar cambios. Probar primero en virtual y después en equipos dados de baja; nunca en equipos en uso. |

## Plan de contingencia si un integrante no puede continuar

- **Si Gabriel (responsable técnico) no está disponible:** Elia asume las pruebas con la documentación técnica ya generada y Manuel apoya en scripting.
- **Si Elia (Scrum Master y líder) no está disponible:** Gabriel asume la coordinación y Manuel mantiene el seguimiento.
- **Si Manuel (documentación y control de calidad) no está disponible:** Elia asume la documentación y Gabriel realiza la revisión técnica.
