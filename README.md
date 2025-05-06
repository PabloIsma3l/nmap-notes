# 🛠️ Nmap - Notas básicas

Este documento resume los conceptos y comandos esenciales aprendidos sobre la herramienta de escaneo de redes **Nmap**.

---

## 🔍 Conceptos clave aprendidos

- ¿Qué es Nmap y para qué se usa?
- Tipos de escaneo:
  - Escaneo SYN (`-sS`)
  - Escaneo completo (`-sT`)
  - Escaneo UDP (`-sU`)
- Escaneo de puertos y servicios
- Detección de versiones de servicios (`-sV`)
- Uso de scripts NSE para automatización de tareas comunes y ataques como fuerza bruta
- Opciones de anonimato como el cambio de dirección MAC

---

## 🧪 Comandos prácticos

```bash
# Escaneo básico
nmap 127.0.0.1

# Escaneo SYN
nmap -sS 127.0.0.1

# Detección de versiones de servicios
nmap -sV 127.0.0.1

# Uso de scripts para ataques de fuerza bruta (ejemplo: SSH)
nmap --script ssh-brute -p 22 192.168.1.10

# Cambiar la dirección MAC para anonimato
nmap --spoof-mac 0 192.168.1.10
# O usar una marca específica: Apple, Cisco, etc.
nmap --spoof-mac Apple 192.168.1.10
