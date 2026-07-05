# **2. Aplicación de Design Thinking**

Design Thinking es un proceso de innovación centrado en el ser humano que recorre cinco etapas iterativas: Empatizar, Definir, Idear, Prototipar y Testear (Riley, 2024). En este proyecto, las etapas de Prototipar y Testear se integran con el ciclo BML de Lean Startup (Bland & Osterwalder, 2019).

## **2.1. Equipo de trabajo**

Cada integrante del grupo asumió un rol específico para el desarrollo del proyecto. La siguiente tabla muestra la distribución de responsabilidades en las etapas de Design Thinking.

| Integrante         | Rol                                        | Etapas de Design Thinking                                                                                               |
| :----------------- | :----------------------------------------- | :---------------------------------------------------------------------------------------------------------------------- |
| **Andrés Mendoza** | Product Owner / Innovation Lead            | Empatizar, Definir: facilita las actividades, sintetiza hallazgos y redacta el enunciado del problema.                  |
| **Sofía Rojas**    | Scrum Master / Jefe de Proyecto            | Todas: coordina la dinámica del equipo, gestiona tiempos y asegura la entrega de artefactos; apoya en Testear.          |
| **Luis Castro**    | Diseñador UX/UI                            | Idear, Prototipar: diseña la arquitectura de la información, el flujo de tareas y los wireframes.                       |
| **Carlos Ruiz**    | Tech Lead / Fullstack Developer            | Idear, Prototipar, Testear: evalúa la viabilidad técnica, lidera el prototipo y define los criterios de aceptación.    |

---

## **2.2. Empatizar**

### **2.2.1. Resumen del proyecto / Contexto**

_Este análisis es un estudio simulado elaborado con fines académicos. La información sobre Mueblería J & M proviene de la reconstrucción de prácticas comunes del sector minorista de muebles en Arequipa._

**Empresa:** Mueblería J & M, negocio familiar de comercio minorista de muebles para el hogar localizado en la ciudad de Arequipa, Perú.

**Proceso analizado:** Gestión logística interna, abarcando desde el registro del pedido por el vendedor, la verificación de stock en almacén, hasta la coordinación y ejecución de la entrega a domicilio.

**Problema central identificado:** El negocio opera bajo un modelo de madurez digital inicial (Nivel 1), donde la gestión logística es enteramente manual. Los pedidos se anotan en cuadernos, el inventario se controla físicamente y las entregas se coordinan mediante WhatsApp e llamadas. Esta fragmentación genera pérdida de datos, errores en la disponibilidad de productos y retrasos en las entregas, afectando la eficiencia operativa y la experiencia del cliente.

**Innovación propuesta:** Implementar un sistema web básico de gestión logística que integre en una sola plataforma los módulos de registro de pedidos, control de inventario y planificación de entregas, accesible desde cualquier dispositivo con conexión a internet.

### **2.2.2. Alcance del proyecto**

El alcance corresponde al desarrollo de un **prototipo funcional de un sistema web básico de gestión logística** para Mueblería J & M. El sistema se centrará en la digitalización de los tres procesos críticos identificados.

| Incluido en el alcance                                                                                                       | Excluido del alcance                                          |
| :--------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------ |
| Módulo de registro de pedidos con datos de cliente, producto y estado.                                                       | Integración con pasarelas de pago o facturación electrónica.      |
| Módulo de inventario digital con actualización automática y alertas de stock mínimo.                                         | E-commerce o catálogo virtual interactivo para el cliente final. |
| Módulo de planificación de entregas con listado estructurado para el repartidor.                                            | Optimización de rutas mediante IA o integración con Google Maps API. |
| Interfaz web responsiva accesible para vendedor, almacén y repartidor.                                                       | Integración oficial con API de WhatsApp Business.                |

### **2.2.3. Análisis comparativo de la competencia**

Se realizó un benchmarking para identificar cómo otros negocios de retail de muebles o logística minorista gestionan sus procesos internos, buscando prácticas replicables.

