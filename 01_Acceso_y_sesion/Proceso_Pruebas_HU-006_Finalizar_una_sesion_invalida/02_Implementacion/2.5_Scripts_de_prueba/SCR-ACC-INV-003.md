# SCR-ACC-INV-003 · Sin continuidad protegida

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-INV-003.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-INV-003 |
| Descripción | Pasos y puntos de verificación para comprobar: intentar recuperación de pantalla protegida después de cierre de sesión por invalidez. |
| Caso asociado | [ACC-INV-003](../2.4_Casos_de_prueba/ACC-INV-003.md) · CA-HU-006-03 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-003 de [2.3 Datos](../../02_Implementacion/2.3_Datos_de_prueba.md) (solo datos ficticios). Confirmar que la sesión fue cerrada por invalidez previamente. |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---|---|---|---|
| 1 | Paso | Abrir aplicación y intentar acceder directamente a una pantalla protegida (sin nueva sesión). | La pantalla no carga o es redirigida al flujo de login. |
| 2 | Paso | Verificar el mensaje mostrado en la pantalla protegida. | No se muestra el contenido de la pantalla protegida; solo se accede al área pública. |
| 3 | Verificación | Buscar el mensaje «Inicie sesión nuevamente» en la respuesta. | El mensaje está presente y indica que se requiere nueva identificación. |
| 4 | Verificación | Ejecutar la misma prueba en teléfono (emulación 390×844). | El mensaje «Inicie sesión nuevamente» es visible y no cortado en el tamaño de teléfono. |
| 5 | Verificación | Ejecutar con lector de pantalla NVDA. | El lector anuncia el mensaje «Se requiere iniciar sesión nuevamente». |

**Estado final esperado:** No se recupera el acceso a la pantalla protegida. El mensaje «Inicie sesión nuevamente» es observable, indicando que se requiere nueva identificación. La sesión no se restaura automáticamente.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).