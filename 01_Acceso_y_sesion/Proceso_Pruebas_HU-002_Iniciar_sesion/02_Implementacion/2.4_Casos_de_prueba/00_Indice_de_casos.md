# Índice de casos y scripts · HU-002

[Volver al flujo](../../00_Flujo_metodologico.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Plantilla de caso](_Plantilla_Caso.md) · [Plantilla de script](../2.5_Scripts_de_prueba/_Plantilla_Script.md)

El **caso** define *qué* se comprueba. El **script** define *cómo* se comprueba, con pasos y puntos de verificación. Cada caso tiene un solo script con el mismo consecutivo.

| Orden | Caso | Nombre | Escenario | Prioridad | Script |
|---:|---|---|---|---|---|
| 1 | [ACC-ING-001](ACC-ING-001.md) | Iniciar sesión con credenciales válidas de una cuenta activa | Básico (happy path) | Alta | [SCR-ACC-ING-001](../2.5_Scripts_de_prueba/SCR-ACC-ING-001.md) |
| 2 | [ACC-ING-002](ACC-ING-002.md) | Iniciar sesión con una cuenta activa de rol administrador | Alterno (happy path) | Alta | [SCR-ACC-ING-002](../2.5_Scripts_de_prueba/SCR-ACC-ING-002.md) |
| 3 | [ACC-ING-003](ACC-ING-003.md) | Abrir la pantalla protegida solicitada después de iniciar sesión | Alterno | Alta | [SCR-ACC-ING-003](../2.5_Scripts_de_prueba/SCR-ACC-ING-003.md) |
| 4 | [ACC-ING-004](ACC-ING-004.md) | Rechazar el ingreso con un correo que no pertenece a ninguna cuenta | Excepción (error path) | Alta | [SCR-ACC-ING-004](../2.5_Scripts_de_prueba/SCR-ACC-ING-004.md) |
| 5 | [ACC-ING-005](ACC-ING-005.md) | Rechazar el ingreso con contraseña incorrecta y mostrar el mismo mensaje que con correo inexistente | Excepción (error path) | Alta | [SCR-ACC-ING-005](../2.5_Scripts_de_prueba/SCR-ACC-ING-005.md) |
| 6 | [ACC-ING-006](ACC-ING-006.md) | Rechazar el ingreso de una cuenta inactiva aunque las credenciales sean correctas | Excepción (error path) | Alta | [SCR-ACC-ING-006](../2.5_Scripts_de_prueba/SCR-ACC-ING-006.md) |
| 7 | [ACC-ING-007](ACC-ING-007.md) | Rechazar la sexta solicitud de ingreso dentro del mismo minuto | Excepción (error path) | Alta | [SCR-ACC-ING-007](../2.5_Scripts_de_prueba/SCR-ACC-ING-007.md) |
| 8 | [ACC-ING-008](ACC-ING-008.md) | No mostrar la contraseña en la respuesta de un ingreso aceptado ni de uno rechazado | Calidad | Alta | [SCR-ACC-ING-008](../2.5_Scripts_de_prueba/SCR-ACC-ING-008.md) |
| 9 | [ACC-ING-009](ACC-ING-009.md) | Comprobar que la contraseña no queda en texto legible en los registros almacenados | Calidad | Alta | [SCR-ACC-ING-009](../2.5_Scripts_de_prueba/SCR-ACC-ING-009.md) |
| 10 | [ACC-ING-010](ACC-ING-010.md) | Comprobar que el ingreso no otorga funciones ajenas al rol de la cuenta | Calidad | Alta | [SCR-ACC-ING-010](../2.5_Scripts_de_prueba/SCR-ACC-ING-010.md) |
| 11 | [ACC-ING-011](ACC-ING-011.md) | Iniciar sesión usando solo el teclado | Calidad | Media | [SCR-ACC-ING-011](../2.5_Scripts_de_prueba/SCR-ACC-ING-011.md) |
| 12 | [ACC-ING-012](ACC-ING-012.md) | Anunciar los campos y el error de ingreso con lector de pantalla | Calidad | Media | [SCR-ACC-ING-012](../2.5_Scripts_de_prueba/SCR-ACC-ING-012.md) |
| 13 | [ACC-ING-013](ACC-ING-013.md) | Iniciar sesión en computador y en teléfono | Calidad | Media | [SCR-ACC-ING-013](../2.5_Scripts_de_prueba/SCR-ACC-ING-013.md) |

Total: **13 casos** y **13 scripts**.
