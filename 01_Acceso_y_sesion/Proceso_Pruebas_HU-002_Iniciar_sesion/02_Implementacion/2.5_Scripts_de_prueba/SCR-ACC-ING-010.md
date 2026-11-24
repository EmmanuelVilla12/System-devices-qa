# SCR-ACC-ING-010 · Comprobar que el ingreso no otorga funciones ajenas al rol de la cuenta

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-ING-010.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-ING-010 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que la sesión iniciada reconoce el rol y que el acceso a una función de otro rol se rechaza. |
| Caso asociado | [ACC-ING-010](../2.4_Casos_de_prueba/ACC-ING-010.md) · CA-HU-002-01 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-010 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Iniciar sesión** sin sesión iniciada. | Se muestra el formulario con Correo electrónico y Contraseña. |
| 2 | Paso | Escribir `ingreso.usuario@dsqa.test` en Correo electrónico. | El campo muestra el valor. |
| 3 | Paso | Escribir `Llave8Norte` en Contraseña. | El campo oculta los caracteres. |
| 4 | Paso | Enviar la solicitud de ingreso. | El sistema procesa la solicitud. |
| 5 | Paso | Abrir la dirección de la función restringida confirmada en PA-04. | El sistema procesa la solicitud. |
| 6 | Verificación | Revisar la respuesta. | Se muestra Acceso denegado; no se muestra el contenido de la función. |
| 7 | Verificación | Abrir **Perfil**. | La sesión sigue iniciada como `Rocío Londoño`. |

**Estado final esperado:** Sesión abierta; cerrarla al terminar.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
