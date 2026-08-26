# Bitácora de Inspección de Red Linux

**Herramienta:** WSL2 (Ubuntu)
**Estado General:** OPERATIVO (Conectividad total)

---

### 1. Interfaz e IP Privada
* **Comando:** `ip a`
* **Interfaz:** `eth0` | **Estado:** `UP`
* **IP Privada:** `172.19.92.146/20`
* **MAC:** `00:15:5d:76:69:87` (Microsoft Hyper-V)

### 2. Puerta de Enlace (Default Gateway)
* **Comando:** `ip route`
* **Gateway IP:** `172.19.80.1` (Ruta asignada en eth0)

### 3. Prueba de Conectividad ICMP
* **Comando:** `ping -c 4 8.8.8.8`
* **Resultado:** 4 recibidos, 0% pérdida
* **Latencia Promedio:** 9.00 ms | **TTL:** 113

### 4. Egreso Público (NAT)
* **Comando:** `curl ifconfig.me`
* **IP Pública:** `65.88.88.44`

---

### Diagnóstico Técnico
Se confirma la traducción de direcciones por NAT: el tráfico originado en la IP de clase B `172.19.92.146` sale a Internet a través de la interfaz del gateway `172.19.80.1` e ingresa a la red pública bajo la IP `65.88.88.44`. Red lista para laboratorios.