| Empresa / Referente                     | Tipo               | Herramienta de gestión                        | Mecanismo operativo                                                                                                           | Fortaleza identificada                                                                            | Brecha respecto a Mueblería J & M                                                                                      |
| :-------------------------------------- | :----------------- | :-------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------------------------------- |
| **Tiendas Grandes (Retail)**           | Directo            | ERP Corporativo (SAP/Oracle)                 | Procesos automatizados de punta a punta, desde la venta hasta la entrega con trazabilidad total.                                           | Precisión absoluta en inventario y tiempos de entrega.                                          | Costo de implementación prohibitivo y complejidad excesiva para un negocio familiar.                               |
| **Mueblerías Locales Medianas**         | Directo            | Hojas de cálculo (Excel/Google Sheets)       | Registro digital básico de ventas e inventario, pero coordinación de entregas aún manual.                                           | Mejor control de datos que el papel; visibilidad compartida simple.                                  | Sigue siendo un proceso fragmentado; falta de alertas automáticas y flujo coordinado entre roles. |
| **Courier Logístico Local**             | Indirecto          | App de gestión de rutas propia               | Planificación digital de entregas y confirmación de recepción mediante firma digital o foto.                                           | Eficiencia extrema en la última milla y trazabilidad del repartidor.                                  | Especializado solo en entrega; no gestiona la venta ni el inventario del producto. |
| **SaaS de Gestión de Inventario**       | Análogo            | Software en la nube (SaaS)                    | Gestión de stock en tiempo real con alertas de reposición y reportes de movimiento.                                           | Estandarización de procesos y facilidad de despliegue.                                            | Generalista; no adaptado al flujo específico de pedidos personalizados de muebles. |
| **Mueblería J & M (As-Is)**             | Referente interno  | Cuadernos / WhatsApp / Llamadas               | Gestión reactiva y manual. Dependencia total de la memoria del personal y comunicación informal.                                           | Máxima flexibilidad inmediata.                                                                           | Nula sistematización; alta tasa de error y riesgo de pérdida de información. |
| **Sistema Propuesto (Solución)**       | Solución propuesta | Sistema Web a medida (PaaS/SaaS)             | Plataforma unificada de Pedidos $\rightarrow$ Inventario $\rightarrow$ Entregas, diseñada para el flujo real del negocio. | Balance óptimo entre impacto y esfuerzo; elimina los tres cuellos de botella principales. | Requiere desarrollo propio y capacitación básica del personal.                                          |

**Conclusión del benchmarking:** Existe una brecha digital significativa entre Mueblería J & M y los referentes del sector. Mientras que los grandes retailers usan ERPs complejos, las medianas empresas usan hojas de cálculo que siguen siendo insuficientes para coordinar el flujo completo. La oportunidad reside en crear una solución a medida que sea más potente que un Excel pero más simple que un ERP, enfocándose específicamente en el flujo logístico.

---

## **2.3. Definir**

### **2.3.1. Proto personas**

Se definen tres proto personas que representan a los actores clave del proceso logístico. Estas representaciones permiten diseñar la interfaz basándose en necesidades y puntos de dolor reales.

---

**Proto Persona 1**

**Nombre y apellido:** Juan Pérez
**Rol / tipo de usuario:** Vendedor
**Descripción del rol:** Encargado de atender a los clientes en tienda y redes sociales, cerrar las ventas y registrar los pedidos.
**Puntos de dolor:** Registra pedidos en papel y luego debe coordinar verbalmente con almacén. A veces confirma un producto que ya no hay stock, generando molestia en el cliente. Pierde tiempo anotando la misma información varias veces.
**Necesidades:** Un formulario digital rápido para registrar pedidos y una forma de ver la disponibilidad real del inventario antes de cerrar la venta.

---

**Proto Persona 2**

**Nombre y apellido:** María Gómez
**Rol / tipo de usuario:** Encargada de Almacén
**Descripción del rol:** Responsable de custodiar los muebles, verificar la existencia de productos y preparar los pedidos para entrega.
**Puntos de dolor:** Recibe pedidos vía WhatsApp o papel que a veces no son legibles. Debe contar físicamente los muebles para saber si hay stock, un proceso lento y propenso a errores. No sabe qué pedidos son urgentes hasta que el vendedor se lo indica.
**Necesidades:** Una lista digital de pedidos pendientes por preparar y un inventario actualizado que se descuente automáticamente al confirmar una venta.

---

**Proto Persona 3**

