# 🐧 My-Linux-Learning-Journey

Registro diario de mi aprendizaje en Administración de Sistemas Linux y WSL.

---

## 📌 Índice de Contenidos

* 🚀 [Semana 1: Primeros Pasos en la Terminal de Linux (WSL)](#día-1-primeros-pasos-en-la-terminal-de-linux-wsl)
* 🏢 [Semana 2: Despliegue de Servidor de Empresa y Gestión de Archivos](#día-2-despliegue-de-servidor-de-empresa-y-gestión-de-archivos)
* 🔍 [Semana 3: Inspección Avanzada y Búsqueda de Archivos](#día-3-inspección-avanzada-y-búsqueda-de-archivos)

---

## 🐧 Semana 1: Primeros pasos en la Terminal de Linux (WSL)

**Fecha:** 14/07/2026 | **Tiempo dedicado:** 30 minutos

### 🎯 Objetivo del Día
Aprendí a instalar **Linux WSL2** (*Windows Subsystem for Linux*) y a navegar por la estructura del sistema de archivos mediante la consola de **Ubuntu**.

### 🛠️ Lección Aprendida
Vi cómo Linux puede correr en un sistema compartido con Windows y estar en su propio entorno usando la distribución de Ubuntu. Aprendí la navegación básica con `pwd`, `cd` y `ls`.

---

## 🏢 Semana 2: Despliegue de Servidor de Empresa y Gestión de Archivos

**Fecha:** 27/07/2026 | **Tiempo dedicado:** 60 minutos

### 🎯 Objetivo del Día
Crear una estructura de directorios simulando una empresa (`sistemas`, `contabilidad`, `recursos_humanos`), generar reportes internos y transferir/respaldar archivos usando `cp` y `mv`.

### 🛠️ Comandos Dominados
* `mkdir -p` para crear arquitecturas de carpetas en un solo paso.
* `cp` para duplicar y hacer respaldos de seguridad.
* `mv` para transferir archivos entre departamentos y renombrarlos.
* `ls -R` para auditar de forma recursiva toda la estructura.

---

## 🔍 Semana 3: Inspección Avanzada y Búsqueda de Archivos

**Fecha:** 31/07/2026 | **Tiempo dedicado:** 60 minutos

### 🎯 Objetivo del Día
Aprender a auditar e inspeccionar archivos de texto (*logs*) sin saturar la consola, además de rastrear y localizar archivos en la estructura del servidor mediante patrones de búsqueda.

### 🛠️ Comandos Dominados
* `wc -l`: Contar el número total de líneas en un archivo.
* `head -n X`: Leer las primeras **X** líneas de un archivo.
* `tail -n X`: Leer las últimas **X** líneas de un archivo.
* `find . -name "*.txt"`: Buscar archivos dentro del directorio actual (`.`) que coincidan con un patrón o extensión usando comodines (`*`).

### 💡 Lección Aprendida y Resolución de Problemas
* **Líneas finales en blanco:** Al ejecutar `tail -n 1`, si un archivo termina en un salto de línea, puede no mostrar texto visible; aumentar a `tail -n 2` permite ver la última línea con contenido real.
* **Sintaxis en `find`:** Para ejecutar búsquedas correctas, es imprescindible escribir el guion medio en `-name` e indicar el punto `.` como directorio raíz de búsqueda.

---

