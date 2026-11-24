# SCR-ACC-REG-014 · Rechazar contraseñas que contienen espacios

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REG-014.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REG-014 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que una contraseña con un espacio intermedio o inicial se rechaza indicando la condición «sin espacios». |
| Caso asociado | [ACC-REG-014](../2.4_Casos_de_prueba/ACC-REG-014.md) · CA-HU-001-05 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-014A, D-014B de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Registro** sin sesión iniciada. | Se muestra el formulario con Nombre, Correo electrónico, Contraseña y Rol. |
| 2 | Paso | Escribir `Paula Cifuentes` en Nombre. | El campo muestra el valor escrito. |
| 3 | Paso | Escribir `paula.cifuentes@dsqa.test` en Correo electrónico. | El campo muestra el valor escrito. |
| 4 | Paso | Escribir `Bosque 52` en Contraseña. | El campo oculta los caracteres. |
| 5 | Paso | Seleccionar `Usuario` en Rol. | El rol queda seleccionado. |
| 6 | Paso | Enviar el formulario. | El sistema procesa la solicitud. |
| 7 | Verificación | Revisar la respuesta. | Se rechaza; se indica «sin espacios». |
| 8 | Paso | Cambiar la contraseña a ` Bosque52` (espacio al inicio) y enviar. | El sistema procesa la solicitud. |
| 9 | Verificación | Revisar la respuesta. | Se rechaza; se indica «sin espacios». |

**Estado final esperado:** No existe `paula.cifuentes@dsqa.test`.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
