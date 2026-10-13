# Auditoría de madurez del proyecto

**Fecha de evaluación:** 13 de octubre de 2026  
**Fuente de evaluación:** información disponible en este repositorio, incluida la documentación, el Gantt y las Issues abiertas.

## Criterio de evaluación

- **CUMPLIDO:** el repositorio contiene una respuesta y evidencia suficiente para la pregunta. Esto no significa que un trabajo futuro ya se haya ejecutado.
- **PARCIAL:** hay una definición o evidencia inicial, pero falta detalle, validación o confirmación.
- **PENDIENTE:** el repositorio no contiene evidencia suficiente para responder.

Las metas de éxito documentadas son criterios de evaluación, no resultados medidos. Las Issues abiertas identifican trabajo pendiente y no se consideran evidencia de que ese trabajo ya se completó.

## 1. Problema y valor

### 1. ¿Pueden explicar el problema en menos de 30 segundos sin mencionar ninguna tecnología?

**Estado: PARCIAL.** El repositorio permite resumir que las configuraciones actuales de los laboratorios dejan riesgos de seguridad y control, pero no contiene una explicación breve aprobada que evite términos tecnológicos. [README: Problema](../../README.md#problema)

### 2. ¿Quién tiene el problema y quién utilizará la solución?

**Estado: PARCIAL.** El problema se sitúa en los laboratorios de UNIFRANZ, sede Cochabamba. El repositorio no identifica de forma concreta a las personas usuarias de la solución ni valida sus necesidades. [README](../../README.md), [documento del proyecto](documento-proyecto-bios-uefi.pdf)

### 3. ¿Qué evidencia demuestra que el problema es real, relevante o necesario?

**Estado: PARCIAL.** El documento del proyecto reporta configuraciones de fábrica y riesgos, pero el diagnóstico del estado «antes» sigue como trabajo planificado. La Issue [#6](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/6) pide documentar al menos tres equipos con capturas o exports.

### 4. ¿Qué consecuencias tiene actualmente ese problema?

**Estado: PARCIAL.** El README identifica riesgos relacionados con el arranque desde medios externos, las contraseñas de administrador diferenciadas y el uso de Secure Boot. No hay evidencia de incidentes o mediciones de impacto actual. [README: Problema](../../README.md#problema)

### 5. ¿Qué valor concreto aportará su solución al usuario?

**Estado: PARCIAL.** El objetivo plantea mejorar la seguridad, la gestión y el control de la infraestructura; el beneficio concreto para personas usuarias no está medido ni validado con ellas. [README: Objetivo](../../README.md#objetivo)

### 6. ¿Pueden explicar claramente por qué su solución es una respuesta adecuada al problema y no simplemente una aplicación interesante?

**Estado: PARCIAL.** La propuesta relaciona el problema reportado con la estandarización del perfil BIOS/UEFI, su despliegue y su verificación. El repositorio aún no contiene validación con usuarios ni resultados que demuestren el efecto de la propuesta. [README](../../README.md), [MVP](mvp.md)

## 2. Objetivos y éxito

### 7. ¿El objetivo general describe un resultado concreto que puede comprobarse?

**Estado: PARCIAL.** El objetivo general plantea diseñar e implementar una propuesta de personalización y estandarización. Hay criterios medibles para los entregables, pero todavía no se registran resultados de ejecución. [README: Objetivo](../../README.md#objetivo), [criterios de éxito](criterios-exito.md)

### 8. ¿Los objetivos específicos permiten dividir y comprobar el avance hacia ese resultado?

**Estado: PARCIAL.** El Gantt desglosa diagnóstico, diseño, desarrollo, pruebas y cierre en actividades con fechas. Faltan dependencias explícitas y algunos criterios de término de tarea se añadieron en Issues. [Gantt](../../gestion/gantt/cronograma.csv)

### 9. ¿Existe una relación clara entre problema → objetivos → solución → resultados esperados?

**Estado: PARCIAL.** El README conecta riesgos de configuración con el objetivo de estandarizar y con entregables como perfil, guion y pruebas. La relación con necesidades validadas y resultados observados todavía no está demostrada. [README](../../README.md), [criterios de éxito](criterios-exito.md)

### 10. ¿Cómo sabrán al final del proyecto que realmente tuvieron éxito?

**Estado: PARCIAL.** Se definieron metas de despliegue, tiempo, rollback y verificación auditable, además de criterios por entregable. Aún no hay mediciones que demuestren que se alcanzaron. [Criterios de éxito y aceptación](criterios-exito.md)

## 3. Usuarios y requisitos

### 11. ¿Los usuarios y sus necesidades están suficientemente definidos para determinar qué debe hacer el sistema?

**Estado: PARCIAL.** Está identificado el contexto de laboratorios, pero no se documentan perfiles de usuario, necesidades validadas ni requisitos derivados de consultas. [README](../../README.md), [equipo](../../gestion/equipo.md)

### 12. ¿Las funcionalidades principales están directamente relacionadas con necesidades reales de los usuarios?

**Estado: PARCIAL.** Perfil base, despliegue, verificación y log responden al objetivo de estandarización y control, pero la relación con necesidades de usuarios no se ha validado en el repositorio. [MVP](mvp.md), [README](../../README.md#objetivo)

### 13. ¿Las funcionalidades principales están suficientemente descritas para que otro integrante pueda comenzar a desarrollarlas sin tener que adivinar qué deben hacer?

**Estado: PARCIAL.** El MVP define el resultado esperado; aún falta la lógica técnica detallada del script, el formato del perfil y el diseño de rollback. La Issue [#8](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/8) cubre el diseño pendiente.

### 14. ¿Cada funcionalidad principal tiene criterios de aceptación verificables?

**Estado: PARCIAL.** Hay criterios de aceptación para cinco entregables principales y para el MVP. No se documentan criterios individuales para cada función o parámetro del perfil. [Criterios de éxito](criterios-exito.md), [MVP](mvp.md)

### 15. ¿Existen requisitos de calidad además de las funcionalidades, como seguridad, rendimiento, disponibilidad, facilidad de uso o compatibilidad, cuando sean relevantes?

**Estado: PARCIAL.** Se definieron metas sobre tasa de éxito, tiempo, rollback y logs; los riesgos identifican autorización, compatibilidad de herramientas y protección de equipos. No hay requisitos documentados para todos los atributos de calidad pertinentes ni resultados de validación. [Criterios de éxito](criterios-exito.md), [riesgos y acuerdos](../../gestion/riesgos-y-acuerdos.md)

## 4. Alcance

### 16. ¿Está claramente definido qué desarrollará el equipo?

**Estado: CUMPLIDO.** El README enumera entregables y el documento del MVP delimita el producto mínimo: perfil base, script, verificación y log en QEMU/OVMF. [README](../../README.md#entregables-previstos), [MVP](mvp.md)

### 17. ¿Está claramente definido qué NO desarrollará?

**Estado: CUMPLIDO.** El alcance excluye crear firmware desde cero, modificar su código fuente, gestión remota centralizada, equipos fuera de los laboratorios de Ingeniería de Sistemas y hace opcional EDK2. [Alcance](alcance.md), [README](../../README.md#fuera-del-alcance)

### 18. ¿Han identificado funcionalidades que podrían parecer interesantes pero que no son necesarias para cumplir el objetivo?

**Estado: CUMPLIDO.** EDK2 para el logo institucional está identificado como opcional y fuera del alcance obligatorio; también está separado de las exclusiones propias del MVP. [Alcance](alcance.md), [MVP](mvp.md)

### 19. ¿El alcance es realista considerando el tiempo, conocimientos y recursos disponibles?

**Estado: PARCIAL.** El Gantt distribuye el trabajo hasta la defensa del 16 de diciembre de 2026, pero el repositorio no contiene estimaciones de esfuerzo ni confirmación final de autorizaciones y entorno. [Gantt](../../gestion/gantt/cronograma.csv), Issues [#4](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/4) y [#5](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/5)

### 20. Si tuvieran que reducir el proyecto un 40%, ¿qué conservarían y qué eliminarían?

**Estado: PARCIAL.** La definición del MVP prioriza la aplicación y verificación del perfil en virtual; no hay una decisión documentada que compare explícitamente una reducción del 40 % ni qué entregables completos se recortarían. [MVP](mvp.md), [alcance](alcance.md)

## 5. MVP

### 21. ¿Existe una primera versión funcional claramente definida?

**Estado: CUMPLIDO.** Está definido un script que aplica el perfil base en QEMU/OVMF, verifica cada parámetro y genera un log. La implementación aún está pendiente. [MVP](mvp.md)

### 22. ¿El MVP resuelve una parte real del problema y entrega valor al usuario?

**Estado: PARCIAL.** El MVP permite probar la estandarización y verificación del perfil en un entorno virtual. El repositorio no demuestra todavía el valor para usuarios de los laboratorios ni una aplicación en su entorno real. [MVP](mvp.md), Issue [#11](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/11)

### 23. ¿El MVP puede estar terminado dentro del tiempo disponible?

**Estado: PARCIAL.** El Gantt programa el desarrollo del guion del 26 de octubre al 22 de noviembre y las pruebas virtuales hasta el 29 de noviembre. No hay estimación de esfuerzo ni validación del entorno que permita confirmar la viabilidad temporal. [Gantt](../../gestion/gantt/cronograma.csv), Issues [#4](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/4) y [#9](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/9)

### 24. ¿Las funcionalidades posteriores están claramente separadas del MVP?

**Estado: CUMPLIDO.** El rollback, las pruebas físicas, EDK2, capacitación y manual técnico están fuera del MVP; algunos continúan como entregables del proyecto completo. [MVP](mvp.md), [alcance](alcance.md), [README](../../README.md#entregables-previstos)

## 6. Diseño y viabilidad técnica

### 25. ¿La solución propuesta es técnicamente viable con las tecnologías, conocimientos y recursos que tiene el equipo?

**Estado: PARCIAL.** El repositorio enumera Ubuntu, QEMU/OVMF, VMware y herramientas de fabricantes, pero el entorno de pruebas y su disponibilidad aún requieren confirmación. [README: Herramientas previstas](../../README.md#herramientas-previstas), Issue [#4](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/4)

### 26. ¿Han identificado las partes técnicamente más difíciles o inciertas del proyecto?

**Estado: CUMPLIDO.** Se identifican compatibilidad de herramientas, autorización para acceder a equipos y el riesgo de inutilizar un equipo durante las pruebas. El diseño de despliegue y rollback sigue pendiente. [Riesgos y acuerdos](../../gestion/riesgos-y-acuerdos.md), Issue [#8](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/8)

### 27. ¿Han validado, o tienen previsto validar antes de depender de ellas, las tecnologías o integraciones críticas?

**Estado: PARCIAL.** El Gantt prevé preparar y probar el entorno virtual antes del desarrollo; las Issues piden confirmar el entorno y ejecutar pruebas. El repositorio todavía no aporta resultados de esas validaciones. [Gantt](../../gestion/gantt/cronograma.csv), Issues [#4](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/4) y [#11](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/11)

### 28. ¿Las principales decisiones tecnológicas tienen una justificación relacionada con las necesidades del proyecto?

**Estado: PENDIENTE.** Se enumeran herramientas previstas, pero no se documenta la justificación comparativa para seleccionarlas. [README: Herramientas previstas](../../README.md#herramientas-previstas)

### 29. ¿Han identificado las dependencias externas necesarias para construir y ejecutar el sistema?

**Estado: PARCIAL.** Se enumeran entornos virtuales, herramientas de fabricante y la necesidad de autorización y equipos de prueba. No se documentan aún versiones, requisitos de instalación ni dependencias completas del sistema. [README](../../README.md#herramientas-previstas), [riesgos y acuerdos](../../gestion/riesgos-y-acuerdos.md), Issue [#5](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/5)

### 30. ¿La solución tiene una estructura técnica inicial suficientemente clara para comenzar el desarrollo?

**Estado: PARCIAL.** El repositorio tiene carpetas para código y pruebas, y un MVP definido; los README de código y pruebas indican que el contenido se agregará posteriormente. La arquitectura y el diseño técnico siguen vacíos. [src/README](../../src/README.md), [tests/README](../../tests/README.md), [MVP](mvp.md), [docs](../../docs/)

## 7. Datos, seguridad y calidad

### 31. ¿Han identificado qué información manejará el sistema y de dónde provendrá?

**Estado: PARCIAL.** Los entregables implican un perfil de parámetros, configuración actual y logs de resultados. El repositorio aún no especifica el formato de esos datos ni su fuente concreta para cada equipo. [Criterios de éxito](criterios-exito.md), Issue [#6](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/6)

### 32. ¿Han identificado restricciones importantes relacionadas con datos, privacidad, seguridad, permisos o acceso?

**Estado: PARCIAL.** Se reconoce que se requiere autorización institucional y que las pruebas físicas serán en equipos dados de baja, nunca en equipos en uso. No se detallan restricciones de privacidad o manejo de logs. [Riesgos y acuerdos](../../gestion/riesgos-y-acuerdos.md), Issues [#5](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/5) y [#12](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/12)

### 33. ¿Han definido cómo comprobarán que las funcionalidades principales funcionan correctamente?

**Estado: PARCIAL.** Hay criterios de aceptación sobre aplicar y verificar todos los parámetros, restaurar la configuración y generar logs. Falta evidencia de ejecución y un caso de prueba detallado por parámetro. [Criterios de éxito](criterios-exito.md), [MVP](mvp.md)

### 34. ¿Existe una estrategia inicial de pruebas que acompañará el desarrollo?

**Estado: PARCIAL.** El Gantt contempla pruebas virtuales y en equipos dados de baja, y existen carpetas para pruebas unitarias, de integración y de sistema. Todavía no hay casos, datos de prueba ni resultados registrados. [Gantt](../../gestion/gantt/cronograma.csv), [tests/README](../../tests/README.md), Issues [#11](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/11) y [#12](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/12)

## 8. Plan de desarrollo

### 35. ¿El Gantt está compuesto por tareas concretas que realmente habrá que ejecutar?

**Estado: CUMPLIDO.** El Gantt contiene 20 hitos, actividades y tareas continuas que cubren planificación, análisis, diseño, desarrollo, pruebas y cierre. [Cronograma Gantt](../../gestion/gantt/cronograma.csv)

### 36. ¿Cada tarea tiene responsable?

**Estado: PARCIAL.** Las actividades indican responsables, pero algunas filas usan «Todos» y no nombran a cada persona. Las Issues #5–#15 sí están asignadas a cuentas individuales. [Gantt](../../gestion/gantt/cronograma.csv), Issues [#5–#15](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues)

### 37. ¿Las tareas tienen estimaciones razonables?

**Estado: PARCIAL.** El Gantt proporciona fechas de inicio y fin, pero no estimaciones de esfuerzo, capacidad ni la justificación de las duraciones. [Gantt](../../gestion/gantt/cronograma.csv)

### 38. ¿Las dependencias entre tareas están identificadas?

**Estado: PENDIENTE.** El cronograma ordena actividades por fechas, pero no declara relaciones o bloqueos entre tareas. [Gantt](../../gestion/gantt/cronograma.csv)

### 39. ¿El Gantt contempla desarrollo, integración, pruebas, correcciones y documentación?

**Estado: PARCIAL.** El Gantt sí contempla desarrollo, pruebas y documentación, pero no presenta tareas explícitas de integración y corrección. [Gantt](../../gestion/gantt/cronograma.csv)

### 40. ¿Han identificado qué tareas podrían bloquear al resto del equipo?

**Estado: CUMPLIDO.** El repositorio identifica autorización, disponibilidad del entorno, definición del perfil y compatibilidad de herramientas como asuntos que deben confirmarse antes de avanzar. [Riesgos y acuerdos](../../gestion/riesgos-y-acuerdos.md), Issues [#4](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/4), [#5](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/5), [#7](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/7)

## 9. Equipo y riesgos

### 41. ¿Cada integrante tiene una responsabilidad concreta y verificable?

**Estado: CUMPLIDO.** El repositorio identifica a Elia Solis Escobar como Scrum Master, a Juan Manuel Chacon Villarroel en documentación y control de calidad, y a Gabriel Ruben Oconor Aruquipa como desarrollador técnico. Las Issues de trabajo tienen responsables asignados. [Equipo](../../gestion/equipo.md), Issues [#5–#15](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues)

### 42. ¿El equipo tiene un mecanismo acordado para revisar e integrar el trabajo?

**Estado: PARCIAL.** Existe un archivo de contribución, pero solo declara su propósito; no describe ramas, revisiones, integración o criterios de aprobación. El historial muestra un PR combinado, que no constituye por sí solo un procedimiento acordado. [CONTRIBUTING.md](../../CONTRIBUTING.md), [PR #1](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/pull/1)

### 43. ¿Cuáles son los tres riesgos que más podrían hacer fracasar o retrasar el proyecto?

**Estado: CUMPLIDO.** Se registraron tres riesgos: no obtener autorización, incompatibilidad de la herramienta del fabricante y que el script inutilice un equipo durante pruebas. [Riesgos y acuerdos](../../gestion/riesgos-y-acuerdos.md)

### 44. ¿Cada uno de esos riesgos tiene una estrategia de mitigación?

**Estado: CUMPLIDO.** La tabla asigna una mitigación a cada riesgo. Son acciones previstas; la implementación y eficacia de esas mitigaciones aún deben verificarse. [Riesgos y acuerdos](../../gestion/riesgos-y-acuerdos.md)

### 45. ¿Qué harían si una persona clave del equipo deja de estar disponible?

**Estado: CUMPLIDO.** El documento define la reasignación de coordinación, pruebas, scripting, documentación y revisión técnica para la indisponibilidad de cada integrante. [Plan de contingencia](../../gestion/riesgos-y-acuerdos.md#plan-de-contingencia-si-un-integrante-no-puede-continuar), [equipo](../../gestion/equipo.md)

## 10. Preparación para desarrollar

### 46. ¿Existe actualmente alguna decisión fundamental que todavía no hayan tomado y que pueda bloquear el inicio del desarrollo?

**Estado: CUMPLIDO.** Sí. Siguen abiertas las tareas de confirmar autorización y entorno, terminar el perfil base y diseñar la lógica de despliegue y rollback. [Issues #4](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/4), [#5](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/5), [#7](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/7) y [#8](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/8)

### 47. ¿Existe algún requisito importante que todavía no comprendan suficientemente?

**Estado: PENDIENTE.** El repositorio no contiene una lista de requisitos incomprendidos ni una validación de necesidades con usuarios; no permite confirmar qué requisitos entienden suficientemente. [README](../../README.md), [equipo](../../gestion/equipo.md)

### 48. ¿Existe alguna dependencia técnica, información, permiso, acceso, herramienta o recurso que todavía no tengan y que sea necesario para comenzar?

**Estado: CUMPLIDO.** El repositorio identifica asuntos cuya disponibilidad debe confirmarse: autorización institucional y entorno técnico de pruebas. No afirma que esos recursos estén definitivamente ausentes. Issues [#4](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/4) y [#5](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/5)

### 49. Si mañana tuvieran que comenzar a programar, ¿cada integrante sabría exactamente qué debe construir primero?

**Estado: PARCIAL.** Las Issues asignan tareas y el MVP define el resultado, pero el perfil final y el diseño de la lógica todavía están pendientes; por eso no hay especificación suficiente para comenzar todas las partes sin decisiones adicionales. [MVP](mvp.md), Issues [#7](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/7), [#8](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/8) y [#9](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/9)

### 50. Si un nuevo integrante entrara mañana y solo revisara el repositorio, ¿podría comprender qué problema están resolviendo, qué van a construir, cuál es el MVP y qué trabajo debe realizarse a continuación?

**Estado: PARCIAL.** El README, el MVP, el alcance, el Gantt y las Issues explican el problema, el producto y el trabajo siguiente. La definición de usuarios, el estado confirmado de autorización y entorno y varios detalles técnicos siguen pendientes. [README](../../README.md), [MVP](mvp.md), [Gantt](../../gestion/gantt/cronograma.csv), Issues [#4](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/4)–[#15](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/15)

## 11. Prueba de fracaso

### 51. ¿Qué tendría que ser cierto para que este proyecto fracase?

**Estado: CUMPLIDO.** Los riesgos documentados describen condiciones de fracaso o retraso: falta de autorización sin alternativa virtual, incompatibilidad sin herramienta viable o daño a un equipo durante pruebas. [Riesgos y acuerdos](../../gestion/riesgos-y-acuerdos.md)

### 52. ¿Ya tienen una estrategia para evitar o controlar cada una de esas condiciones?

**Estado: PARCIAL.** Cada riesgo tiene mitigación y existe un plan de contingencia del equipo. Aún falta ejecutar y verificar las mitigaciones, incluido implementar y probar el rollback. [Riesgos y acuerdos](../../gestion/riesgos-y-acuerdos.md), Issue [#10](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/10)

## Acciones correctivas

Las acciones marcadas **IMPLEMENTADA** describen cambios de documentación o seguimiento ya realizados en el repositorio. La creación de una Issue deja registrada una tarea, pero no significa que su trabajo técnico esté terminado.

| Problema detectado | Acción correctiva | Responsable | Evidencia |
|---|---|---|---|
| **IMPLEMENTADA:** MVP no delimitado. | Definir el MVP, sus inclusiones, exclusiones y criterio de éxito. | Juan Manuel Chacon Villarroel | [mvp.md](mvp.md) |
| **IMPLEMENTADA:** exclusiones del proyecto no estaban consolidadas. | Documentar explícitamente el trabajo fuera del alcance y distinguirlo de lo excluido solo del MVP. | Juan Manuel Chacon Villarroel | [alcance.md](alcance.md) |
| **IMPLEMENTADA:** criterios de éxito y aceptación no estaban consolidados. | Registrar las metas medibles y criterios de aceptación por entregable. | Juan Manuel Chacon Villarroel | [criterios-exito.md](criterios-exito.md) |
| **IMPLEMENTADA:** riesgos y continuidad no estaban documentados como tabla y plan. | Registrar los tres riesgos, mitigaciones previstas y plan para la indisponibilidad de integrantes. | Elia Solis Escobar | [riesgos-y-acuerdos.md](../../gestion/riesgos-y-acuerdos.md) |
| **IMPLEMENTADA:** faltaba convertir trabajo del Gantt en tareas rastreables. | Crear y asignar las Issues #5–#15 con criterios de cierre y referencia a fase, actividad y fechas del Gantt. Las tareas técnicas de esas Issues continúan abiertas. | Elia Solis Escobar | [#5](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/5), [#6](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/6), [#7](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/7), [#8](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/8), [#9](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/9), [#10](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/10), [#11](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/11), [#12](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/12), [#13](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/13), [#14](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/14), [#15](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/15) |
| **PENDIENTE:** autorización institucional sin resultado actualizado en el repositorio. | Confirmar y registrar el resultado antes de planificar pruebas físicas. | Elia Solis Escobar | [Issue #5](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/5) |
| **PENDIENTE:** falta diagnóstico con datos de equipos. | Documentar configuración actual de al menos tres equipos con capturas o exports, si el acceso autorizado lo permite. | Gabriel Ruben Oconor Aruquipa | [Issue #6](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/6) |
| **PENDIENTE:** perfil y diseño técnico aún no están finalizados. | Acordar el perfil base y documentar la lógica de despliegue y rollback antes de implementar. | Gabriel Ruben Oconor Aruquipa; Elia Solis Escobar | [Issues #7](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/7) y [#8](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/8) |
| **PENDIENTE:** disponibilidad y compatibilidad del entorno/herramientas no están verificadas. | Registrar el entorno real de pruebas, identificar los equipos y validar las herramientas previstas antes de depender de ellas. | Gabriel Ruben Oconor Aruquipa | [Issues #4](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/4) y [#11](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/11) |
| **PENDIENTE:** faltan implementación y resultados de pruebas. | Implementar despliegue y rollback; ejecutar pruebas virtuales y, si hay autorización y equipos dados de baja disponibles, pruebas físicas; conservar logs y evidencias. | Gabriel Ruben Oconor Aruquipa; Juan Manuel Chacon Villarroel | [Issues #9](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/9)–[#12](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/12) |
| **PENDIENTE:** metas de éxito todavía no tienen mediciones. | Medir tasa de éxito y tiempo frente al proceso manual en al menos tres ejecuciones y reportar los resultados observados. | Juan Manuel Chacon Villarroel | [Issue #13](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/13), [criterios de éxito](criterios-exito.md) |
| **PENDIENTE:** usuarios, requisitos detallados, dependencias y criterios de calidad requieren más evidencia. | Documentar necesidades y requisitos confirmados, fuentes de datos, restricciones de acceso y criterios por función; enlazar cada decisión con evidencia. | Elia Solis Escobar; Gabriel Ruben Oconor Aruquipa; Juan Manuel Chacon Villarroel | [README](../../README.md), [equipo](../../gestion/equipo.md), [Issue #2](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/2) |
| **PENDIENTE:** el plan no explicita dependencias, estimaciones de esfuerzo, integración ni correcciones. | Revisar el Gantt y añadir dependencias y tareas de integración/corrección con responsables individuales y fechas acordadas. | Juan Manuel Chacon Villarroel; Elia Solis Escobar | [Gantt](../../gestion/gantt/cronograma.csv), [Issue #3](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/3) |
| **PENDIENTE:** falta un procedimiento de colaboración detallado. | Documentar el flujo de ramas, revisión e integración en CONTRIBUTING.md. | Juan Manuel Chacon Villarroel | [CONTRIBUTING.md](../../CONTRIBUTING.md), [Issue #3](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/3) |
| **PENDIENTE:** faltan entregables finales y ensayo de defensa. | Preparar manual, informe, checklist y ensayo usando únicamente resultados y evidencias confirmados. | Juan Manuel Chacon Villarroel; Elia Solis Escobar; Gabriel Ruben Oconor Aruquipa | [Issues #14](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/14) y [#15](https://github.com/ellie-elia/SO2-2026-BIOS-UEFI/issues/15) |
