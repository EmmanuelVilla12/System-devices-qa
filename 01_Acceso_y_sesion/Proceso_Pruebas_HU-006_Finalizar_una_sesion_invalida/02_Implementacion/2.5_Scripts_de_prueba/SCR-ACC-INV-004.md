# SCR-ACC-INV-004 · Rol insuficiente con sesión válida

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-INV-004.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-INV-004 |
| Descripción | Pasos y puntos de verificación para comprobar: sesión válida pero rol insuficiente -> acceso denegado, sin cerrar sesión. |
| Caso asociado | [ACC-INV-004](../2.4_Casos_de_prueba/ACC-INV-004.md) · CA-HU-006-04 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-004 de [2.3 Datos](../../02_Implementacion/2.3_Datos_de_prueba.md) (solo datos ficticios). Confirmar que la sesión está iniciada con rol soporte y la función requiere rol administrador. |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---|---|---|---|
| 1 | Paso | Abrir aplicación con sesión iniciada (rol soporte). | Se accede al área principal con el rol actual visible. |
| 2 | Paso | Solicitar una función protegida que requiere rol administrador o permisos superiores. | El sistema bloquea la operación y muestra respuesta de "Acceso denegado". |
| 3 | Verificación | Revisar que la sesión sigue activa después del rechazo. | El token de sesión sigue vigente; el usuario continúa en el área principal. |
| 4 | Verificación | Verificar que no se muestra el mensaje "Inicie sesión nuevamente". | No aparece el mensaje de nuevo ingreso; solo "Acceso denegado". |
| 5 | Verificación | Ejecutar la misma prueba en teléfono (emulación 390×844). | El mensaje "Acceso denegado" es visible y no cortado en el tamaño de teléfono. |
| 6 | Verificación | Ejecutar con lector de pantalla NVDA. | El lector anuncia "Acceso denegado" sin anunciar "inicie sesión nuevamente". |

**Estado final esperado:** La sesión permanece activa con el rol original. Se muestra "Acceso denegado" y la operación no se ejecuta. No se cierra la sesión ni se muestra el mensaje de nuevo ingreso.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).