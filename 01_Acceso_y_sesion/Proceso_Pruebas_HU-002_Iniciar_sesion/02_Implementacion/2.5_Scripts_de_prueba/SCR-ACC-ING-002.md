# SCR-ACC-ING-002 · Iniciar sesión con una cuenta activa de rol administrador

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-ING-002.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-ING-002 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que el ingreso reconoce el rol administrador de la cuenta en la sesión iniciada. |
| Caso asociado | [ACC-ING-002](../2.4_Casos_de_prueba/ACC-ING-002.md) · CA-HU-002-01 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-002 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Iniciar sesión** sin sesión iniciada. | Se muestra el formulario con Correo electrónico y Contraseña. |
| 2 | Paso | Escribir `ingreso.admin@dsqa.test` en Correo electrónico. | El campo muestra el valor. |
| 3 | Paso | Escribir `Torre5Oeste` en Contraseña. | El campo oculta los caracteres. |
| 4 | Paso | Enviar la solicitud de ingreso. | El sistema procesa la solicitud. |
| 5 | Verificación | Revisar la pantalla presentada. | Se muestra el inicio. |
| 6 | Verificación | Abrir **Perfil** y leer nombre y rol. | Nombre `Germán Toro`, rol administrador. |

**Estado final esperado:** Sesión abierta de `ingreso.admin@dsqa.test`; cerrarla al terminar.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
