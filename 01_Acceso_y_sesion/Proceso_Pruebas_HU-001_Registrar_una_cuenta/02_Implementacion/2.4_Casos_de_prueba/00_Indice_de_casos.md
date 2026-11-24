# Índice de casos y scripts · HU-001

[Volver al flujo](../../00_Flujo_metodologico.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Plantilla de caso](_Plantilla_Caso.md) · [Plantilla de script](../2.5_Scripts_de_prueba/_Plantilla_Script.md)

El **caso** define *qué* se comprueba. El **script** define *cómo* se comprueba, con pasos y puntos de verificación. Cada caso tiene un solo script con el mismo consecutivo.

| Orden | Caso | Nombre | Escenario | Prioridad | Script |
|---:|---|---|---|---|---|
| 3 | [ACC-REG-001](ACC-REG-001.md) | Registrar una cuenta válida con rol usuario | Básico (happy path) | Alta | [SCR-ACC-REG-001](../2.5_Scripts_de_prueba/SCR-ACC-REG-001.md) |
| 4 | [ACC-REG-002](ACC-REG-002.md) | Registrar una cuenta válida con rol soporte | Alterno (happy path) | Alta | [SCR-ACC-REG-002](../2.5_Scripts_de_prueba/SCR-ACC-REG-002.md) |
| 5 | [ACC-REG-003](ACC-REG-003.md) | Registrar una cuenta de administrador sin aprobación adicional | Alterno (happy path) | Alta | [SCR-ACC-REG-003](../2.5_Scripts_de_prueba/SCR-ACC-REG-003.md) |
| 1 | [ACC-REG-004](ACC-REG-004.md) | Consultar las opciones del campo Rol | Alterno | Media | [SCR-ACC-REG-004](../2.5_Scripts_de_prueba/SCR-ACC-REG-004.md) |
| 6 | [ACC-REG-005](ACC-REG-005.md) | Aceptar nombres de 3 y de 50 caracteres | Alterno (happy path) | Alta | [SCR-ACC-REG-005](../2.5_Scripts_de_prueba/SCR-ACC-REG-005.md) |
| 7 | [ACC-REG-006](ACC-REG-006.md) | Aceptar contraseñas de 8 y de 72 caracteres | Alterno (happy path) | Alta | [SCR-ACC-REG-006](../2.5_Scripts_de_prueba/SCR-ACC-REG-006.md) |
| 8 | [ACC-REG-007](ACC-REG-007.md) | Rechazar el registro con un correo que ya pertenece a una cuenta | Excepción (error path) | Alta | [SCR-ACC-REG-007](../2.5_Scripts_de_prueba/SCR-ACC-REG-007.md) |
| 9 | [ACC-REG-008](ACC-REG-008.md) | Rechazar el registro cuando falta un dato obligatorio | Excepción (error path) | Alta | [SCR-ACC-REG-008](../2.5_Scripts_de_prueba/SCR-ACC-REG-008.md) |
| 10 | [ACC-REG-009](ACC-REG-009.md) | Rechazar nombres de 2 y de 51 caracteres | Excepción (error path) | Alta | [SCR-ACC-REG-009](../2.5_Scripts_de_prueba/SCR-ACC-REG-009.md) |
| 11 | [ACC-REG-010](ACC-REG-010.md) | Rechazar correos con formato inválido | Excepción (error path) | Alta | [SCR-ACC-REG-010](../2.5_Scripts_de_prueba/SCR-ACC-REG-010.md) |
| 2 | [ACC-REG-011](ACC-REG-011.md) | Actualizar la lista de condiciones mientras se escribe y corrige la contraseña | Alterno | Alta | [SCR-ACC-REG-011](../2.5_Scripts_de_prueba/SCR-ACC-REG-011.md) |
| 12 | [ACC-REG-012](ACC-REG-012.md) | Rechazar contraseñas de 7 y de 73 caracteres | Excepción (error path) | Alta | [SCR-ACC-REG-012](../2.5_Scripts_de_prueba/SCR-ACC-REG-012.md) |
| 13 | [ACC-REG-013](ACC-REG-013.md) | Rechazar contraseñas con composición incompleta | Excepción (error path) | Alta | [SCR-ACC-REG-013](../2.5_Scripts_de_prueba/SCR-ACC-REG-013.md) |
| 14 | [ACC-REG-014](ACC-REG-014.md) | Rechazar contraseñas que contienen espacios | Excepción (error path) | Media | [SCR-ACC-REG-014](../2.5_Scripts_de_prueba/SCR-ACC-REG-014.md) |
| 15 | [ACC-REG-015](ACC-REG-015.md) | Rechazar una contraseña que contiene el nombre | Excepción (error path) | Media | [SCR-ACC-REG-015](../2.5_Scripts_de_prueba/SCR-ACC-REG-015.md) |
| 16 | [ACC-REG-016](ACC-REG-016.md) | Rechazar la cuarta solicitud de registro dentro del mismo minuto | Excepción (error path) | Alta | [SCR-ACC-REG-016](../2.5_Scripts_de_prueba/SCR-ACC-REG-016.md) |
| 17 | [ACC-REG-017](ACC-REG-017.md) | Iniciar sesión con la cuenta recién registrada | Alterno (integración) | Alta | [SCR-ACC-REG-017](../2.5_Scripts_de_prueba/SCR-ACC-REG-017.md) |
| 18 | [ACC-REG-018](ACC-REG-018.md) | Proteger la contraseña en la respuesta y en el almacenamiento | Calidad | Alta | [SCR-ACC-REG-018](../2.5_Scripts_de_prueba/SCR-ACC-REG-018.md) |
| 19 | [ACC-REG-019](ACC-REG-019.md) | Completar el registro solo con teclado | Calidad | Media | [SCR-ACC-REG-019](../2.5_Scripts_de_prueba/SCR-ACC-REG-019.md) |
| 20 | [ACC-REG-020](ACC-REG-020.md) | Identificar campos, condiciones y errores con lector de pantalla | Calidad | Media | [SCR-ACC-REG-020](../2.5_Scripts_de_prueba/SCR-ACC-REG-020.md) |
| 21 | [ACC-REG-021](ACC-REG-021.md) | Leer y operar el registro en computador y teléfono | Calidad | Media | [SCR-ACC-REG-021](../2.5_Scripts_de_prueba/SCR-ACC-REG-021.md) |

Total: **21 casos** y **21 scripts**.
