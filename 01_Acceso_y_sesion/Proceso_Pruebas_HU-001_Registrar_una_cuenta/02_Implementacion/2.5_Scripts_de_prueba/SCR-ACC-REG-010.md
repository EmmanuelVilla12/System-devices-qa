# SCR-ACC-REG-010 · Rechazar correos con formato inválido

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REG-010.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REG-010 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que tres formatos de correo claramente inválidos se rechazan con el error junto al campo Correo. |
| Caso asociado | [ACC-REG-010](../2.4_Casos_de_prueba/ACC-REG-010.md) · CA-HU-001-03 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-010A, D-010B, D-010C de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Registro** sin sesión iniciada. | Se muestra el formulario con Nombre, Correo electrónico, Contraseña y Rol. |
| 2 | Paso | Escribir `Felipe Correa` en Nombre. | El campo muestra el valor escrito. |
| 3 | Paso | Escribir `felipe.correadsqa.test` en Correo electrónico. | El campo muestra el valor escrito. |
| 4 | Paso | Escribir `Bosque52` en Contraseña. | El campo oculta los caracteres. |
| 5 | Paso | Seleccionar `Usuario` en Rol. | El rol queda seleccionado. |
| 6 | Paso | Enviar el formulario. | El sistema procesa la solicitud. |
| 7 | Verificación | Revisar la respuesta. | Se rechaza; error junto a Correo electrónico. |
| 8 | Paso | Cambiar el correo a `felipe@@dsqa.test` y enviar. | El sistema procesa la solicitud. |
| 9 | Verificación | Revisar la respuesta. | Se rechaza; error junto a Correo electrónico. |
| 10 | Paso | Cambiar el correo a `@dsqa.test` y enviar. | El sistema procesa la solicitud. |
| 11 | Verificación | Revisar la respuesta. | Se rechaza; error junto a Correo electrónico. |

**Estado final esperado:** No existe ninguna cuenta a nombre de `Felipe Correa`.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
