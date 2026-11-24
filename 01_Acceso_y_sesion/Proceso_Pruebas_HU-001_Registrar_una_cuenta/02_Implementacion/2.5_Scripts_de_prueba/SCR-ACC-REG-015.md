# SCR-ACC-REG-015 · Rechazar una contraseña que contiene el nombre

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REG-015.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REG-015 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que una contraseña que contiene una palabra del nombre, escrita igual, se rechaza indicando esa condición. |
| Caso asociado | [ACC-REG-015](../2.4_Casos_de_prueba/ACC-REG-015.md) · CA-HU-001-05 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-015 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Registro** sin sesión iniciada. | Se muestra el formulario con Nombre, Correo electrónico, Contraseña y Rol. |
| 2 | Paso | Escribir `Gonzalo Pardo` en Nombre. | El campo muestra el valor escrito. |
| 3 | Paso | Escribir `gonzalo.pardo@dsqa.test` en Correo electrónico. | El campo muestra el valor escrito. |
| 4 | Paso | Escribir `Pardo2026` en Contraseña. | El campo oculta los caracteres. |
| 5 | Verificación | Revisar la lista antes de enviar. | «Sin el nombre de la persona» aparece no cumplida. |
| 6 | Paso | Seleccionar `Usuario` en Rol. | El rol queda seleccionado. |
| 7 | Paso | Enviar el formulario. | El sistema procesa la solicitud. |
| 8 | Verificación | Revisar la respuesta. | Se rechaza indicando «sin el nombre de la persona». |
| 9 | Verificación | Buscar el correo mediante consulta de solo lectura a la base de ensayo (ver PA-05). | No existe. |

**Estado final esperado:** No existe `gonzalo.pardo@dsqa.test`.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
