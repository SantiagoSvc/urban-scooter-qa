# Validación de datos — Clases de equivalencia y valores límite

Técnicas aplicadas: particiones de clases de equivalencia y análisis de valores límite
sobre los campos del formulario de pedido.

Total de pruebas: **30** — 23 pasaron, 7 fallaron

| Campo | Clase de equivalencia | Valores de prueba | Resultado esperado | Resultado | Bug |
|---|---|---|---|---|---|
| Nombre | Longitud (Límite Inf) | 2 | Éxito | PASÓ | — |
| Nombre | Longitud (Dentro) | 8 | Éxito | PASÓ | — |
| Nombre | Longitud (Límite Sup) | 15 | Éxito | PASÓ | — |
| Nombre | Longitud (Fuera Sup) | 16 | Error | PASÓ | — |
| Nombre | Tipo (Alfanumérico) | 12345 | Error | PASÓ | — |
| Apellido | Longitud (Límite Inf) | 2 | Éxito | PASÓ | — |
| Apellido | Longitud (Fuera Inf) | 1 | Error | PASÓ | — |
| Apellido | Longitud (Dentro) | 5 | Éxito | PASÓ | — |
| Apellido | Longitud (Límite Sup) | 15 | Éxito | PASÓ | — |
| Apellido | Longitud (FUERA) | 16 | Error | FALLÓ | [KAN-1](https://santiagovalenciacortes.atlassian.net/browse/KAN-1) |
| Apellido | Tipo (Alfanumérico) | 123@ | Error | PASÓ | — |
| Dirección | Longitud (Límite Inf) | 5 | Éxito | PASÓ | — |
| Dirección | Longitud (Límite Sup) | 50 | Éxito | FALLÓ | [KAN-2](https://santiagovalenciacortes.atlassian.net/browse/KAN-2) |
| Dirección | Longitud (Fuera Sup) | 51 | Error | PASÓ | — |
| Dirección | Caracteres Especiales | #, -, . | Éxito | FALLÓ | [KAN-31](https://santiagovalenciacortes.atlassian.net/browse/KAN-31) |
| Teléfono | Longitud (Límite Inf) | 10 | Éxito | PASÓ | — |
| Teléfono | Longitud (Límite Sup) | 12 | Éxito | PASÓ | — |
| Teléfono | Tipo (Inválido) | ABCDEFGHIJ | Error | PASÓ | — |
| Teléfono | Caracteres Especiales | #, -, . | Error | PASÓ | — |
| Fecha Entrega | Obligatoriedad | Vacío | Error | FALLÓ | [KAN-32](https://santiagovalenciacortes.atlassian.net/browse/KAN-32) |
| Fecha Entrega | Formato (Inválido) | Año pasado | Error | FALLÓ | [KAN-33](https://santiagovalenciacortes.atlassian.net/browse/KAN-33) |
| Fecha Entrega | Fecha actual (Hoy) | Fecha hoy | Éxito | PASÓ | — |
| Fecha Entrega | Fecha futura próxima | mañana | Éxito | PASÓ | — |
| Fecha Entrega | Formato de texto aleatorio | ABCD | Error | PASÓ | — |
| Fecha Entrega | Dato vacio | "deliveryDate": null | Error | PASÓ | — |
| Período | Obligatoriedad | Eliminar "rentTime" del body | Error | FALLÓ | [KAN-34](https://santiagovalenciacortes.atlassian.net/browse/KAN-34) |
| Período | Clase Válida | 1, 4, | Éxito | PASÓ | — |
| Período | Fuera | 2007 | Error | FALLÓ | [KAN-35](https://santiagovalenciacortes.atlassian.net/browse/KAN-35) |
| Color | Opcional | Vacío | Éxito | PASÓ | — |
| Comentario | Límite Máximo | 250 carac. | Éxito | PASÓ | — |
