#  Módulo 2: Gestión de Servicios e Incidentes ITSM con Jira Service Management

##  Descripción del Módulo
Este módulo documenta la implementación y operación de un sistema de gestión de servicios de TI (ITSM) alineado con las mejores prácticas de **ITIL v4**. El objetivo es simular el flujo de trabajo real de un Help Desk L1/L2 mediante la recepción, clasificación, asignación, escalamiento y resolución de tickets de incidentes y solicitudes de servicio.

---

## ⚙️ Entorno y Tecnologías Utilizadas
* **Plataforma ITSM:** Jira Service Management Cloud (`soportetilab.atlassian.net`)
* **Plantilla de Proyecto:** IT Service Management / Gestión de Servicios de TI
* **Roles Simulados:**
  * **Usuario Final / Cliente:** Requestor (`alopez@DapaCorp.onmicrosoft.com`)
  * **Agente de Soporte L1:** Assignee (`Jiovanni López`)

---

##  Actividades y Procedimientos Ejecutados

### 1. Configuración de la Mesa de Ayuda Corporativa
* Despliegue del espacio de trabajo de soporte técnico en Jira Service Management.
* Configuración del **Portal de Clientes** para la recepción estructurada de solicitudes de usuarios finales.
* Definición de colas de trabajo (*Queues*) para el filtrado eficiente de tickets (*All Open*, *Assigned to me*, *Unassigned*).

### 2. Registro e Ingesta de Incidentes
* **Generación de Ticket:** Registro de la solicitud `PDM-1` mediante el portal de autoservicio.
* **Resumen del Incidente:** *Usuario bloqueado - Restablecimiento de contraseña M365*.
* **Categorización:** Solicitud de Acceso / Incidente de Software (`Submit a request or incident`).
* **Priorización:** Definición de nivel de prioridad Media (`Medium`) de acuerdo con el impacto individual del usuario.

### 3. Gestión del Ciclo de Vida del Ticket (Workflow)
* **Asignación:** Toma de responsabilidad del ticket (*Assignee*) por parte del agente de soporte.
* **Transición de Estados:**
  1. `Tareas por hacer (Open)` $\rightarrow$ Ticket recién ingresado en cola.
  2. `En curso (In Progress)` $\rightarrow$ Início de atención diagnóstica y trabajo técnico.
  3. `Resuelto (Resolved)` $\rightarrow$ Cierre del caso tras aplicar la solución.

### 4. Documentación y Comunicación con el Cliente
* **Registro de Notas Internas:** Documentación técnica privada en el ticket sobre las acciones realizadas en el panel de administración de Microsoft Entra ID.
* **Respuesta al Cliente:** Envío de notificación formal al usuario confirmando la solución del problema e instrucciones para el restablecimiento de su clave.

---

##  Competencias Demostradas
* **Metodología ITIL v4:** Comprensión práctica de la Gestión de Incidentes (*Incident Management*) y Solicitudes de Servicio (*Service Request Management*).
* **Manejo de Plataformas ITSM:** Dominio operativo de Jira Service Management (colas, asignaciones, estados y portales de usuario).
* **Atención y Comunicación:** Redacción clara de soluciones tanto para registro técnico interno como para cara al cliente final.

---

##  Evidencia de Pruebas (Screenshots)

| Módulo / Caso de Uso | Captura de Pantalla |
| :--- | :--- |
| **Portal de Atención al Cliente** | `![Portal Jira](./screenshots/01_jira_portal.png)` |
| **Cola de Tickets (Queues)** | `![Colas de Trabajo](./screenshots/02_jira_queues.png)` |
| **Atención y Comentarios del Agente** | `![Ticket In Progress](./screenshots/03_jira_in_progress.png)` |
| **Cierre y Resolución del Ticket** | `![Ticket Resuelto](./screenshots/04_jira_resolved.png)` |
