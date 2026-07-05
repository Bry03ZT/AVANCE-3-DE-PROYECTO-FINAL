A partir del contexto definido dentro de [contexto], crea un prototipo UI siguiendo EXACTAMENTE la arquitectura de información definida dentro de [arquitectura], y alineado con la protopersona descrita dentro de en [protopersona] para completar el taskflow dentro de en [taskflow].

## CONTEXTO, PROTOPERSONA Y TASKFLOW:

[contexto]
Sistema web básico de gestión logística para Mueblería J & M (tienda de muebles en Arequipa). El sistema debe centralizar el registro de pedidos, el control de inventario en tiempo real y la planificación de entregas a domicilio. El objetivo es eliminar el registro manual en cuadernos y la coordinación informal por WhatsApp. Interfaz responsiva optimizada para vendedores, almacén y repartidores.
[/contexto]

[protopersona]
```text
Nombre y apellido: Juan Pérez
Rol / tipo de usuario: Vendedor
Descripción del rol: Encargado de atender clientes en tienda y redes sociales, cerrar ventas y registrar pedidos.
Puntos de dolor: Registro manual propenso a errores, falta de visibilidad de stock en tiempo real, duplicidad de tareas.
Necesidades: Formulario de registro rápido, consulta de stock instantánea y confirmación de pedido digital.
```
[/protopersona]

[taskflow]
```text
Taskflow: Verificación de stock y registro de pedido (Happy Path)

Rol / tipo de usuario: Vendedor (Juan Pérez)

Objetivo del usuario dentro del sistema: Verificar el inventario desde el dashboard, consultar disponibilidad y registrar un nuevo pedido.

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
15. Mira una animación de éxito al guardar y cómo se cierra el modal automáticamente
16. Mira la Tabla de Pedidos actualizada con el nuevo registro en estado Pendiente
```
[/taskflow]

## REGLAS OBLIGATORIAS:

1. El prototipo debe representar visualmente el contexto definido en [contexto].

2. Respeta EXACTAMENTE:
   - la jerarquía
   - el orden
   - los niveles
     definidos en [arquitectura].

3. REGLA DE INTERPRETACIÓN:
   La arquitectura es un contrato estructural estricto.
   La creatividad debe aplicarse como “capa visual” sobre esa estructura.

   Antes de generar el prototipo, valida mentalmente que:
   - cada página existe solo si está definida
   - cada sección existe solo si está definida

4. ALINEACIÓN CON EL USUARIO Y FLUJO:
   El diseño debe priorizar la facilidad de uso y la eficiencia para la protopersona definida en [protopersona], facilitando la compleción del [taskflow]. Los elementos visuales y de interacción deben guiar al usuario a través del flujo sin fricción.

## REGLAS DE CREATIVIDAD PERMITIDA:

Usa una estética de fondo claro (light mode) con fondo blanco roto (off-white, ej. #FAFAFA o #F5F5F5) como color de fondo general de las vistas.

**Paleta de colores corporativa obligatoria:**
- **Color primario:** Rojo oscuro `#B71C1C` — usar en la barra de navegación, botones de acción principal, encabezados de sección y elementos destacados.
- **Color de acento:** Rojo medio `#D32F2F` — usar en hover de botones y estados activos.
- **Fondo general:** Blanco roto `#FAFAFA` — fondo de todas las vistas.
- **Texto principal:** Gris muy oscuro `#212121` — para máxima legibilidad.
- **Texto secundario:** Gris medio `#757575` — para etiquetas y metadatos.
- **Superficies / tarjetas:** Blanco puro `#FFFFFF` con sombra suave.
- **Estados de alerta de stock:** Rojo `#B71C1C` para agotado, Naranja `#E65100` para stock bajo, Verde `#2E7D32` para disponible.

Haz el diseño visualmente atractivo, moderno y creativo.

Puedes usar:
- animaciones
- microinteracciones
- transiciones
- gradientes suaves
- sombras
- tarjetas modernas
- efectos hover
- composición visual creativa
- tipografía moderna
- detalles visuales premium

Revisa y ajusta el contraste entre texto y fondo de cada elemento.

PERO sin romper la estructura definida en [arquitectura].

## ARQUITECTURA:

[arquitectura]
```text
Vista: Dashboard General
	Sección: Barra de navegación
		Link: Pedidos -> Vista: Gestión de Pedidos
		Link: Inventario -> Vista: Control de Inventario
		Link: Entregas -> Vista: Planificación de Entregas
		Link icon: Usuario (Perfil/Cerrar sesión)
	Sección: Resumen Operativo
		Widget: Pedidos Pendientes
		Widget: Productos con Stock Crítico
		Widget: Entregas Programadas para Hoy

Vista: Gestión de Pedidos
	Sección: Buscador de Pedidos
		Input: Buscar por Cliente o ID
	Sección: Botón "Nuevo Pedido" -> Modal: Registro de Pedido
	Sección: Tabla de Pedidos
		Columnas: ID, Cliente, Producto, Fecha, Estado
		Acción: Ver detalle / Cambiar estado

Modal: Registro de Pedido
	Campo: Nombre del Cliente
	Campo: Teléfono / Contacto
	Campo: Dirección de Entrega
	Selector: Producto (Muestra stock disponible)
	Campo: Cantidad
	Campo: Fecha/Hora acordada
	Botón: Guardar Pedido
	Botón: Cancelar

Vista: Control de Inventario
	Sección: Buscador de Productos
		Input: Buscar producto
	Sección: Tabla de Inventario
		Columnas: Producto, Categoría, Stock Actual, Stock Mínimo, Estado
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
			Botón: Marcar como Entregado
```
[/arquitectura]
