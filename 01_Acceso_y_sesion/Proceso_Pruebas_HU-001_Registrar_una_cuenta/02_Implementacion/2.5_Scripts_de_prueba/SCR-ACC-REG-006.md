# SCR-ACC-REG-006 · Aceptar contraseñas de 8 y de 72 caracteres

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REG-006.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REG-006 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que contraseñas de exactamente 8 y 72 caracteres que cumplen las demás condiciones se aceptan. |
| Caso asociado | [ACC-REG-006](../2.4_Casos_de_prueba/ACC-REG-006.md) · CA-HU-001-01, CA-HU-001-04 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-006A, D-006B de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Registro** sin sesión iniciada. | Se muestra el formulario con Nombre, Correo electrónico, Contraseña y Rol. |
| 2 | Paso | Escribir `Wilson Tabares` en Nombre. | El campo muestra el valor escrito. |
| 3 | Paso | Escribir `wilson.ocho@dsqa.test` en Correo electrónico. | El campo muestra el valor escrito. |
| 4 | Paso | Escribir `Lago7Fri` en Contraseña. | El campo oculta los caracteres. |
| 5 | Verificación | Revisar la lista de condiciones antes de enviar. | Todas las condiciones aparecen cumplidas, incluida la longitud. |
| 6 | Paso | Seleccionar `Usuario` en Rol. | El rol queda seleccionado. |
| 7 | Paso | Enviar el formulario. | El sistema procesa la solicitud. |
| 8 | Verificación | Revisar la respuesta. | Registro aceptado. |
| 9 | Paso | Repetir los pasos 1 a 7 con D-006B (pegar PWD-72 desde 2.3). | El sistema procesa la segunda solicitud. |
| 10 | Verificación | Revisar la respuesta. | Registro aceptado. |

**Estado final esperado:** Existen las dos cuentas de Wilson Tabares.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
