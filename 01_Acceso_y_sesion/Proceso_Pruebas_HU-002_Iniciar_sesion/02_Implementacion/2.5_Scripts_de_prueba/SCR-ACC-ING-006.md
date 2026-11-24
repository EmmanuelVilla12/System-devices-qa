# SCR-ACC-ING-006 · Rechazar el ingreso de una cuenta inactiva aunque las credenciales sean correctas

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-ING-006.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-ING-006 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que una cuenta inactiva no puede iniciar sesión aunque use sus credenciales correctas. |
| Caso asociado | [ACC-ING-006](../2.4_Casos_de_prueba/ACC-ING-006.md) · CA-HU-002-04 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-006 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Iniciar sesión** sin sesión iniciada. | Se muestra el formulario con Correo electrónico y Contraseña. |
| 2 | Paso | Escribir `cuenta.inactiva@dsqa.test` en Correo electrónico. | El campo muestra el valor. |
| 3 | Paso | Escribir `Pausa6Gris` en Contraseña. | El campo oculta los caracteres. |
| 4 | Paso | Enviar la solicitud de ingreso. | El sistema procesa la solicitud. |
| 5 | Verificación | Revisar el resultado. | Se rechaza el ingreso; no aparece el inicio. |
| 6 | Verificación | Abrir la dirección de **Perfil**. | Se solicita iniciar sesión. |

**Estado final esperado:** Sin sesión; la cuenta sigue inactiva.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
