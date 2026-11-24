# SCR-ACC-REG-005 · Aceptar nombres de 3 y de 50 caracteres

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REG-005.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REG-005 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que los nombres de exactamente 3 y 50 caracteres se aceptan y se muestran completos. |
| Caso asociado | [ACC-REG-005](../2.4_Casos_de_prueba/ACC-REG-005.md) · CA-HU-001-01 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-005A, D-005B de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Registro** sin sesión iniciada. | Se muestra el formulario con Nombre, Correo electrónico, Contraseña y Rol. |
| 2 | Paso | Escribir `Teo` en Nombre. | El campo muestra el valor escrito. |
| 3 | Paso | Escribir `teo.limite3@dsqa.test` en Correo electrónico. | El campo muestra el valor escrito. |
| 4 | Paso | Escribir `Bosque52` en Contraseña. | El campo oculta los caracteres. |
| 5 | Paso | Seleccionar `Usuario` en Rol. | El rol queda seleccionado. |
| 6 | Paso | Enviar el formulario. | El sistema procesa la solicitud. |
| 7 | Verificación | Revisar la respuesta. | Registro aceptado con nombre `Teo`. |
| 8 | Paso | Repetir los pasos 1 a 6 con D-005B. | El sistema procesa la segunda solicitud. |
| 9 | Verificación | Revisar la respuesta. | Registro aceptado; el nombre mostrado tiene 50 caracteres: `Ximena Alejandra Giraldo Cárdenas de Montoya Henao`. |

**Estado final esperado:** Existen las cuentas `teo.limite3@dsqa.test` y `nombre.cincuenta@dsqa.test`.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
