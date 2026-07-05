# **3. Aplicación de Lean Startup**

Lean Startup estructura la validación de la solución propuesta a través del ciclo **Build → Measure → Learn**, priorizando el aprendizaje rápido sobre la construcción perfecta (Bland & Osterwalder, 2019). La etapa de Construir se ejecuta con el equipo organizado en un Sprint de Scrum (Kniberg, 2015), gestionado con un tablero Kanban (Hammarberg & Sundén, 2014).

## **3.1. Equipo de trabajo**

La siguiente tabla muestra cómo cada integrante del equipo participa en las fases del ciclo BML según su rol.

| Integrante         | Rol                                        | Fase del ciclo BML                                                                                                                                                                   |
| :----------------- | :----------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Andrés Mendoza** | Product Owner / Innovation Lead            | Preparación: formula las hipótesis y define los criterios de éxito. Learn: lidera la revisión de aprendizajes y la decisión de producto.                                             |
| **Sofía Rojas**    | Scrum Master / Jefe de Proyecto            | Build: facilita el Sprint, elimina bloqueos y garantiza el cumplimiento de las ceremonias Scrum. Measure: modera las pruebas y registra los resultados.                               |
| **Luis Castro**    | Diseñador UX/UI                            | Build: diseña e implementa la arquitectura y las vistas en el prototipo web.                                                                                                         |
| **Carlos Ruiz**    | Tech Lead / Fullstack Developer            | Build: lidera el desarrollo técnico del prototipo web. Measure: verifica los criterios de aceptación durante las pruebas.                                                           |

Este documento describe el **Ciclo 1** del proceso de validación. La planificación de los ciclos futuros se presenta en la sección 3.6.

---

## **3.2. Preparación**

### **3.2.1. Contexto del problema**

**Empresa:** Mueblería J & M.
**Problema validado:** La gestión logística es manual y fragmentada. El registro en cuadernos y el control físico de stock generan errores operativos y pérdida de eficiencia. El personal desea digitalizarse, pero necesita una herramienta simple que no complique su flujo de trabajo diario.
**Oportunidad:** Un sistema web centralizado transformaría el proceso de reactivo (esperar a que alguien avise) a proactivo (ver el estado en tiempo real), eliminando la duplicidad de tareas y el error humano.

### **3.2.2. Proto persona**

_(Ver sección 2.3, Design Thinking, para el detalle completo)._

**Usuario principal del experimento:** Juan Pérez, Vendedor, requiere rapidez al registrar pedidos y certeza sobre el stock disponible.
**Usuario secundario:** Pedro Díaz, Repartidor, requiere claridad en sus rutas diarias desde el móvil.

### **3.2.3. Hipótesis de validación**

**Hipótesis 1:**
**Creemos que** Juan Pérez (Vendedor)
**tiene el problema de** generar errores en los pedidos y confirmar stock inexistente debido al registro manual
**y que** contar con un formulario digital vinculado a un inventario actualizado en tiempo real
**le ayudará a** registrar pedidos sin errores y reducir las quejas de clientes por falta de disponibilidad.

**Hipótesis 2:**
**Creemos que** Pedro Díaz (Repartidor)
**tiene el problema de** coordinar entregas ineficientemente por depender de mensajes de WhatsApp desorganizados
**y que** tener una lista de entregas estructurada y accesible desde su celular
**le ayudará a** organizar mejor su ruta y confirmar entregas de forma inmediata.

### **3.2.4. Plan de experimento**

| Elemento                | Detalle                                                                                                                                           |
| :---------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Tipo de experimento** | Prototipo web navegable desarrollado por el equipo (demo funcional de flujos).                                                                              |
| **Duración**            | 2 semanas (Sprint 1, ejecutado con Scrum + Kanban).                                                                                               |
| **Participantes**       | 3 perfiles simulados: Vendedor, Encargado de Almacén, Repartidor.                                                                                    |
| **Escenario de prueba** | 3 tareas críticas: registro de pedido, actualización de stock y confirmación de entrega. El moderador observa la interacción sin intervenir. |

### **3.2.5. Criterios de éxito**

| # | Métrica | Condición de éxito |
| :--- | :--- | :--- |
| 1 | Completación del flujo sin ayuda | Al menos 2 de 3 participantes completan su tarea sin solicitar ayuda al moderador. |
| 2 | Tiempo de tarea | Tiempo promedio por tarea ≤ 3 minutos. |
| 3 | Satisfacción del usuario | Puntaje promedio ≥ 4 / 5 en la encuesta post-tarea. |

---

## **3.3. Construir (Build)**

