# Pruebas de API — Urban Scooter

Herramienta: **Postman**
Cobertura: endpoints de salud, estaciones, creación de repartidores, login,
creación y cancelación de pedidos.
Total de casos: **24** — 20 pasaron, 4 fallaron

| ID | Endpoint | Caso de prueba | Resultado | Bug |
|---|---|---|---|---|
| A1 | GET /health | Comprobar que el back-end responde | PASÓ | — |
| A2 | GET /stations | Buscar estaciones de metro | PASÓ | — |
| A3 | POST /courier | Crear repartidor: Login (2-10 letras) | PASÓ | — |
| A4 | POST /courier | Crear repartidor: Password (4 números) | PASÓ | — |
| A5 | POST /courier | Error: Sin enviar parámetro "login" | PASÓ | — |
| A6 | POST /courier | Error: Sin enviar parámetro "password" | PASÓ | — |
| A7 | POST /courier | Error: Login ya existente | PASÓ | — |
| A8 | POST /courier | Error: Datos vacíos o formato inválido | PASÓ | — |
| A9 | POST /orders | Crear pedido: Asignar número de seguimiento | PASÓ | — |
| A10 | GET /track | Recuperar datos de pedido mediante track | PASÓ | — |
| A11 | GET /track | Error: Consultar pedido que no existe | PASÓ | — |
| A12 | GET /track | Error: Consultar pedido sin código | PASÓ | — |
| A13 | PUT /accept | Repartidor acepta pedido (validar ID/track) | PASÓ | — |
| A14 | PUT /finish | Completar pedido (validar estados 2XX) | PASÓ | — |
| A15 | PUT /cancel | Error: Cancelar pedido no aceptado | FALLÓ | [KAN-23](https://santiagovalenciacortes.atlassian.net/browse/KAN-23) |
| A16 | PUT /cancel | Error: Cancelar pedido que no existe | FALLÓ | [KAN-24](https://santiagovalenciacortes.atlassian.net/browse/KAN-24) |
| A17 | PUT /cancel | Error: Cancelar pedido ya aceptado | PASÓ | — |
| A18 | PUT /cancel | Error: Cancelar pedido sin código | PASÓ | — |
| A19 | GET /orders | Recuperar lista de pedidos (estación/ID) | PASÓ | — |
| A20 | GET /ordersCount | Obtener número de pedidos completados | FALLÓ | [KAN-9](https://santiagovalenciacortes.atlassian.net/browse/KAN-9) |
| A21 | DELETE /courier | Eliminar repartidor: Con pedidos asociados | FALLÓ | [KAN-25](https://santiagovalenciacortes.atlassian.net/browse/KAN-25) |
| A22 | DELETE /courier | Eliminar repartidor: Sin pedidos asociados | PASÓ | — |
| A23 | DELETE /courier | Eliminar repartidor: Ya eliminado | PASÓ | — |
| A24 | DELETE /courier | Eliminar repartidor: No existe | PASÓ | — |
