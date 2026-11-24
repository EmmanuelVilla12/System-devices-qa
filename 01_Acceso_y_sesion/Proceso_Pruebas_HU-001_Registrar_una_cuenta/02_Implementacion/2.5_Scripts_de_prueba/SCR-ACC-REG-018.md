# SCR-ACC-REG-018 · Proteger la contraseña en la respuesta y en el almacenamiento

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REG-018.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REG-018 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que la contraseña no aparece en los datos de respuesta ni se guarda en texto legible. |
| Caso asociado | [ACC-REG-018](../2.4_Casos_de_prueba/ACC-REG-018.md) · CA-HU-001-01 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-018 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Registro** sin sesión iniciada. | Se muestra el formulario con Nombre, Correo electrónico, Contraseña y Rol. |
| 2 | Paso | Escribir `Natalia Pineda` en Nombre. | El campo muestra el valor escrito. |
| 3 | Paso | Escribir `natalia.pineda@dsqa.test` en Correo electrónico. | El campo muestra el valor escrito. |
| 4 | Paso | Escribir `Faro2026Luz` en Contraseña. | El campo oculta los caracteres. |
| 5 | Paso | Seleccionar `Usuario` en Rol. | El rol queda seleccionado. |
| 6 | Paso | Enviar el formulario. | El sistema procesa la solicitud. |
| 7 | Verificación | En el panel de red, abrir la respuesta del registro y buscar `Faro2026Luz`. | No hay coincidencias ni un campo de contraseña. |
| 8 | Verificación | Revisar los datos mostrados en pantalla. | No aparece la contraseña. |
| 9 | Verificación | Consultar la cuenta mediante consulta de solo lectura a la base de ensayo (ver PA-05) y buscar `Faro2026Luz`. | El valor no aparece en texto legible. |

**Estado final esperado:** Existe la cuenta `natalia.pineda@dsqa.test`.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
