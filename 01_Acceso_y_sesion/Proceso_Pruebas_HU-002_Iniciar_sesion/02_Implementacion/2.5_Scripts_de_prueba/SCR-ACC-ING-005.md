# SCR-ACC-ING-005 · Rechazar el ingreso con contraseña incorrecta y mostrar el mismo mensaje que con correo inexistente

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-ING-005.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-ING-005 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que una contraseña incorrecta de un correo registrado no inicia sesión y produce exactamente el mismo mensaje que un correo inexistente. |
| Caso asociado | [ACC-ING-005](../2.4_Casos_de_prueba/ACC-ING-005.md) · CA-HU-002-03 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-005A, D-005B, D-005C de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Iniciar sesión** sin sesión iniciada. | Se muestra el formulario con Correo electrónico y Contraseña. |
| 2 | Paso | Escribir `no.existe.g1@dsqa.test` en Correo electrónico. | El campo muestra el valor. |
| 3 | Paso | Escribir `Llave8Norte` en Contraseña. | El campo oculta los caracteres. |
| 4 | Paso | Enviar la solicitud de ingreso. | El sistema procesa la solicitud. |
| 5 | Verificación | Transcribir el mensaje (referencia). | Mensaje de rechazo sin sesión iniciada. |
| 6 | Paso | Cambiar a `ingreso.usuario@dsqa.test` / `Llave8Sur` y enviar. | El sistema procesa la solicitud. |
| 7 | Verificación | Comparar el mensaje con la referencia. | Texto idéntico; no hay sesión. |
| 8 | Paso | Cambiar la contraseña a `llave8norte` y enviar. | El sistema procesa la solicitud. |
| 9 | Verificación | Comparar el mensaje con la referencia. | Texto idéntico; no hay sesión. |

**Estado final esperado:** Sin sesión; la cuenta `ingreso.usuario@dsqa.test` sigue activa.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
