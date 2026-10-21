# Justificación de decisiones tecnológicas

Este documento resume las razones que aparecen en la sección 4 del [documento del proyecto](documento-proyecto-bios-uefi.pdf). La fuente explica el propósito de las herramientas elegidas, pero no compara todas las alternativas solicitadas. Donde no hay comparación explícita, se deja constancia y no se atribuye una desventaja a la alternativa.

| Herramienta elegida | Alternativas consideradas | Razón de la elección según la sección 4 |
|---------------------|--------------------------|------------------------------------------|
| QEMU con OVMF | VirtualBox | QEMU/OVMF permite simular UEFI con mayor control por línea de comandos; la sección 4 identifica ese control como clave para desarrollar el guion de despliegue. La fuente no evalúa VirtualBox ni afirma que carezca de esas capacidades, por lo que no permite una comparación directa. |
| QEMU con OVMF | VMware Workstation | Se plantean como herramientas complementarias: QEMU/OVMF ofrece control por línea de comandos para automatizar; VMware ofrece una interfaz gráfica útil para configurar rápidamente el tipo de firmware y hacer demostraciones visuales. |
| VMware Workstation | Hyper-V | La fuente justifica VMware por su interfaz gráfica para configurar y demostrar BIOS/UEFI. No evalúa Hyper-V, así que el repositorio no aporta una razón comparativa para preferir VMware frente a Hyper-V. |
| Ubuntu | Otras distribuciones | La sección 4 elige Ubuntu porque permite instalar QEMU/OVMF desde sus repositorios centrales sin compilación manual ni ajustes técnicos intrincados. No contiene una comparación con distribuciones concretas. |
| Herramientas del fabricante, como Dell Command \\| Configure (CCTK) y HP BCU | Configuración manual desde la interfaz BIOS/UEFI | El documento plantea las utilidades del fabricante como el medio para aplicar configuraciones reales desde terminal y evitar entrar manualmente a la interfaz de firmware de cada equipo. La herramienta concreta depende del fabricante y modelo, todavía por identificar mediante el diagnóstico (Issue #6). |

## Límite de la justificación disponible

La sección 4 justifica el uso previsto de las herramientas principales, pero no documenta pruebas comparativas de VirtualBox, Hyper-V u otras distribuciones. Tampoco registra resultados experimentales que demuestren superioridad entre alternativas. Para afirmar esas comparaciones, el equipo tendría que investigarlas y documentar sus resultados; este archivo no las presupone.
