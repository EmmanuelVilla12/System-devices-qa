# SCR-ACC-INV-002 · Sesión rechazada como inválida

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-INV-002.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-INV-002 |
| Descripción | Pasos y puntos de verificación para comprobar: cerrar sesión por invalidación del servicio y solicitar nuevo ingreso. |
| Caso asociado | [ACC-INV-002](../2.4_Casos_de_prueba/ACC-INV-002.md) · CA-HU-006-02 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-002 de [2.3 Datos](../../02_Implementacion/2.3_Datos_de_prueba.md) (solo datos ficticios). Confirmar que la aplicación tiene la sesión registrada pero el servicio la declara inválida. |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---|---|---|---|
| 1 | Paso | Abrir aplicación sin sesión iniciada. | Se muestra la pantalla de login o bien la función protegida con requerimiento de sesión. |
| 2 | Paso | Intentar acceso a una función protegida; la aplicación tiene sesión registrada pero el servicio la declara inválida. | El sistema finaliza la sesión registrada y muestra respuesta de autorización fallida. |
| 3 | Verificación | Revisar el cuerpo de la respuesta y los headers. | La sesión marcada como invalidada por el servicio; ausencia de token activo. |
| 4 | Verificación | Verificar que los datos locales (carro, formulario) han sido limpiados. | No hay datos locales persistentes; el estado es "limpio". |
| 5 | Verificación | Buscar el mensaje «Inicie sesión nuevamente» en la respuesta. | El mensaje está presente, identificado y legible en computador (1366×768). |
| 6 | Verificación | Ejecutar la misma prueba en teléfono (emulación 390×844). | El mensaje «Inicie sesión nuevamente» es visible y no cortado en el tamaño de teléfono. |
| 7 | Verificación | Ejecutar con lector de pantalla NVDA. | El lector anuncia el mensaje «Inicie sesión nuevamente». |

**Estado final esperado:** La sesión registrada ha sido finalizada. Los datos locales han sido limpiados. El mensaje «Inicie sesión nuevamente» es observable en computador y teléfono, y es legible con lector de pantalla.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).