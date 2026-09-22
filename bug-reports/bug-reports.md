# Reporte de defectos

Todos los defectos encontrados se registraron en Jira durante la ejecución del plan
de pruebas. Cada ticket contiene título, pasos de reproducción, resultado esperado,
resultado obtenido y evidencia.

> **Nota:** el proyecto de Jira es privado. Esta tabla resume los defectos y su
> referencia; las capturas de pantalla se pueden compartir a solicitud.

Hallazgos registrados: **43** en 33 tickets de Jira (algunos defectos afectan a varios casos de prueba).

| Área | Referencia | Descripción | Ticket |
|---|---|---|---|
| Web | 5 | Apellido: Validar longitud (rangos 1, 2, 15, 16). | [KAN-1](https://santiagovalenciacortes.atlassian.net/browse/KAN-1) |
| Web | 6 | Dirección: Validar longitud (rangos 4, 5, 50, 51). | [KAN-2](https://santiagovalenciacortes.atlassian.net/browse/KAN-2) |
| Web | 7 | Teléfono: Validar longitud (rangos 9, 10, 12, 13). | [KAN-3](https://santiagovalenciacortes.atlassian.net/browse/KAN-3) |
| Web | 8 | Pedido: Validar botón 'Pedir' genera ID único. | [KAN-5](https://santiagovalenciacortes.atlassian.net/browse/KAN-5) |
| Web | 11 | Encabezado: Validar búsqueda presionando la tecla "Enter" con un número de pedido existente. | [KAN-10](https://santiagovalenciacortes.atlassian.net/browse/KAN-10) |
| Web | 14 | Encabezado: Validar búsqueda consecutiva (buscar un pedido e inmediatamente buscar otro diferente). | [KAN-11](https://santiagovalenciacortes.atlassian.net/browse/KAN-11) |
| Web | 15 | Datos: Validar el valor en "Fecha de entrega". Esperado: Muestra fecha de entrega (Bug: muestra fecha fin de alquiler). | [KAN-6](https://santiagovalenciacortes.atlassian.net/browse/KAN-6) |
| Web | 16 | Datos: Validar truncamiento en "Comentario" con texto largo. Esperado: Máximo 2 líneas (Bug: desborda el diseño). | [KAN-7](https://santiagovalenciacortes.atlassian.net/browse/KAN-7) |
| Web | 17 | Estados: Validar el cálculo correcto de la fecha "fin de alquiler" para diferentes periodos (ej. 2 días, 4 días). | [KAN-12](https://santiagovalenciacortes.atlassian.net/browse/KAN-12) |
| Web | 20 | Cancelación: Validar regla de negocio (Back-end) que impide cancelar pedidos ya entregados. | [KAN-13](https://santiagovalenciacortes.atlassian.net/browse/KAN-13) |
| Web | 21 | Cancelar: Validar persistencia verificando que una orden eliminada no puede ser buscada nuevamente. | [KAN-14](https://santiagovalenciacortes.atlassian.net/browse/KAN-14) |
| Web | 26 | API: Eliminar repartidor (Delete) con pedidos activos. | [KAN-15](https://santiagovalenciacortes.atlassian.net/browse/KAN-15) |
| Web | 31 | Interfaz: Validar funcionalidad botón "Yes" en modal. | [KAN-5](https://santiagovalenciacortes.atlassian.net/browse/KAN-5) |
| Web | 34 | Estados: Validar visualización de nombre de repartidor (largo máximo) sin truncar. | [KAN-28](https://santiagovalenciacortes.atlassian.net/browse/KAN-28) |
| Web | 35 | Estados: Validar transición "Llegó": estado activo y cambio de número a "tick". | [KAN-29](https://santiagovalenciacortes.atlassian.net/browse/KAN-29) |
| Web | 36 | Estados: Validar transición "Paseo": activa al confirmar finalización. | [KAN-30](https://santiagovalenciacortes.atlassian.net/browse/KAN-30) |
| Web | 40 | Cancelación: Validar UI: botón "Cancelar" se deshabilita/oculta tras iniciar la entrega. | [KAN-26](https://santiagovalenciacortes.atlassian.net/browse/KAN-26) |
| Web | 41 | Cancelación: Validar UI: mensaje de confirmación de cancelación (coherencia con el estado real). | [KAN-27](https://santiagovalenciacortes.atlassian.net/browse/KAN-27) |
| Web / datos | Apellido — Longitud (FUERA) | Error | [KAN-1](https://santiagovalenciacortes.atlassian.net/browse/KAN-1) |
| Web / datos | Dirección — Longitud (Límite Sup) | Éxito | [KAN-2](https://santiagovalenciacortes.atlassian.net/browse/KAN-2) |
| Web / datos | Dirección — Caracteres Especiales | Éxito | [KAN-31](https://santiagovalenciacortes.atlassian.net/browse/KAN-31) |
| Web / datos | Fecha Entrega — Obligatoriedad | Error | [KAN-32](https://santiagovalenciacortes.atlassian.net/browse/KAN-32) |
| Web / datos | Fecha Entrega — Formato (Inválido) | Error | [KAN-33](https://santiagovalenciacortes.atlassian.net/browse/KAN-33) |
| Web / datos | Período — Obligatoriedad | Error | [KAN-34](https://santiagovalenciacortes.atlassian.net/browse/KAN-34) |
| Web / datos | Período — Fuera | Error | [KAN-35](https://santiagovalenciacortes.atlassian.net/browse/KAN-35) |
| Móvil | M1 — Límite: Menor Login (1 char) | Sale "Usuario o contraseña no válido" | [KAN-16](https://santiagovalenciacortes.atlassian.net/browse/KAN-16) |
| Móvil | M2 — Límite: Mayor Login (11 chars) | Sale "Usuario o contraseña no válido" | [KAN-17](https://santiagovalenciacortes.atlassian.net/browse/KAN-17) |
| Móvil | M4 — Límite: Error Pass (=4 dígitos) | Sale "Usuario o contraseña no válido" | [KAN-18](https://santiagovalenciacortes.atlassian.net/browse/KAN-18) |
| Móvil | M11 — Pestaña "Mis pedidos" | Muestra solo mis pedidos | [KAN-7](https://santiagovalenciacortes.atlassian.net/browse/KAN-7) |
| Móvil | M23 — Ventana acceso Internet | Muestra el pop-up exacto: "Sin acceso a Internet" al realizar cualquier acción de red. | [KAN-19](https://santiagovalenciacortes.atlassian.net/browse/KAN-19) |
| Móvil | M24 — Ventana Diseño/UI | El diseño del pop-up coincide con Figma y bloquea clics en elementos fuera del botón "Ok". | [KAN-20](https://santiagovalenciacortes.atlassian.net/browse/KAN-20) |
| Móvil | M25 — Clic "Ok" en alerta Offline | Cierra la alerta y devuelve al usuario a la pantalla anterior sin procesar la acción de red. | [KAN-21](https://santiagovalenciacortes.atlassian.net/browse/KAN-21) |
| Móvil | M26 — Límite: Recibir notif. 09:58 PM | La notificación NO debe aparecer (validar que el sistema espera hasta las 9:59 PM) | [KAN-22](https://santiagovalenciacortes.atlassian.net/browse/KAN-22) |
| Móvil | M27 — Límite: Recibir notif. 09:59 PM | La notificación aparece con Título: '2 horas para el pedido', logo de la app y texto descriptivo | [KAN-22](https://santiagovalenciacortes.atlassian.net/browse/KAN-22) |
| Móvil | M28 — Límite: Recibir notif. 10:00 PM | La notificación NO debe ser enviada (validar comportamiento tras cumplirse el tiempo) | [KAN-22](https://santiagovalenciacortes.atlassian.net/browse/KAN-22) |
| Móvil | M29 — Apariencia y Texto | Texto y diseño coinciden con UX/UI | [KAN-22](https://santiagovalenciacortes.atlassian.net/browse/KAN-22) |
| Móvil | M30 — Interacción en uso | Navega al pedido indicado | [KAN-22](https://santiagovalenciacortes.atlassian.net/browse/KAN-22) |
| Móvil | M31 — Interacción en inicio | Navega al pedido indicado | [KAN-22](https://santiagovalenciacortes.atlassian.net/browse/KAN-22) |
| Móvil | M32 — Interacción en reposo | Abre directamente el pedido | [KAN-22](https://santiagovalenciacortes.atlassian.net/browse/KAN-22) |
| API | A15 — PUT /cancel | Error: Cancelar pedido no aceptado | [KAN-23](https://santiagovalenciacortes.atlassian.net/browse/KAN-23) |
| API | A16 — PUT /cancel | Error: Cancelar pedido que no existe | [KAN-24](https://santiagovalenciacortes.atlassian.net/browse/KAN-24) |
| API | A20 — GET /ordersCount | Obtener número de pedidos completados | [KAN-9](https://santiagovalenciacortes.atlassian.net/browse/KAN-9) |
| API | A21 — DELETE /courier | Eliminar repartidor: Con pedidos asociados | [KAN-25](https://santiagovalenciacortes.atlassian.net/browse/KAN-25) |

## Defectos destacados

**Modo sin conexión (M23–M25).** El pop-up de "Sin acceso a Internet" no coincide con
el diseño de Figma y no bloquea la interacción con la pantalla de fondo. Es el grupo de
defectos con mayor impacto en la experiencia del usuario, porque deja la aplicación en
un estado ambiguo.

**Notificaciones (M26–M32).** Siete casos quedaron marcados como *bloqueados* y no como
fallidos: la funcionalidad de notificaciones no está implementada en la API ni en la
aplicación, de modo que no es posible ejecutar la prueba. Se documentaron igualmente para
dejar constancia de la cobertura pendiente.

**Límites del formulario de login (M1, M2, M4).** El mensaje de error no se comporta como
especifica el requisito en los valores límite de longitud de usuario y contraseña.
