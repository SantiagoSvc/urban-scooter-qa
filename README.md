# Urban Scooter — Plan de QA completo

![Manual Testing](https://img.shields.io/badge/Manual_Testing-100_Cases-blue?style=for-the-badge)
![API Testing](https://img.shields.io/badge/API_Testing-Postman-orange?style=for-the-badge&logo=postman)
![Mobile](https://img.shields.io/badge/Mobile_Testing-Android-green?style=for-the-badge&logo=android)
![Jira](https://img.shields.io/badge/Defect_Tracking-Jira-0052CC?style=for-the-badge&logo=jira)

**Plan de aseguramiento de calidad para una aplicación de alquiler de scooters (web + Android).**
Pruebas manuales · Diseño de casos · Validación de API · Gestión de defectos en Jira

---

## Resumen del proyecto

| Ítem | Detalle |
|---|---|
| Aplicación | Urban Scooter — alquiler de scooters, web y app Android |
| Casos ejecutados | **100** — 41 web, 35 móvil, 24 API |
| Defectos | 43 hallazgos en 33 tickets de Jira |
| Técnicas | Clases de equivalencia, valores límite, pruebas exploratorias |
| Herramientas | Jira, Postman, Chrome DevTools, Emulador de Android Studio |

---

## Objetivo

Verificar que la aplicación de Urban Scooter cumpla con los requisitos funcionales antes
de su lanzamiento, con foco en los flujos que generan ingresos: registro de usuarios,
creación y gestión de pedidos, y comunicación entre la app y el backend.

El riesgo que se busca prevenir es que un pedido se pierda, se duplique o se asigne al
repartidor equivocado por un fallo de validación o de sincronización, y que un usuario
quede bloqueado en un estado ambiguo cuando pierde la conexión.

---

## Qué se probó

### Aplicación web — 41 revisiones
[`test-cases/web-checklist.md`](test-cases/web-checklist.md)

Página de inicio, formulario de pedido, validación de campos obligatorios, longitudes,
flujo completo de creación de pedido y comportamiento de la interfaz.
Ejecutado en **Chrome y Opera**.

### Validación de datos — 30 pruebas
[`test-cases/data-validation.md`](test-cases/data-validation.md)

Particiones de clases de equivalencia y análisis de valores límite sobre cada campo del
formulario: longitud mínima, máxima, valores dentro y fuera del rango, y tipo de dato.

### Aplicación móvil Android — 35 casos
[`test-cases/mobile-test-cases.md`](test-cases/mobile-test-cases.md)

Organizados por módulo: Login, Pedidos, Modo sin conexión, Notificaciones y General.
Cada caso documenta precondiciones, pasos, resultado esperado y resultado obtenido.
Ejecutado en emulador de Android Studio.

### API — 24 casos
[`api-testing/api-checklist.md`](api-testing/api-checklist.md)

Validación de endpoints con Postman: `/health`, `/stations`, creación de repartidores,
login, creación y cancelación de pedidos. Se verificaron códigos de estado 200, 201,
400, 401, 404 y los mensajes de error asociados.

### Defectos
[`bug-reports/bug-reports.md`](bug-reports/bug-reports.md)

---

## Técnicas de diseño aplicadas

| Técnica | Aplicada a |
|---|---|
| Particiones de clases de equivalencia | Campos del formulario — grupos de entrada válidos e inválidos |
| Análisis de valores límite | Longitud de nombre y apellido, formato de teléfono, rangos de fecha |
| Pruebas exploratorias | Casos borde fuera de los casos formales |
| Pruebas de estado | Transiciones de pedido: libre, aceptado, completado |

---

## Hallazgos destacados

**Modo sin conexión.** El pop-up de "Sin acceso a Internet" no coincide con el diseño
especificado y no bloquea la interacción con la pantalla de fondo, lo que deja la app en
un estado ambiguo para el usuario.

**Notificaciones.** Siete casos quedaron marcados como *bloqueados* en lugar de fallidos:
la funcionalidad no está implementada en la API ni en la aplicación, por lo que la prueba
no se puede ejecutar. Se documentaron igualmente para dejar constancia de la cobertura
pendiente y evitar que se den por cubiertos en un ciclo posterior.

**Valores límite en login.** El mensaje de error no se comporta según el requisito en los
límites de longitud de usuario y contraseña.

---

## Estructura del repositorio

```
urban-scooter-qa/
├── test-cases/
│   ├── urban-scooter-test-cases.xlsx   Documento completo del plan de pruebas
│   ├── web-checklist.md                41 revisiones de la aplicación web
│   ├── data-validation.md              30 pruebas de clases de equivalencia y límites
│   └── mobile-test-cases.md            35 casos de la aplicación Android
├── api-testing/
│   └── api-checklist.md                24 casos de validación de endpoints
├── bug-reports/
│   └── bug-reports.md                  Defectos encontrados y referencia en Jira
└── README.md
```

> Los defectos se registraron en un proyecto de Jira privado. Las tablas de este
> repositorio incluyen la referencia de cada ticket; las capturas de pantalla se pueden
> compartir a solicitud.

---

## Autor

**Santiago Valencia Cortés** — Ingeniero QA
Ingeniero Mecatrónico orientado a QA manual y automatización de pruebas.

GitHub: <https://github.com/SantiagoSvc> · LinkedIn: <https://linkedin.com/in/santivacomecatronica>
