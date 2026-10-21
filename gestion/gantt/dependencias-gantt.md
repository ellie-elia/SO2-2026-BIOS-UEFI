# Dependencias entre actividades del Gantt

Las relaciones siguientes hacen explícito el orden de entradas y resultados necesario para las 20 actividades del [cronograma original](cronograma.csv). Se basan en el alcance, el flujo del MVP, el orden del Gantt y los riesgos ya documentados; no cambian sus fechas. Cuando el cronograma no identifica una dependencia, se indica como tal en vez de inventar una.

| Actividad | Depende de | Motivo |
|-----------|-----------|--------|
| 1. Desarrollar la estructura inicial del proyecto semestral | Sin dependencia previa identificada | Es el hito inicial del cronograma. |
| 2. Revisar la estructura inicial y ajustar alcance y objetivos | 1 | Se revisa y ajusta la estructura inicial ya elaborada. |
| 3. Gestionar autorización institucional para equipos de baja y laboratorio | Sin dependencia previa identificada; debe gestionarse tempranamente | El proyecto indica gestionar el permiso desde el inicio. La autorización es requisito para las pruebas físicas. |
| 4. Investigar BIOS/UEFI, Secure Boot y herramientas | Sin dependencia previa identificada | Es una actividad de análisis que puede realizarse en paralelo con la gestión del permiso. Sus resultados alimentan el diseño técnico. |
| 5. Diagnosticar el firmware actual de los laboratorios (estado “antes”) | 3; resultados de 4 como referencia técnica | El acceso a equipos requiere autorización. La investigación ayuda a interpretar los parámetros observados. |
| 6. Preparar documento mejorado, Gantt y presentación (2.ª entrega) | 2 y 4 | Integra el alcance y objetivos ajustados, y la investigación técnica prevista para la segunda entrega. |
| 7. Preparar entorno de pruebas (Ubuntu, QEMU/OVMF, VMware) | 4 | La selección e instalación del entorno se apoya en la investigación de herramientas y firmware. |
| 8. Diseñar esquema de parámetros base BIOS/UEFI | 4 y resultados disponibles de 5 | El perfil se apoya en la investigación y debe ajustarse a los modelos y configuración observados en el diagnóstico. Puede avanzar mientras el diagnóstico se completa, revisando sus resultados. |
| 9. Diseñar lógica del guion y del rollback | 8 | La lógica de despliegue debe aplicar y verificar el perfil; el rollback debe responder a fallos de verificación. |
| 10. Desarrollar guion de despliegue automatizado | 7, 8 y 9 | Requiere un entorno donde probar, un perfil definido y una lógica de despliegue acordada. |
| 11. Desarrollar mecanismo de respaldo y rollback | 9 y 10 | Implementa el flujo de respaldo y reversión diseñado y debe integrarse con el guion de despliegue. |
| 12. Personalización opcional con EDK2 (logo institucional) | Sin dependencia obligatoria identificada | El documento del proyecto la considera opcional y fuera del alcance obligatorio; no bloquea el MVP ni los demás entregables. |
| 13. Probar en QEMU/OVMF y VMware | 7 y una versión ejecutable de 10; 11 para validar rollback | Las pruebas requieren el entorno preparado y el guion. La verificación del rollback requiere que su mecanismo esté implementado. |
| 14. Probar en equipos reales dados de baja | 3, 5, 10, 11 y pruebas virtuales iniciales de 13 | Requiere permiso, conocer los equipos y tener el guion y el rollback. El plan de riesgos establece probar primero en virtual antes de intervenir equipos físicos. |
| 15. Medir tiempo y tasa de éxito frente al proceso manual | 10 y resultados de 13 y 14 | La comparación requiere ejecuciones del guion y resultados de pruebas; el informe debe indicar qué entorno y ejecuciones se midieron. |
| 16. Preparar manual técnico, informe final y checklist de calidad | Resultados de 5 y 13–15; entregables de 10 y 11 | La documentación final debe describir el diagnóstico, la implementación, los resultados y la evidencia realmente obtenidos. |
| 17. Capacitar al personal y entregar el guion | 10 y material operativo disponible de 16 | La capacitación y entrega requieren un guion validado y sus instrucciones de operación. |
| 18. Preparar y ensayar la defensa | Resultados de 13–15 y material de 16 | La defensa debe basarse en resultados y evidencias confirmados y coherentes con el informe. |
| 19. Realizar defensa final del proyecto | 18 | El ensayo y preparación preceden a la defensa final. |
| 20. Realizar reuniones semanales de seguimiento Scrum | Sin dependencia previa; actividad transversal | Es una actividad continua que acompaña el seguimiento y los ajustes del resto del plan. |

## Condiciones para las pruebas físicas

La actividad 13 del Gantt corresponde a pruebas virtuales; no sustituye la autorización institucional (actividad 3) ni las pruebas físicas de la actividad 14. Si no se confirma el acceso a equipos reales, el repositorio debe registrar esa situación y aplicar la alternativa virtual prevista en los riesgos del proyecto, sin presentar pruebas físicas como realizadas.
