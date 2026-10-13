# Criterios de éxito y aceptación

Los siguientes umbrales son los criterios medibles definidos para evaluar el proyecto. El criterio del MVP se especifica por separado en [mvp.md](mvp.md).

## Criterios de éxito medibles

- El script configura correctamente al menos el 90 % de los equipos en el primer intento.
- El tiempo de despliegue automatizado es menor o igual al 30 % del tiempo del proceso manual.
- El rollback restaura la configuración original en el 100 % de los casos probados.
- Cada parámetro del perfil base queda verificado y registrado en un log auditable.

## Criterios de aceptación por entregable

| Entregable | Criterio de aceptación |
|---|---|
| Diagnóstico (estado «antes») | Documento con la configuración actual de al menos 3 equipos, con capturas o exports. |
| Perfil base | Tabla de parámetros aprobada y probada en al menos 1 equipo virtual. |
| Script de despliegue | Se ejecuta sin errores en QEMU/OVMF, configura todos los parámetros y genera un log. |
| Mecanismo de rollback | Restaura la configuración original en el 100 % de las pruebas. |
| Medición comparativa | Tabla con tiempos manuales frente a automatizados en al menos 3 ejecuciones. |

El resultado de cada criterio debe respaldarse con la documentación o evidencia de prueba correspondiente. Estos criterios no cambian la definición del MVP: el rollback, por ejemplo, es un entregable del proyecto completo y queda fuera del MVP.
