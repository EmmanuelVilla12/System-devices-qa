# SCR-ACC-ING-004 · Rechazar el ingreso con un correo que no pertenece a ninguna cuenta

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-ING-004.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-ING-004 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que un correo no registrado no inicia sesión y que el mensaje no revela cuál credencial falló. |
| Caso asociado | [ACC-ING-004](../2.4_Casos_de_prueba/ACC-ING-004.md) · CA-HU-002-03 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-004 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Iniciar sesión** sin sesión iniciada. | Se muestra el formulario con Correo electrónico y Contraseña. |
| 2 | Paso | Escribir `no.existe.g1@dsqa.test` en Correo electrónico. | El campo muestra el valor. |
| 3 | Paso | Escribir `Llave8Norte` en Contraseña. | El campo oculta los caracteres. |
| 4 | Paso | Enviar la solicitud de ingreso. | El sistema procesa la solicitud. |
| 5 | Verificación | Revisar el resultado. | Se mantiene la pantalla de ingreso; no hay sesión iniciada. |
| 6 | Verificación | Transcribir el mensaje literal. | El texto no indica cuál credencial falló. |
| 7 | Verificación | Abrir la dirección de **Perfil**. | Se solicita iniciar sesión: no hay acceso. |

**Estado final esperado:** Sin sesión.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
