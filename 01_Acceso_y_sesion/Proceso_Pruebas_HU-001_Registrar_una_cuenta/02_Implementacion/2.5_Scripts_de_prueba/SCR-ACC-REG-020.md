# SCR-ACC-REG-020 · Identificar campos, condiciones y errores con lector de pantalla

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REG-020.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REG-020 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que los campos se identifican y que avisos y errores se comunican de manera accesible. |
| Caso asociado | [ACC-REG-020](../2.4_Casos_de_prueba/ACC-REG-020.md) · CA-HU-001-03, CA-HU-001-04 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-020 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Registro** con el lector activo y enfocar Nombre. | El lector anuncia «Nombre». |
| 2 | Paso | Escribir `Daniela Úsuga` y pasar a Correo electrónico. | El lector anuncia «Correo electrónico». |
| 3 | Paso | Escribir `daniela.usugadsqa.test` y pasar a Contraseña. | El lector anuncia «Contraseña». |
| 4 | Paso | Escribir `Coral81x`. | — |
| 5 | Verificación | Escuchar o recorrer la lista de condiciones. | El lector informa qué condiciones se cumplen. |
| 6 | Paso | Seleccionar `Usuario` en Rol y enviar. | El sistema procesa la solicitud. |
| 7 | Verificación | Escuchar el anuncio posterior al envío. | El lector anuncia el error asociado a Correo electrónico. |

**Estado final esperado:** No se crea ninguna cuenta.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
