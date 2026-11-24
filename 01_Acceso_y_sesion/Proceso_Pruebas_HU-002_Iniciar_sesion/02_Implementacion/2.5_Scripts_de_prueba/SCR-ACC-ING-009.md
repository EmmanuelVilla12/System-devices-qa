# SCR-ACC-ING-009 · Comprobar que la contraseña no queda en texto legible en los registros almacenados

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-ING-009.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-ING-009 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que, después de un ingreso, la contraseña no aparece en texto legible ni en la base ni en los registros almacenados del servicio. |
| Caso asociado | [ACC-ING-009](../2.4_Casos_de_prueba/ACC-ING-009.md) · CA-HU-002-06 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-009 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Iniciar sesión** sin sesión iniciada. | Se muestra el formulario con Correo electrónico y Contraseña. |
| 2 | Paso | Escribir `ingreso.soporte@dsqa.test` en Correo electrónico. | El campo muestra el valor. |
| 3 | Paso | Escribir `Duna3Plata` en Contraseña. | El campo oculta los caracteres. |
| 4 | Paso | Enviar la solicitud de ingreso. | El sistema procesa la solicitud. |
| 5 | Paso | Anotar la hora del envío. | Hora registrada. |
| 6 | Verificación | Consultar la cuenta en la base (solo lectura) y buscar `Duna3Plata`. | Sin coincidencias en texto legible. |
| 7 | Verificación | Buscar `Duna3Plata` en los registros del servicio de la hora anotada. | Sin coincidencias. |

**Estado final esperado:** Sin sesión al terminar.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
