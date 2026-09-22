# Checklist de pruebas — Aplicación web

Aplicación: **Urban Scooter** (web de alquiler de scooters)
Navegadores: Chrome y Opera
Total de revisiones: **41** — 23 pasaron, 18 fallaron

| ID | Revisión | Resultado | Navegador | Bug |
|---|---|---|---|---|
| 1 | Página de inicio: Validar título y plano del scooter. | PASÓ | Chrome / Opera | — |
| 2 | Página de inicio: Validar animación scroll y tablas. | PASÓ | Chrome / Opera | — |
| 3 | Formulario: Validar campos obligatorios en rojo. | PASÓ | Chrome / Opera | — |
| 4 | Nombre: Validar longitud (rangos 1, 2, 15, 16). | PASÓ | Chrome / Opera | — |
| 5 | Apellido: Validar longitud (rangos 1, 2, 15, 16). | FALLÓ | Chrome / Opera | [KAN-1](https://santiagovalenciacortes.atlassian.net/browse/KAN-1) |
| 6 | Dirección: Validar longitud (rangos 4, 5, 50, 51). | FALLÓ | Chrome / Opera | [KAN-2](https://santiagovalenciacortes.atlassian.net/browse/KAN-2) |
| 7 | Teléfono: Validar longitud (rangos 9, 10, 12, 13). | FALLÓ | Chrome / Opera | [KAN-3](https://santiagovalenciacortes.atlassian.net/browse/KAN-3) |
| 8 | Pedido: Validar botón 'Pedir' genera ID único. | FALLÓ | Chrome / Opera | [KAN-5](https://santiagovalenciacortes.atlassian.net/browse/KAN-5) |
| 9 | Encabezado: Validar visibilidad del botón "Estado del pedido" y despliegue del nuevo campo al seleccionarlo. | PASÓ | Chrome / Opera | — |
| 10 | Encabezado: Validar el ingreso de valores en el campo de búsqueda de pedido. | PASÓ | Chrome / Opera | — |
| 11 | Encabezado: Validar búsqueda presionando la tecla "Enter" con un número de pedido existente. | FALLÓ | Chrome / Opera | [KAN-10](https://santiagovalenciacortes.atlassian.net/browse/KAN-10) |
| 12 | Encabezado: Validar búsqueda presionando el botón "¡Vamos!" con un número de pedido existente. | PASÓ | Chrome / Opera | — |
| 13 | Encabezado: Validar búsqueda con un número de pedido inexistente. Esperado: Muestra pantalla de no encontrado. | PASÓ | Chrome / Opera | — |
| 14 | Encabezado: Validar búsqueda consecutiva (buscar un pedido e inmediatamente buscar otro diferente). | FALLÓ | Chrome / Opera | [KAN-11](https://santiagovalenciacortes.atlassian.net/browse/KAN-11) |
| 15 | Datos: Validar el valor en "Fecha de entrega". Esperado: Muestra fecha de entrega (Bug: muestra fecha fin de alquiler). | FALLÓ | Chrome / Opera | [KAN-6](https://santiagovalenciacortes.atlassian.net/browse/KAN-6) |
| 16 | Datos: Validar truncamiento en "Comentario" con texto largo. Esperado: Máximo 2 líneas (Bug: desborda el diseño). | FALLÓ | Chrome / Opera | [KAN-7](https://santiagovalenciacortes.atlassian.net/browse/KAN-7) |
| 17 | Estados: Validar el cálculo correcto de la fecha "fin de alquiler" para diferentes periodos (ej. 2 días, 4 días). | FALLÓ | Chrome / Opera | [KAN-12](https://santiagovalenciacortes.atlassian.net/browse/KAN-12) |
| 18 | Cancelar: Validar visibilidad del botón "Cancelar" y apertura del modal mostrando alternativas. | PASÓ | Chrome / Opera | — |
| 19 | Cancelar: Validar el funcionamiento independiente de las opciones "Sí, cancelar" y "No, volver" en el modal. | PASÓ | Chrome / Opera | — |
| 20 | Cancelación: Validar regla de negocio (Back-end) que impide cancelar pedidos ya entregados. | FALLÓ | Chrome / Opera | [KAN-13](https://santiagovalenciacortes.atlassian.net/browse/KAN-13) |
| 21 | Cancelar: Validar persistencia verificando que una orden eliminada no puede ser buscada nuevamente. | FALLÓ | Chrome / Opera | [KAN-14](https://santiagovalenciacortes.atlassian.net/browse/KAN-14) |
| 22 | Retraso: Validar criterios de retraso: el pedido pasa a esta categoría si la fecha/hora actual supera la pactada. | PASÓ | Chrome / Opera | — |
| 23 | Retraso: Validar cambios en la interfaz: los elementos se muestran en color rojo cuando el pedido está retrasado. | PASÓ | Chrome / Opera | — |
| 24 | API: Crear repartidor (Post) sin Login. | PASÓ | — | — |
| 25 | API: Crear repartidor (Post) sin Password. | PASÓ | — | — |
| 26 | API: Eliminar repartidor (Delete) con pedidos activos. | FALLÓ | — | [KAN-15](https://santiagovalenciacortes.atlassian.net/browse/KAN-15) |
| 27 | API: Eliminar repartidor (Delete) inexistente. | PASÓ | — | — |
| 28 | API: Cancelar pedido no aceptado (Put). | PASÓ | — | — |
| 29 | API: Cancelar pedido inexistente (Put). | PASÓ | — | — |
| 30 | API: Obtener pedidos por estación inexistente. | PASÓ | — | — |
| 31 | Interfaz: Validar funcionalidad botón "Yes" en modal. | FALLÓ | Chrome / Opera | [KAN-5](https://santiagovalenciacortes.atlassian.net/browse/KAN-5) |
| 32 | Estados: Validar activación automática de "En el almacén" tras crear el pedido. | PASÓ | Chrome / Opera | — |
| 33 | Estados: Validar transición "En camino": activa al aceptar y muestra nombre de repartidor. | PASÓ | Chrome / Opera | — |
| 34 | Estados: Validar visualización de nombre de repartidor (largo máximo) sin truncar. | FALLÓ | Chrome / Opera | [KAN-28](https://santiagovalenciacortes.atlassian.net/browse/KAN-28) |
| 35 | Estados: Validar transición "Llegó": estado activo y cambio de número a "tick". | FALLÓ | Chrome / Opera | [KAN-29](https://santiagovalenciacortes.atlassian.net/browse/KAN-29) |
| 36 | Estados: Validar transición "Paseo": activa al confirmar finalización. | FALLÓ | Chrome / Opera | [KAN-30](https://santiagovalenciacortes.atlassian.net/browse/KAN-30) |
| 37 | Estados: Validar exclusividad: solo un estado marcado como activo en todo momento. | PASÓ | Chrome / Opera | — |
| 38 | Atraso: Validar cambio a color rojo al superar 11:59 PM de fecha límite. | PASÓ | Chrome / Opera | — |
| 39 | Atraso: Validar cambio de texto a "El repartidor se retrasó" en estados atrasados. | PASÓ | Chrome / Opera | — |
| 40 | Cancelación: Validar UI: botón "Cancelar" se deshabilita/oculta tras iniciar la entrega. | FALLÓ | Chrome / Opera | [KAN-26](https://santiagovalenciacortes.atlassian.net/browse/KAN-26) |
| 41 | Cancelación: Validar UI: mensaje de confirmación de cancelación (coherencia con el estado real). | FALLÓ | Chrome / Opera | [KAN-27](https://santiagovalenciacortes.atlassian.net/browse/KAN-27) |
