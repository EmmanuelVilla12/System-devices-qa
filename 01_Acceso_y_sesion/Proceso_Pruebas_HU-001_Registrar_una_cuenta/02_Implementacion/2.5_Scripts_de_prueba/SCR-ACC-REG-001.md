# SCR-ACC-REG-001 · Registrar una cuenta válida con rol usuario

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REG-001.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REG-001 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que un registro con nombre, correo, contraseña y rol válidos crea una cuenta activa con rol usuario y muestra sus datos sin la contraseña. |
| Caso asociado | [ACC-REG-001](../2.4_Casos_de_prueba/ACC-REG-001.md) · CA-HU-001-01 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-001 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Registro** sin sesión iniciada. | Se muestra el formulario con Nombre, Correo electrónico, Contraseña y Rol. |
| 2 | Paso | Escribir `Valentina Arango` en Nombre. | El campo muestra el valor escrito. |
| 3 | Paso | Escribir `valentina.arango@dsqa.test` en Correo electrónico. | El campo muestra el valor escrito. |
| 4 | Paso | Escribir `Girasol47` en Contraseña. | El campo oculta los caracteres. |
| 5 | Paso | Seleccionar `Usuario` en Rol. | El rol queda seleccionado. |
| 6 | Paso | Enviar el formulario. | El sistema procesa la solicitud. |
| 7 | Verificación | Revisar la respuesta en pantalla. | Se muestran nombre, correo y rol usuario; no aparece `Girasol47` ni un campo de contraseña. |
| 8 | Verificación | Buscar `valentina.arango@dsqa.test` mediante consulta de solo lectura a la base de ensayo (ver PA-05). | Existe una cuenta con estado activo y rol usuario. |

**Estado final esperado:** Existe una cuenta activa `valentina.arango@dsqa.test` con rol usuario.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
