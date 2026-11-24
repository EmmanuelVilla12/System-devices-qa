# SCR-ACC-REG-007 · Rechazar el registro con un correo que ya pertenece a una cuenta

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REG-007.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REG-007 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que un correo existente no genera una segunda cuenta y que se identifica como el dato a corregir. |
| Caso asociado | [ACC-REG-007](../2.4_Casos_de_prueba/ACC-REG-007.md) · CA-HU-001-02 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-007 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Verificación | Buscar `existente.g1@dsqa.test` mediante consulta de solo lectura a la base de ensayo (ver PA-05). | Una cuenta: `Mariela Bustos`, rol usuario. |
| 2 | Paso | Abrir **Registro** sin sesión iniciada. | Se muestra el formulario con Nombre, Correo electrónico, Contraseña y Rol. |
| 3 | Paso | Escribir `Mateo Salgado` en Nombre. | El campo muestra el valor escrito. |
| 4 | Paso | Escribir `existente.g1@dsqa.test` en Correo electrónico. | El campo muestra el valor escrito. |
| 5 | Paso | Escribir `Bosque52` en Contraseña. | El campo oculta los caracteres. |
| 6 | Paso | Seleccionar `Soporte` en Rol. | El rol queda seleccionado. |
| 7 | Paso | Enviar el formulario. | El sistema procesa la solicitud. |
| 8 | Verificación | Revisar el aviso. | Aparece junto al campo Correo electrónico; no hay confirmación de registro. |
| 9 | Verificación | Repetir la consulta del paso 1. | Sigue habiendo una sola cuenta, con nombre `Mariela Bustos` y rol usuario. |

**Estado final esperado:** Sigue existiendo una sola cuenta con `existente.g1@dsqa.test`, sin cambios.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