El **artefacto mínimo de validación** es la versión más simple de la solución que permite validar la hipótesis. Para evitar desperdicio de recursos, se diferencia entre artefactos de diseño y MVPs funcionales.

### **3.3.1. Artefacto mínimo de validación del Ciclo 1**

Para el Ciclo 1, el artefacto es un **prototipo navegable de diseño**. No ejecuta lógica de base de datos real, sino que simula los flujos de navegación para validar la usabilidad.

| Componente | Descripción | Responsable |
| :--- | :--- | :--- |
| Pantallas de alta fidelidad | Diseño visual del Dashboard, Gestión de Pedidos, Inventario y Entregas. | Luis Castro (UX/UI) |
| Flujo de navegación interactivo | Vínculos entre pantallas que permiten recorrer el Taskflow 1 y 2. | Luis Castro (UX/UI) |
| Datos estáticos para la demo | Ejemplos de muebles, nombres de clientes y rutas de entrega cargados en el prototipo. | Carlos Ruiz (Tech Lead) |
| Criterios de prueba | Definición de las 3 tareas y métricas de éxito. | Sofía Rojas (Scrum Master) |

### **3.3.2. Métricas a observar**

| Métrica | Cómo se mide | Fuente |
| :--- | :--- | :--- |
| Completación del flujo sin ayuda | Observación directa: ¿llegó al final sin ayuda? (Sí/No). | Moderador |
| Tiempo de tarea | Tiempo transcurrido desde la instrucción hasta el fin. | Cronómetro |
| Satisfacción del usuario | Respuesta oral a: *"¿Qué tan fácil fue completar esta tarea?"* (1-5). | Encuesta oral |

---

## **3.4. Medir (Measure)**

_En esta fase se ejecutan las pruebas sobre el prototipo construido._

### **3.4.1. Ejecución de las pruebas de usabilidad**

**Tarea 1: Registro de pedido — Juan Pérez**
> *"Registra la venta de un 'Comedor de Roble' para el cliente 'Miguel Torres' con entrega el viernes a las 10am."*

| Métrica                          | Resultado                                                                              | Estado |
| :------------------------------- | :------------------------------------------------------------------------------------- | :----- |
| Completación del flujo sin ayuda | Completó el registro sin ayuda. Encontró el botón "Nuevo Pedido" rápidamente. | ✅     |
| Tiempo de tarea                  | 1 min 30 seg                                                                           | ✅     |
| Satisfacción del usuario         | 5 / 5                                                                                  | ✅     |

---

**Tarea 2: Actualización de stock — María Gómez**
> *"Busca el producto 'Cama King' en el inventario y actualiza la cantidad a 5 unidades."*

| Métrica                          | Resultado                                                                                                               | Estado |
| :------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------- | :----- |
| Completación del flujo sin ayuda | Completó la tarea, pero dudó en dónde hacer clic para editar la cantidad. | ⚠️     |
| Tiempo de tarea                  | 2 min 10 seg                                                                                                            | ✅     |
| Satisfacción del usuario         | 4 / 5                                                                                                                   | ✅     |

**Hallazgo:** El botón de edición de stock no es lo suficientemente visible. **Corrección:** Cambiar el enlace de texto por un botón de acción claro ("Editar").

---

**Tarea 3: Confirmación de entrega — Pedro Díaz**
> *"Consulta la lista de entregas de hoy y marca la primera como entregada."*

| Métrica                          | Resultado                                                                                                                                           | Estado |
| :------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :----- |
| Completación del flujo sin ayuda | No encontró el botón "Marcar como Entregado" inicialmente; estaba al final de la tarjeta, fuera del área visible en su móvil. | ❌     |
| Tiempo de tarea                  | 3 min 45 seg (incluyendo guía del moderador)                                                                                                             | ❌     |
| Satisfacción del usuario         | 3 / 5                                                                                                                    | ⚠️     |

**Hallazgo:** La disposición de la tarjeta de entrega no es "mobile-first", obligando al usuario a hacer scroll excesivo. **Corrección:** Reposicionar el botón de acción en la parte superior de la tarjeta.

### **3.4.2. Resultados comparados con los criterios de éxito**

| Métrica | Condición de éxito | Resultado | Estado |
| :--- | :--- | :--- | :--- |
| Completación del flujo sin ayuda | ≥ 2 / 3 sin ayuda | 2 / 3 (Juan y María; Pedro solicitó ayuda) | ✅ Cumplido |
| Tiempo de tarea | Promedio ≤ 3 min | Promedio: 2 min 25 seg | ✅ Cumplido |
| Satisfacción del usuario | Promedio ≥ 4 / 5 | 4.0 / 5 (Juan: 5, María: 4, Pedro: 3) | ✅ Cumplido |

