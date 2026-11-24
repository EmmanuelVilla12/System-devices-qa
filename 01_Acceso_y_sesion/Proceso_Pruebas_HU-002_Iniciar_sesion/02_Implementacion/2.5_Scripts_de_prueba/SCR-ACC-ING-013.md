# SCR-ACC-ING-013 · Iniciar sesión en computador y en teléfono

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-ING-013.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-ING-013 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que el formulario de ingreso y sus errores se leen y usan en computador y en teléfono. |
| Caso asociado | [ACC-ING-013](../2.4_Casos_de_prueba/ACC-ING-013.md) · CA-HU-002-01 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-013A, D-013B de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | En 1366×768, ingresar con D-013A. | Sesión iniciada. |
| 2 | Paso | Cerrar sesión y cambiar a 390×844. | Se muestra el formulario de ingreso. |
| 3 | Paso | Ingresar con `Llave8Oeste`. | La solicitud se rechaza. |
| 4 | Verificación | Revisar el mensaje y los campos. | Se leen completos, sin desplazamiento horizontal. |
| 5 | Paso | Ingresar con `Llave8Norte`. | Sesión iniciada. |

**Estado final esperado:** Sesión abierta en móvil; cerrarla al terminar.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
