# MVP: aplicación del perfil base BIOS/UEFI

## Definición

Script que aplica el perfil base de BIOS/UEFI a un equipo virtual en QEMU/OVMF, verifica que cada parámetro quedó correctamente configurado y genera un log con el resultado.

## Qué incluye

- Perfil base de parámetros BIOS/UEFI.
- Script de despliegue del perfil.
- Verificación de cada parámetro.
- Log auditable con el resultado.

## Qué no incluye el MVP

- Rollback automatizado.
- Pruebas en hardware real.
- Personalización con EDK2.
- Capacitación.
- Manual técnico.

Estos elementos pueden formar parte de entregables del proyecto completo, pero no son necesarios para considerar terminado el MVP.

## Criterio de éxito del MVP

El script configura correctamente el 100 % de los parámetros del perfil base en el entorno virtual QEMU/OVMF y deja evidencia verificable en el log.
