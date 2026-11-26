# SCR-ACC-INV-005 · Mensaje identificable y legible (RNF-004 y RNF-005)

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-INV-005.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-INV-005 |
| Descripción | Pasos y puntos de verificación para comprobar: mensaje de sesión inválida es identificable y legible en computador y teléfono, y con lector de pantalla. |
| Caso asociado | [ACC-INV-005](../2.4_Casos_de_prueba/ACC-INV-005.md) · RNF-002, RNF-004, RNF-005 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-005 de [2.3 Datos](../../02_Implementacion/2.3_Datos_de_prueba.md) (solo datos ficticios). Confirmar que el usuario ha accedido a una función protegida con sesión inválida. Tener a disposición lector de pantalla NVDA y dos configuraciones de pantalla. |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---|---|---|---|
| 1 | Paso | Abrir aplicación con sesión inválida (después de ACC-INV-001 o ACC-INV-002). | Se muestra el mensaje de sesión inválida o requerimiento de nuevo ingreso. |
| 2 | Verificación | Medir y verificar el mensaje en computador (1366×768): contraste, tamaño de fuente, posición. | El mensaje "Inicie sesión nuevamente" tiene contraste suficiente, tamaño de fuente legible y no está cortado en el borde de la pantalla. |
| 3 | Verificación | Ejecutar en teléfono (emulación 390×844). | El mensaje "Inicie sesión nuevamente" es visible y no cortado en el tamaño de teléfono. |
| 4 | Verificación | Ejecutar con lector de pantalla NVDA en computador. | El lector anuncia "iniciar sesión nuevamente" o mensaje equivalente. |
| 5 | Verificación | Verificar que el mensaje no esté superpuesto por otros elementos UI. | El mensaje es completamente visible y distinguible. |

**Estado final esperado:** El mensaje "Inicie sesión nuevamente" es visible, identificado y legible en computador (1366×768) y teléfono (390×844), y es legible con lector de pantalla NVDA.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).