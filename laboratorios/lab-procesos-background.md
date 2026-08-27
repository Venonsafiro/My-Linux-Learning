# Día de práctica #24
08/21/2026 Jueves

## 1. Problema identificado
Al intentar ejecutar el script `./miscript.sh` en la terminal, el sistema arroja el error `-bash: ./miscript.sh: Permission denied`. Además, al intentar ejecutarlo desde la carpeta incorrecta arrojó `No such file or directory`.

## 2. Diagnóstico técnico
* Al revisar la estructura con `ls -l`, el archivo presentaba los permisos `-rw-r--r--`. Carecía de la letra `x` (ejecución) para el usuario.
* Se identificó que las instrucciones de control en Bash son sensibles a mayúsculas/minúsculas (*Case-Sensitive*); escribir `While` con "W" mayúscula invalida la orden del bucle.

## 3. Solución aplicada
* **Asignación de permisos:** Se ejecutó `chmod +x miscript.sh` para otorgar permisos de ejecución (cambiando a `-rwxr-xr-x` en verde).
* **Corrección de código:** Se reescribió el script asegurando la palabra clave en minúsculas (`while true; do echo "..."; sleep 3; done`).
* **Control de procesos:** Se puso a correr en segundo plano (`./miscript.sh &`), se identificó su PID asignado en memoria RAM (`633`) y se finalizó el proceso de forma limpia usando el comando `kill 633`.
