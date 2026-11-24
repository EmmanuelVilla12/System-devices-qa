# SCR-ACC-REG-004 · Consultar las opciones del campo Rol

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REG-004.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REG-004 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que el campo Rol ofrece las tres opciones de la ficha y ninguna otra, sin enviar el formulario. |
| Caso asociado | [ACC-REG-004](../2.4_Casos_de_prueba/ACC-REG-004.md) · CA-HU-001-06 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-004 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Registro** sin sesión iniciada. | Se muestra el formulario. |
| 2 | Paso | Abrir la lista del campo Rol. | Se despliegan las opciones. |
| 3 | Verificación | Contar y leer las opciones. | Hay tres opciones: usuario, soporte y administrador. |
| 4 | Verificación | Buscar textos de aprobación junto al campo. | No se indica que el rol requiera aprobación adicional. |
| 5 | Paso | Cerrar la lista sin enviar. | El formulario sigue sin enviar. |

**Estado final esperado:** No se crea ninguna cuenta.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
