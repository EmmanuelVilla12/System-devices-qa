# SCR-ACC-ING-008 · No mostrar la contraseña en la respuesta de un ingreso aceptado ni de uno rechazado

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-ING-008.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-ING-008 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que la respuesta del ingreso y los datos de la cuenta no muestran la contraseña, tanto si el ingreso se acepta como si se rechaza. |
| Caso asociado | [ACC-ING-008](../2.4_Casos_de_prueba/ACC-ING-008.md) · CA-HU-002-06 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-008A, D-008B de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Iniciar sesión** sin sesión iniciada. | Se muestra el formulario con Correo electrónico y Contraseña. |
| 2 | Paso | Escribir `ingreso.soporte@dsqa.test` en Correo electrónico. | El campo muestra el valor. |
| 3 | Paso | Escribir `Duna3Plata` en Contraseña. | El campo oculta los caracteres. |
| 4 | Paso | Enviar la solicitud de ingreso. | El sistema procesa la solicitud. |
| 5 | Verificación | En el panel de red, abrir la respuesta del ingreso y buscar `Duna3Plata`. | Sin coincidencias ni campo de contraseña. |
| 6 | Verificación | Abrir **Perfil** y revisar los datos. | No aparece la contraseña. |
| 7 | Paso | Cerrar sesión e ingresar con `ingreso.soporte@dsqa.test` / `Duna3Bronce`. | La solicitud se rechaza. |
| 8 | Verificación | Buscar `Duna3Bronce` en la respuesta y en la pantalla. | Sin coincidencias. |

**Estado final esperado:** Sin sesión al terminar (cerrar la sesión del envío aceptado).

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
