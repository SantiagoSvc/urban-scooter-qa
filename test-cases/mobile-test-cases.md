# Casos de prueba — Aplicación móvil (Android)

Entorno: Emulador de Android Studio
Módulos: Login, Pedidos, Modo sin conexión, Notificaciones, General
Total de casos: **35** — 21 pasaron, 7 fallaron, 7 bloqueados por funcionalidad no implementada

| ID | Módulo | Caso de prueba | Precondiciones | Pasos | Resultado esperado | Resultado | Bug |
|---|---|---|---|---|---|---|---|
| M1 | Login | Límite: Menor Login (1 char) | Pantalla login | Ingresar 1 carácter | Sale "Usuario o contraseña no válido" | FALLÓ | [KAN-16](https://santiagovalenciacortes.atlassian.net/browse/KAN-16) |
| M2 | Login | Límite: Mayor Login (11 chars) | Pantalla login | Ingresar 11 caracteres | Sale "Usuario o contraseña no válido" | FALLÓ | [KAN-17](https://santiagovalenciacortes.atlassian.net/browse/KAN-17) |
| M3 | Login | Límite: Menor Pass (<4 dígitos) | Pantalla login | Ingresar 3 dígitos | Sale "Usuario o contraseña no válido" | PASÓ | — |
| M4 | Login | Límite: Error Pass (=4 dígitos) | Pantalla login | Ingresar 4 dígitos incorrectos | Sale "Usuario o contraseña no válido" | FALLÓ | [KAN-18](https://santiagovalenciacortes.atlassian.net/browse/KAN-18) |
| M5 | Login | Login Exitoso | Pantalla login | Ingresar datos válidos | Ingresa a "Lista de pedidos" | PASÓ | — |
| M6 | Login | Clic "Iniciar sesión" sin datos | Pantalla login | Tocar botón sin credenciales | Muestra validación de campos | PASÓ | — |
| M7 | Login | Clic "Ok" en alerta de error | Alerta visible | Tocar botón "Ok" | Cierra ventana emergente | PASÓ | — |
| M8 | Login | Clic "Olvidé contraseña" | Pantalla login | Tocar enlace | Muestra: "Contacta gerencia: 0101" | PASÓ | — |
| M9 | Login | Clic "Ok" en alerta gerencia | Alerta visible | Tocar botón "Ok" | Cierra ventana emergente | PASÓ | — |
| M10 | Pedidos | Pestaña "Todos los pedidos" | Lista pedidos | Hacer click en pestaña | Muestra lista global de pedidos | PASÓ | — |
| M11 | Pedidos | Pestaña "Mis pedidos" | Lista pedidos | Hacer click en pestaña | Muestra solo mis pedidos | FALLÓ | [KAN-7](https://santiagovalenciacortes.atlassian.net/browse/KAN-7) |
| M12 | Pedidos | Cierre de sesión (imagen) | Perfil/Lista | Tocar icono cerrar sesión | Muestra confirmación de salida | PASÓ | — |
| M13 | Pedidos | Confirmar cierre "Sí" | Alerta cierre | Tocar "Sí" | Redirige a pantalla de login | PASÓ | — |
| M14 | Pedidos | Cancelar cierre "No" | Alerta cierre | Tocar "No" | Cierra alerta y sigue en app | PASÓ | — |
| M15 | Pedidos | Aceptar pedido (Lista global) | Pestaña "Todos" | Tocar "Aceptar" en tarjeta | Muestra alerta de confirmación | PASÓ | — |
| M16 | Pedidos | Confirmar aceptar "Sí" | Alerta aceptar | Tocar "Sí" | Pedido pasa a "Mis pedidos" | PASÓ | — |
| M17 | Pedidos | Cancelar aceptar "No" | Alerta aceptar | Tocar "No" | Cierra alerta, pedido sigue libre | PASÓ | — |
| M18 | Pedidos | Filtros (clic icono) | Lista pedidos | Tocar icono filtros | Abre modal de selección | PASÓ | — |
| M19 | Pedidos | Filtros (aplicar) | Modal filtros | Seleccionar filtro y dar OK | La lista se actualiza según filtro | PASÓ | — |
| M20 | Pedidos | Completar pedido (Mis Pedidos) | Pestaña "Mis" | Tocar "Completar" en tarjeta | Muestra alerta de confirmación | PASÓ | — |
| M21 | Pedidos | Confirmar completar "Sí" | Alerta completar | Tocar "Sí" | Pedido pasa a completados | PASÓ | — |
| M22 | Pedidos | Cancelar completar "No" | Alerta completar | Tocar "No" | Cierra alerta, pedido sigue activo | PASÓ | — |
| M23 | Offline | Ventana acceso Internet | Sin red | Verificar mensaje | Muestra el pop-up exacto: "Sin acceso a Internet" al realizar cualquier acción de red. | FALLÓ | [KAN-19](https://santiagovalenciacortes.atlassian.net/browse/KAN-19) |
| M24 | Offline | Ventana Diseño/UI | Sin red | Verificar diseño | El diseño del pop-up coincide con Figma y bloquea clics en elementos fuera del botón "Ok". | FALLÓ | [KAN-20](https://santiagovalenciacortes.atlassian.net/browse/KAN-20) |
| M25 | Offline | Clic "Ok" en alerta Offline | Alerta visible | Tocar "Ok" | Cierra la alerta y devuelve al usuario a la pantalla anterior sin procesar la acción de red. | FALLÓ | [KAN-21](https://santiagovalenciacortes.atlassian.net/browse/KAN-21) |
| M26 | Notif. | Límite: Recibir notif. 09:58 PM | App instalada | Esperar hora límite | La notificación NO debe aparecer (validar que el sistema espera hasta las 9:59 PM) | BLOQUEADO | [KAN-22](https://santiagovalenciacortes.atlassian.net/browse/KAN-22) |
| M27 | Notif. | Límite: Recibir notif. 09:59 PM | App instalada | Esperar hora límite | La notificación aparece con Título: '2 horas para el pedido', logo de la app y texto descriptivo | BLOQUEADO | [KAN-22](https://santiagovalenciacortes.atlassian.net/browse/KAN-22) |
| M28 | Notif. | Límite: Recibir notif. 10:00 PM | App instalada | Esperar hora límite | La notificación NO debe ser enviada (validar comportamiento tras cumplirse el tiempo) | BLOQUEADO | [KAN-22](https://santiagovalenciacortes.atlassian.net/browse/KAN-22) |
| M29 | Notif. | Apariencia y Texto | App instalada | Recibir notificación | Texto y diseño coinciden con UX/UI | BLOQUEADO | [KAN-22](https://santiagovalenciacortes.atlassian.net/browse/KAN-22) |
| M30 | Notif. | Interacción en uso | App abierta | Recibir notif. y hacer click | Navega al pedido indicado | BLOQUEADO | [KAN-22](https://santiagovalenciacortes.atlassian.net/browse/KAN-22) |
| M31 | Notif. | Interacción en inicio | App en inicio | Recibir notif. y hacer click | Navega al pedido indicado | BLOQUEADO | [KAN-22](https://santiagovalenciacortes.atlassian.net/browse/KAN-22) |
| M32 | Notif. | Interacción en reposo | Pantalla apagada | Recibir notif. y desbloquear | Abre directamente el pedido | BLOQUEADO | [KAN-22](https://santiagovalenciacortes.atlassian.net/browse/KAN-22) |
| M33 | General | Rotación de pantalla | App abierta | Rotar dispositivo | La app NO debe rotar (vertical) | PASÓ | — |
| M34 | General | Persistencia de sesión | Sesión iniciada | Cerrar y abrir app | Entra directo a "Lista" | PASÓ | — |
| M35 | General | Actualización (pull-to-refresh) | Todos pedidos | Deslizar hacia abajo | Lista sincroniza con servidor | PASÓ | — |