**Nombre y apellido:** Pedro Díaz
**Rol / tipo de usuario:** Repartidor
**Descripción del rol:** Encargado de transportar los muebles desde el almacén hasta el domicilio del cliente en Arequipa.
**Puntos de dolor:** Recibe las direcciones y horarios de entrega de forma desorganizada. A menudo tiene que llamar al vendedor para confirmar detalles de la dirección o el producto a entregar. No tiene forma de registrar que ya entregó el producto.
**Necesidades:** Una lista de entregas del día organizada por horario y dirección, accesible desde su celular, y un botón para marcar el pedido como "Entregado".

---

## **2.4. Idear**

### **2.4.1. Arquitectura de la información**

La arquitectura del sistema se diseña para ser minimalista y eficiente, asegurando que cada rol acceda rápidamente a la información que necesita.

```text
Vista: Dashboard General (Acceso compartido)
	Sección: Barra de navegación
		Link: Pedidos -> Vista: Gestión de Pedidos
		Link: Inventario -> Vista: Control de Inventario
		Link: Entregas -> Vista: Planificación de Entregas
		Link icon: Usuario (Perfil/Cerrar sesión)
	Sección: Resumen Operativo (Widgets)
		Widget: Pedidos Pendientes (Contador)
		Widget: Productos con Stock Crítico (Lista corta)
		Widget: Entregas Programadas para Hoy (Contador)

Vista: Gestión de Pedidos
	Sección: Buscador de Pedidos
		Input: Buscar por Cliente o ID
	Sección: Botón "Nuevo Pedido" -> Modal: Registro de Pedido
	Sección: Tabla de Pedidos
		Columnas: ID, Cliente, Producto, Fecha, Estado (Pendiente/En Almacén/En Ruta/Entregado)
		Acción: Ver detalle / Cambiar estado

Modal: Registro de Pedido
	Campo: Nombre del Cliente
	Campo: Teléfono / Contacto
	Campo: Dirección de Entrega
	Selector: Producto (Carga desde Inventario)
	Campo: Cantidad
	Campo: Fecha/Hora acordada
	Botón: Guardar Pedido
	Botón: Cancelar

Vista: Control de Inventario
	Sección: Buscador de Productos
		Input: Buscar producto
	Sección: Tabla de Inventario
		Columnas: Producto, Categoría, Stock Actual, Stock Mínimo, Estado (Disponible/Bajo Stock/Agotado)
		Acción: Editar cantidad / Agregar nuevo producto

Vista: Planificación de Entregas
	Sección: Filtro de Fecha
		Selector: Seleccionar día
	Sección: Lista de Entregas del Día
		Tarjeta de Entrega
			Cliente: [Nombre]
			Dirección: [Dirección]
			Producto: [Producto]
			Horario: [Hora]
			Botón: Marcar como Entregado -> Animación de éxito
```

### **2.4.2. Diseño de interacción: Flujos de tareas**

Se definen los flujos principales para validar la eficiencia del sistema.

**Taskflow 1: Verificación de stock y registro de pedido (Happy Path)**

**Rol / tipo de usuario:** Vendedor (Juan Pérez)

**Objetivo:** Verificar el inventario desde el dashboard, consultar disponibilidad y registrar un nuevo pedido.

```text
1. Entra a la vista Dashboard General
2. Mira el widget Productos con Stock Crítico
3. Hace clic en el link Inventario de la barra de navegación
4. Mira la vista Control de Inventario
5. Escribe el nombre del producto en el Buscador de Productos
6. Mira el Stock Actual en la Tabla de Inventario y confirma disponibilidad
7. Hace clic en el link Pedidos de la barra de navegación
8. Mira la vista Gestión de Pedidos
9. Hace clic en el botón "Nuevo Pedido"
10. Mira el Modal: Registro de Pedido
11. Ingresa los datos del cliente (Nombre, Teléfono, Dirección)
12. Selecciona el producto del selector y define la Cantidad
13. Ingresa la Fecha/Hora acordada para la entrega
14. Hace clic en el botón Guardar Pedido
15. Mira una animación de confirmación y cómo se cierra el modal
16. Mira la Tabla de Pedidos actualizada con el nuevo registro en estado Pendiente
```

**Taskflow 2: Ejecución y confirmación de entrega**

