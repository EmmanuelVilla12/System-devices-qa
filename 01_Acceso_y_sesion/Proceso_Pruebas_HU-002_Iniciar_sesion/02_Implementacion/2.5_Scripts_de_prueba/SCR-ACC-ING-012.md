# SCR-ACC-ING-012 · Anunciar los campos y el error de ingreso con lector de pantalla

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-ING-012.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-ING-012 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que los campos se identifican y que el mensaje de rechazo se comunica de manera accesible. |
| Caso asociado | [ACC-ING-012](../2.4_Casos_de_prueba/ACC-ING-012.md) · CA-HU-002-03 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-012 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Iniciar sesión** con el lector activo y enfocar el correo. | El lector anuncia «Correo electrónico». |
| 2 | Paso | Escribir `ingreso.usuario@dsqa.test` y pasar a Contraseña. | El lector anuncia «Contraseña». |
| 3 | Paso | Escribir `Llave8Este` y enviar. | El sistema procesa la solicitud. |
| 4 | Verificación | Escuchar el anuncio posterior. | El lector anuncia el mensaje de rechazo. |

**Estado final esperado:** Sin sesión.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
