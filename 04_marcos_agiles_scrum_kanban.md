# **4. Marco de ejecución ágil: Scrum + Kanban**

Scrum y Kanban se aplican exclusivamente en los ciclos BML que requieren desarrollo de software: **Ciclo 3 (MVP v1.0)** y **Ciclo 4 (MVP v2.0)**. El Ciclo 1 (prototipo navegable), el Ciclo 2 (entrevistas) y el Ciclo 5 (demo en video) no requieren Sprint formal (Kniberg, 2015; Hammarberg & Sundén, 2014).

## **4.1. Equipo de trabajo — roles en el Sprint**

Cada integrante asume un rol de Scrum definido para la construcción técnica de los MVPs.

| Rol Scrum            | Persona        | Responsabilidad en el Build                                                                              |
| :------------------- | :------------- | :------------------------------------------------------------------------------------------------------- |
| **Product Owner**    | Andrés Mendoza | Define y prioriza las historias de usuario. Acepta los incrementos finales.                               |
| **Scrum Master**     | Sofía Rojas    | Facilita las ceremonias, elimina impedimentos y modera las sesiones de testing y QA.                     |
| **Development Team** | Luis Castro    | Diseño UX/UI y desarrollo del frontend responsivo.                                                       |
| **Development Team** | Carlos Ruiz    | Desarrollo del backend, base de datos, lógica de inventario y validación de criterios de aceptación.     |

## **4.2. Eventos y artefactos de Scrum**

### **4.2.1. Eventos**

Los eventos Scrum se aplican en cada Sprint de desarrollo. La columna de aplicación describe el enfoque para el primer Sprint (Ciclo 3).

| Evento                   | Descripción general                                                        | Aplicación en el Sprint 1 de desarrollo (Ciclo 3)                                                                                                                                                                  |
| :----------------------- | :------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Sprint**               | Ciclo de duración fija que contiene los demás eventos. | Duración de 2 semanas. **Objetivo del Sprint (Sprint Goal):** Desplegar el sistema básico de pedidos e inventario en entorno de prueba. |
| **Sprint Planning**      | Reunión para planear el trabajo del Sprint.                    | El equipo selecciona las historias de usuario del MVP v1.0, integrando los ajustes de UX del Ciclo 2.                                                                                                             |
| **Daily Scrum**          | Reunión diaria de 15 min para coordinar el equipo. | Revisión del avance en el tablero Kanban y resolución de bloqueos en la integración backend-frontend. |
| **Sprint Review**        | Presentación del incremento al cliente/stakeholders. | Demostración del flujo de registro de pedidos y control de stock funcionando en vivo.                                                                                                                   |
| **Sprint Retrospective** | Mejora del proceso de trabajo del equipo. | Análisis de la velocidad del equipo y ajuste de la comunicación entre el diseñador y el desarrollador. |

### **4.2.2. Artefactos**

| Artefacto           | Descripción                                                                                                                                 | Contenido en este proyecto                                                                                                                                                                               |
| :------------------ | :------------------------------------------------------------------------------------------------------------------------------------------ | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Product Backlog** | Lista priorizada de requerimientos del sistema.                                                                                           | Módulo de pedidos, gestión de inventario, lista de entregas, dashboard responsivo y base de datos de productos. |
| **Sprint Backlog**  | Tareas seleccionadas para el Sprint actual.                                                                                                | Implementación de la base de datos, creación de formularios de pedido y vista de inventario. |
| **Incremento**      | Resultado funcional del Sprint que cumple el DoD.                                                                                           | Versión usable del sistema desplegada en entorno de prueba, capaz de registrar un pedido y descontar stock. |

### **4.2.3. MVP v1.0 a desarrollar**

El **MVP v1.0** es la primera versión funcional de la plataforma web unificada para **Mueblería J & M**. Su desarrollo se planifica para ejecutarse en el primer Sprint (2 semanas) y se centra en digitalizar las operaciones críticas para reducir los errores manuales y agilizar la logística.

**Funcionalidades incluidas en el MVP v1.0:**
- Autenticación y navegación básica.
- Formulario digital para el registro de nuevos pedidos.
- Módulo de inventario con actualización de stock en tiempo real.
- Panel de entregas del día optimizado para dispositivos móviles (para repartidores).
- Datos de prueba (Seed data) para simular catálogos y clientes.

**Resultado esperado:** Al finalizar el Sprint, se dispondrá de una versión web usable en un entorno de prueba. El vendedor podrá registrar un pedido, el encargado de almacén descontar stock, y el repartidor visualizar y confirmar sus entregas sin usar papel ni WhatsApp.

