# SCR-ACC-REG-002 · Registrar una cuenta válida con rol soporte

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REG-002.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REG-002 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que el registro con rol soporte crea una cuenta activa con ese rol, sin pasos de aprobación. |
| Caso asociado | [ACC-REG-002](../2.4_Casos_de_prueba/ACC-REG-002.md) · CA-HU-001-01, CA-HU-001-06 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-002 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Registro** sin sesión iniciada. | Se muestra el formulario con Nombre, Correo electrónico, Contraseña y Rol. |
| 2 | Paso | Escribir `Esteban Quintero` en Nombre. | El campo muestra el valor escrito. |
| 3 | Paso | Escribir `esteban.quintero@dsqa.test` en Correo electrónico. | El campo muestra el valor escrito. |
| 4 | Paso | Escribir `Nevado2031` en Contraseña. | El campo oculta los caracteres. |
| 5 | Paso | Seleccionar `Soporte` en Rol. | El rol queda seleccionado. |
| 6 | Paso | Enviar el formulario. | El sistema procesa la solicitud. |
| 7 | Verificación | Revisar la respuesta en pantalla. | Se muestran los datos con rol soporte y sin contraseña; no hay aviso de aprobación pendiente. |
| 8 | Verificación | Buscar el correo mediante consulta de solo lectura a la base de ensayo (ver PA-05). | Cuenta activa con rol soporte. |

**Estado final esperado:** Existe una cuenta activa `esteban.quintero@dsqa.test` con rol soporte.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