### **3.4.3. Resumen de hallazgos de usabilidad**

| #   | Hallazgo                                                          | Severidad | Corrección propuesta                                        |
| :-- | :---------------------------------------------------------------- | :-------- | :---------------------------------------------------------- |
| 1   | Botón de edición de stock poco visible.                            | Media      | Reemplazar enlace por botón de acción destacado.           |
| 2   | Botón de confirmación de entrega fuera de vista en móviles.        | Alta      | Reposicionar el botón en la parte superior de la tarjeta.   |
| 3   | Confusión inicial sobre el estado "En Ruta".                      | Baja      | Agregar una leyenda explicativa de los estados de pedido. |

---

## **3.5. Aprender (Learn)**

### **3.5.1. Informe de aprendizaje validado: Ciclo 1**

**Aprendizajes clave:**
1. **El flujo de registro es intuitivo.** El vendedor valora la rapidez del formulario y la visibilidad del stock, lo que valida la hipótesis de reducción de errores.
2. **La gestión de inventario requiere mejores indicadores visuales.** El usuario de almacén necesita acciones más directas para evitar la fatiga visual.
3. **La experiencia del repartidor es el punto más débil.** El diseño actual no considera la ergonomía móvil, lo que es crítico ya que el repartidor usa el sistema en movimiento.

### **3.5.2. Conclusiones sobre las hipótesis**

| Hipótesis                                                                | Conclusión del Ciclo 1                                                                                                                                              |
| :----------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Hipótesis 1** (registro digital $\rightarrow$ reducción de errores)   | **Validada.** El flujo es eficiente y el usuario percibe la utilidad de tener el stock a la mano.                                                                     |
| **Hipótesis 2** (lista estructurada $\rightarrow$ rutas eficientes)       | **Parcialmente validada.** El concepto es correcto, pero la interfaz móvil dificulta la ejecución rápida de la tarea. Se ajusta el diseño en el Ciclo 2. |

### **3.5.3. Decisión de producto**

| Dimensión                                                  | Decisión       | Acción para el siguiente ciclo                                 |
| :--------------------------------------------------------- | :------------- | :------------------------------------------------------------- |
| Concepto central (sistema web de gestión logística)        | **Perseverar** | El concepto es válido y resuelve el problema raíz. Continuar. |
| Interfaz de Inventario (edición de stock)                   | **Ajustar**    | Implementar botones de acción rápida.                          |
| Diseño de Tarjetas de Entrega (mobile-first)                | **Ajustar**    | Rediseñar la jerarquía visual de las tarjetas para móviles. |

---

## **3.6. Planificación de ciclos BML**

Cada ciclo del proceso Construir - Medir - Aprender emplea un artefacto mínimo de validación distinto, elegido según la pregunta que se busca responder en ese momento del proyecto.

### **3.6.1. Descripción de MVPs por ciclo**

Los MVPs son las versiones desarrolladas del sistema. El MVP v1.0 se despliega en un entorno de prueba controlado; el MVP v2.0 avanza hacia un entorno con mayor alcance según los aprendizajes del ciclo anterior. Los demás ciclos (Ciclos 1, 2 y 5) emplean artefactos mínimos de validación más ligeros que no constituyen un MVP.

**MVP v1.0 (Ciclo 3):** Primera versión del sistema desplegada en un entorno de prueba controlado. Se construye en uno o más Sprints e incorpora los ajustes de UX validados en el Ciclo 2. Permite medir el impacto real con un grupo pequeño de usuarios en entorno de prueba.

**MVP v2.0 (Ciclo 4):** Segunda versión del sistema, construida en Sprints adicionales, con mejoras derivadas del Ciclo 3: validación de mejoras en la gestión de stock crítico y optimización de rutas.

### **3.6.2. Tabla de ciclos BML**

| Ciclo | Artefacto mínimo de validación | Objetivo de validación | Requiere Sprint | Estado |
| :--- | :--- | :--- | :--- | :--- |
| **Ciclo 1** | Prototipo navegable | Validar flujos básicos y usabilidad inicial. | No | ✅ Completado |
| **Ciclo 2** | Entrevistas + Encuesta | Validar que los ajustes de UX resuelven los problemas detectados. | No | 🔜 Planificado |
| **Ciclo 3** | MVP v1.0 | Medir el impacto real con un grupo pequeño de usuarios en entorno de prueba. | Sí | 🔜 Planificado |
| **Ciclo 4** | MVP v2.0 | Validar mejoras en la gestión de stock crítico y optimización de rutas. | Sí | 🔜 Planificado |
| **Ciclo 5** | Demo en video | Validar la percepción de valor ante los dueños del negocio. | No | 🔜 Planificado |
