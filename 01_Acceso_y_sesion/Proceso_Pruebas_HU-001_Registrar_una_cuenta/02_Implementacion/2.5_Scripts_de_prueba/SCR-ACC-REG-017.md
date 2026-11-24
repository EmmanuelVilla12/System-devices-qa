# SCR-ACC-REG-017 · Iniciar sesión con la cuenta recién registrada

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REG-017.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REG-017 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que la cuenta aceptada queda activa y puede usarse para iniciar sesión mediante HU-002. |
| Caso asociado | [ACC-REG-017](../2.4_Casos_de_prueba/ACC-REG-017.md) · CA-HU-001-01 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-017 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Registro** sin sesión iniciada. | Se muestra el formulario con Nombre, Correo electrónico, Contraseña y Rol. |
| 2 | Paso | Escribir `Fernando Lozada` en Nombre. | El campo muestra el valor escrito. |
| 3 | Paso | Escribir `fernando.lozada@dsqa.test` en Correo electrónico. | El campo muestra el valor escrito. |
| 4 | Paso | Escribir `Cometa63` en Contraseña. | El campo oculta los caracteres. |
| 5 | Paso | Seleccionar `Soporte` en Rol. | El rol queda seleccionado. |
| 6 | Paso | Enviar el formulario. | El sistema procesa la solicitud. |
| 7 | Verificación | Revisar la respuesta. | Registro aceptado con rol soporte. |
| 8 | Paso | Abrir **Iniciar sesión** (HU-002). | Se muestra el formulario de ingreso. |
| 9 | Paso | Ingresar `fernando.lozada@dsqa.test` y `Cometa63` y enviar. | El sistema procesa el ingreso. |
| 10 | Verificación | Revisar la pantalla presentada. | Se inicia sesión como Fernando Lozada con rol soporte. |

**Estado final esperado:** Cuenta activa con una sesión abierta; cerrar sesión al terminar.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
