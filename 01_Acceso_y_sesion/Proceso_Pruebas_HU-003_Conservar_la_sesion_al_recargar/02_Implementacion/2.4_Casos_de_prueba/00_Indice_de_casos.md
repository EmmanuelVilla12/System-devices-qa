# Índice de casos y scripts · HU-003

[Volver al flujo](../../00_Flujo_metodologico.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Plantilla de caso](_Plantilla_Caso.md) · [Plantilla de script](../2.5_Scripts_de_prueba/_Plantilla_Script.md)

El **caso** define *qué* se comprueba. El **script** define *cómo* se comprueba, con pasos y puntos de verificación. Cada caso tiene un solo script con el mismo consecutivo.

| Orden | Caso | Nombre | Escenario | Prioridad | Script |
|---:|---|---|---|---|---|
| 1 | [ACC-REC-001](ACC-REC-001.md) | Conservar la identidad al recargar una pantalla protegida con sesión vigente | Básico (happy path) | Alta | [SCR-ACC-REC-001](../2.5_Scripts_de_prueba/SCR-ACC-REC-001.md) |
| 2 | [ACC-REC-002](ACC-REC-002.md) | Mantener las funciones permitidas del rol después de recargar | Alterno | Alta | [SCR-ACC-REC-002](../2.5_Scripts_de_prueba/SCR-ACC-REC-002.md) |
| 3 | [ACC-REC-003](ACC-REC-003.md) | No conceder permisos adicionales al recargar | Alterno | Alta | [SCR-ACC-REC-003](../2.5_Scripts_de_prueba/SCR-ACC-REC-003.md) |
| 4 | [ACC-REC-004](ACC-REC-004.md) | Conservar la sesión al recargar sin ampliar su momento de caducidad | Alterno | Alta | [SCR-ACC-REC-004](../2.5_Scripts_de_prueba/SCR-ACC-REC-004.md) |
| 7 | [ACC-REC-005](ACC-REC-005.md) | Cerrar la sesión y pedir un nuevo ingreso al recargar con la sesión caducada | Excepción (error path) | Alta | [SCR-ACC-REC-005](../2.5_Scripts_de_prueba/SCR-ACC-REC-005.md) |
| 6 | [ACC-REC-006](ACC-REC-006.md) | Cerrar la sesión al recargar cuando el servicio la rechaza como inválida | Excepción (error path) | Alta | [SCR-ACC-REC-006](../2.5_Scripts_de_prueba/SCR-ACC-REC-006.md) |
| 5 | [ACC-REC-007](ACC-REC-007.md) | Usar con teclado los controles de la pantalla recargada | Calidad | Media | [SCR-ACC-REC-007](../2.5_Scripts_de_prueba/SCR-ACC-REC-007.md) |
| 8 | [ACC-REC-008](ACC-REC-008.md) | Mantener legible y utilizable la pantalla recargada en computador y teléfono | Calidad | Media | [SCR-ACC-REC-008](../2.5_Scripts_de_prueba/SCR-ACC-REC-008.md) |

Total: **8 casos** y **8 scripts**.