**Rol / tipo de usuario:** Repartidor (Pedro Díaz)

**Objetivo:** Consultar la ruta del día y marcar un pedido como entregado satisfactoriamente.

```text
1. Ingresa al sistema desde su celular
2. Navega a "Planificación de Entregas"
3. Selecciona la fecha actual
4. Mira la Lista de Entregas del Día
5. Identifica el primer pedido de la lista
6. Lee la dirección y el producto a entregar
7. Realiza la entrega física al domicilio del cliente
8. Hace clic en el botón "Marcar como Entregado"
9. Mira la animación de éxito y ve que el pedido desaparece de la lista de pendientes
```

---

## **2.5. Prototipar**

_Esta etapa se integra con la fase de Construir del ciclo Lean Startup. Los wireframes representan el experimento mínimo de validación._

### **2.5.1. Wireframes de baja fidelidad**

Los wireframes se centran en la funcionalidad y la disposición de los elementos para evitar distracciones visuales durante la validación de usabilidad. El prototipo interactivo simula la navegación entre el Dashboard, la gestión de pedidos y el control de inventario.

---

**Wireframe 1: Dashboard General**
Disposición de widgets informativos en la parte superior y menú lateral persistente para navegación rápida.

**Wireframe 2: Gestión de Pedidos y Modal de Registro**
Tabla limpia con estados diferenciados por colores y un modal centrado con campos claros para la entrada de datos.

**Wireframe 3: Control de Inventario y Planificación de Entregas**
Tabla de stock con resaltado en rojo para productos bajo el mínimo y tarjetas simplificadas para el repartidor optimizadas para lectura móvil.

---

## **2.6. Testear**

### **2.6.1. Plan de pruebas de usabilidad moderadas basadas en tareas**

Se diseñan pruebas donde el moderador observa al usuario interactuar con el prototipo sin intervenir, registrando el tiempo y la facilidad de completación.

**Perfil de participantes:** 3 usuarios simulados externos al equipo, representando los roles de Vendedor, Encargado de Almacén y Repartidor.

**Responsables de la sesión:** Sofía Rojas (moderadora) y Carlos Ruiz (registro de métricas).

**Métricas fijas aplicadas en cada tarea:**

| Métrica | Descripción | Instrumento |
| :--- | :--- | :--- |
| **Completación sin ayuda** | El usuario llega al fin de la tarea sin preguntar ni solicitar ayuda al moderador. | Observación directa |
| **Tiempo de tarea** | Tiempo invertido desde el inicio hasta la completación de la tarea (Segundos/Minutos). | Cronómetro |
| **Satisfacción** | Pregunta post-tarea sobre facilidad de uso (escala de 1 a 5). | Encuesta post-tarea |

---

**Tarea 1: Vendedor - Registro de nuevo pedido**
Participante: Representante del rol de Vendedor

> _"Registra un pedido del producto 'Sala Moderna' para un cliente nuevo en el sistema."_

| Métrica | Criterio de éxito |
| :--- | :--- |
| Completación sin ayuda | Completa la tarea de principio a fin sin solicitar ayuda. |
| Tiempo de tarea | ≤ 3 minutos. |
| Satisfacción | Puntaje ≥ 4 / 5. |

---

**Tarea 2: Almacén - Gestión de inventario crítico**
Participante: Representante del rol de Encargado de Almacén

> _"Identifica qué productos tienen stock crítico en el sistema y actualiza la cantidad de un producto específico."_

| Métrica | Criterio de éxito |
| :--- | :--- |
| Completación sin ayuda | Completa la tarea de principio a fin sin solicitar ayuda. |
| Tiempo de tarea | ≤ 3 minutos. |
| Satisfacción | Puntaje ≥ 4 / 5. |

---

**Tarea 3: Repartidor - Gestión de entregas**
Participante: Representante del rol de Repartidor

> _"Localiza la dirección de la primera entrega del día en tu panel y marca el pedido como entregado."_

| Métrica | Criterio de éxito |
| :--- | :--- |
| Completación sin ayuda | Completa la tarea de principio a fin sin solicitar ayuda. |
| Tiempo de tarea | ≤ 3 minutos. |
| Satisfacción | Puntaje ≥ 4 / 5. |
