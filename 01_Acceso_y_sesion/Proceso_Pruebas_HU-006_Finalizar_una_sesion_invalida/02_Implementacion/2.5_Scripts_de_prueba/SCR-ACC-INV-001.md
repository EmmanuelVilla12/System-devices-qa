# SCR-ACC-INV-001 · Sesión caducada — happy path

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-INV-001.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-INV-001 |
| Descripción | Pasos y puntos de verificación para comprobar: cerrar sesión por caducidad y solicitar nuevo ingreso. |
| Caso asociado | [ACC-INV-001](../2.4_Casos_de_prueba/ACC-INV-001.md) · CA-HU-006-01 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-001 de [2.3 Datos](../../02_Implementacion/2.3_Datos_de_prueba.md) (solo datos ficticios). Confirmar que la sesión ha expirado (TTL > 20 min inactiva). |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---|---|---|---|
| 1 | Paso | Abrir aplicación sin sesión iniciada. | Se muestra la pantalla de login o bien la función protegida con requerimiento de sesión. |
| 2 | Paso | Ingresar a una función protegida con sesión caducada (TTL expirado). | El sistema rechaza el acceso y muestra respuesta de autorización fallida. |
| 3 | Verificación | Revisar el cuerpo de la respuesta y los headers. | La sesión aparece con marca de caducidad o ausencia de token de sesión. |
| 4 | Verificación | Verificar que la sesión se ha cerrado automáticamente. | No hay sesión activa en el navegador; el token ha sido invalidado. |
| 5 | Verificación | Buscar el mensaje «Inicie sesión nuevamente» en la respuesta. | El mensaje está presente, identificado y legible en computador (1366×768). |
| 6 | Verificación | Ejecutar la misma prueba en teléfono (emulación 390×844). | El mensaje «Inicie sesión nuevamente» es visible y no cortado en el tamaño de teléfono. |
| 7 | Verificación | Ejecutar con lector de pantalla NVDA. | El lector anuncia el mensaje «Inicie sesión nuevamente». |

**Estado final esperado:** No hay sesión activa. El mensaje «Inicie sesión nuevamente» es observable en computador y teléfono, y es legible con lector de pantalla.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).