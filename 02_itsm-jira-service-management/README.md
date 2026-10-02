# 🌐 Módulo 3: Diagnóstico de Redes y Troubleshooting en Windows (CLI)

##  Descripción del Módulo
Este módulo documenta los procedimientos metódicos de diagnóstico de red ejecutados desde la línea de comandos de Windows (CMD). El objetivo es aislar y resolver fallas comunes de conectividad local, enrutamiento y resolución de nombres (DNS) que reportan los usuarios finales a la mesa de ayuda.

---

##  Comandos Diagnósticos Ejecutados

### 1. Inspección de Configuración IP (`ipconfig /all`)
* **Propósito:** Obtener la configuración detallada de los adaptadores de red (dirección IPv4, máscara de subred, puerta de enlace predeterminada, servidores DNS y estado DHCP).
* **Escenario de Help Desk:** Se utiliza cuando un usuario reporta "sin acceso a red" para verificar si tiene asignada una IP válida o una dirección APIPA (`169.254.x.x`).

### 2. Depuración de Caché DNS (`ipconfig /flushdns`)
* **Propósito:** Vaciar la tabla local de resolución de nombres DNS en el sistema operativo.
* **Escenario de Help Desk:** Se aplica cuando un usuario no puede cargar un sitio web o servidor interno corporativo debido a registros DNS obsoletos en la caché local.

### 3. Pruebas de Conectividad (`ping`)
* **Propósito:** Validar el alcance de paquetes ICMP a nivel de IP y a nivel de resolución de nombres.
* **Comandos:**
  * `ping 8.8.8.8` *(Prueba de conectividad pura por IP)*.
  * `ping google.com` *(Prueba de resolución de nombres DNS)*.
* **Escenario de Help Desk:** Aísla si la falla es de la interfaz física/router o únicamente del servidor DNS.

### 4. Análisis de Ruta y Enrutamiento (`tracert -d`)
* **Propósito:** Mapear cada router/salto intermedio en el camino hacia una IP destino.
* **Uso del parámetro `-d`:** Deshabilita la resolución de nombres inversa para acelerar la ejecución del comando en la consola.
* **Escenario de Help Desk:** Detecta en cuál salto exacto de la red local, del ISP o de la WAN corporativa se interrumpe la conexión.

### 5. Consultas a Servidores DNS (`nslookup`)
* **Propósito:** Interrogar directamente al servidor DNS asignado para validar la resolución de nombres de dominio a direcciones IP.
* **Escenario de Help Desk:** Confirma si el servidor DNS interno o externo está respondiendo correctamente a las solicitudes de red.

---

##  Evidencia de Pruebas (Screenshots)
*(Agrega aquí las imágenes de tu consola desde la carpeta `screenshots`)*

![Ejecución de Comandos CLI](./screenshots/cmd_diagnostics.png)