## **4.3. Tablero Kanban del Sprint**

El tablero Kanban gestiona el flujo diario de tareas dentro de cada Sprint de desarrollo. Se encuentra publicado en: [ENLACE_A_TU_TABLERO_GITHUB_PROJECTS_AQUI]

Cada tarea avanza de izquierda a derecha por las columnas, con límites WIP que impiden acumular trabajo en progreso y hacen visibles los bloqueos el mismo día en que ocurren (Hammarberg & Sundén, 2014):

| 📋 Product Backlog                                       | 🔍 To Do (WIP ≤ 5)                                           | ⚙️ In Progress (WIP ≤ 3)                           | 🧪 Testing (WIP ≤ 3)                                  | ✅ Done                                |
| :------------------------------------------------------- | :----------------------------------------------------------- | :------------------------------------------------- | :---------------------------------------------------- | :------------------------------------- |
| _(historias o tareas priorizadas, aún fuera del Sprint)_ | _(tareas seleccionadas para el Sprint, listas para iniciar)_ | _(tareas en desarrollo backend, frontend o UX/UI)_ | _(verificación de criterios de aceptación y pruebas)_ | _(tareas terminadas con DoD cumplida)_ |

**Figura 1. Tablero Kanban del Sprint 1 en GitHub Projects**

![Captura del tablero Kanban completo](RUTA_DE_TU_IMAGEN_1_AQUI)

Esta imagen evidencia cómo Kanban se usa para visualizar el avance diario y detectar bloqueos dentro del Sprint.

**Figura 2. Detalle de límites WIP y estados del tablero**

![Captura de las columnas con los límites WIP](RUTA_DE_TU_IMAGEN_2_AQUI)

Esta evidencia permite justificar que el equipo no solo registra tareas, sino que controla la cantidad de trabajo simultáneo para evitar acumulación y pérdida de foco.

**Definición de Done (DoD):** Una tarea alcanza la columna Done del tablero Kanban cuando:
1. El código está implementado y desplegado en el entorno de prueba.
2. Ha sido verificado contra los criterios de aceptación de la historia de usuario correspondiente.
3. No presenta errores críticos de usabilidad. Ninguna tarea puede avanzar a Done sin pasar por la columna de testing.

## **4.4. Historias de usuario y gestión de tareas**

Para cada Sprint de desarrollo se definen **historias de usuario** que describen las funcionalidades desde la perspectiva del usuario final, y **tareas técnicas** derivadas de cada historia que el equipo ejecuta durante el Sprint.

**Figura 3. Historia de usuario registrada para el MVP v1.0**

![Captura de una historia de usuario / Issue en GitHub](RUTA_DE_TU_IMAGEN_3_AQUI)

La tarjeta o issue incluye criterios de aceptación claros, tareas técnicas, estimación de esfuerzo y prioridad.

**Figura 4. Descomposición de la historia en tareas técnicas**

![Captura de las tareas técnicas (checklist) dentro del Issue](RUTA_DE_TU_IMAGEN_4_AQUI)

Las tareas técnicas conectan la necesidad del usuario con el trabajo concreto del Sprint.

**Figura 5. Miembros del equipo agregados en GitHub Projects y en el repositorio de Github**

![Captura de los miembros del equipo agregados](RUTA_DE_TU_IMAGEN_5_AQUI)

Con esto documentamos que el equipo fue incorporado dentro de la herramienta para facilitar la asignación de responsabilidades y la gestión de tareas del proyecto.

**Figura 6. Asignación de tareas a los miembros del equipo en GitHub Projects**

![Captura de tareas asignadas a miembros](RUTA_DE_TU_IMAGEN_6_AQUI)

Con esto documentamos que las tareas del proyecto son distribuidas entre los integrantes del equipo, permitiendo una mejor organización y control durante la construcción del MVP.

## **4.5. Gestión de tareas incompletas y nuevos Sprints**

Si una tarea no alcanza el estado Done al cierre del Sprint:
- **Tareas bloqueadas:** Regresan al Product Backlog para ser repriorizadas por el PO.
- **Tareas parcialmente avanzadas:** Se analizan en la Retrospective; si son críticas, se trasladan al siguiente Sprint manteniendo el avance.
- **Sprint Goal no alcanzado:** El incremento no se considera válido y se planifica un Sprint correctivo antes de avanzar al siguiente ciclo BML.
