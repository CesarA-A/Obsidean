---
Date: 2025-11-02
tags:
---
---

Para ver que versión de Kathara tenemos se usa kathara -v.

## 💻 Guía Rápida de Comandos Kathara

### 🔄 Gestión Básica del Laboratorio
- **Iniciar:** `kathara lstart` 
- **Detener:** `kathara lstop`
- **Limpiar restos:** `kathara lclean`

### 🖥️ Trabajar con Nodos
- **Terminal en nodo:** `kathara lterm <nodo>`
- **Ver nodos activos:** `kathara lshow`
- **Copiar archivos:** `kathara lcp <archivo> <nodo>:/ruta/`

### ⚡ Comandos Avanzados
- **Crear MV:** `kathara vstart -n pc --eth 0:A`
- **Limpiar total:** `kathara wipe -a` (¡Usar con precaución!)
- **GitHub:** `kathara lpull` / `kathara lpush`


En kathara se define el archivo **lab.conf** el cual se utiliza para la conexión de cada MV.
Los **.startup** le define el nodo que tipo de configuración tendrá.


# Docker

Para inciarlo:  sudo systemctl start docker