# SCR-ACC-ING-011 · Iniciar sesión usando solo el teclado

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-ING-011.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-ING-011 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que el ingreso se realiza sin ratón, en orden lógico y con foco visible. |
| Caso asociado | [ACC-ING-011](../2.4_Casos_de_prueba/ACC-ING-011.md) · CA-HU-002-01 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-011 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Iniciar sesión** y pulsar Tab hasta Correo electrónico. | Foco visible en Correo electrónico. |
| 2 | Paso | Escribir `ingreso.admin@dsqa.test` y pulsar Tab. | Foco en Contraseña. |
| 3 | Paso | Escribir `Torre5Oeste` y pulsar Tab. | Foco en el botón de ingreso. |
| 4 | Paso | Pulsar Enter. | El sistema procesa la solicitud. |
| 5 | Verificación | Revisar el resultado. | Sesión iniciada; el foco nunca quedó invisible ni atrapado. |

**Estado final esperado:** Sesión abierta; cerrarla al terminar.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
