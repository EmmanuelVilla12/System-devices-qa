# SCR-ACC-REC-008 · Mantener legible y utilizable la pantalla recargada en computador y teléfono

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REC-008.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REC-008 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que la pantalla recargada conserva sus controles utilizables en computador y teléfono móvil. |
| Caso asociado | [ACC-REC-008](../2.4_Casos_de_prueba/ACC-REC-008.md) · CA-HU-003-01 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-008A, D-008B de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Iniciar sesión (HU-002) con `sesion.soporte@dsqa.test` / `Ancla2Rojo`. | Sesión iniciada como `Lina Cardozo`, rol soporte. |
| 2 | Paso | En 1366×768 abrir **Perfil** y recargar. | Perfil se vuelve a cargar. |
| 3 | Verificación | Revisar la pantalla. | Contenido completo y legible; identidad `Lina Cardozo`. |
| 4 | Paso | Cambiar a 390×844 y recargar. | Perfil se vuelve a cargar. |
| 5 | Verificación | Revisar la pantalla. | Contenido completo, sin texto cortado ni desplazamiento horizontal. |

**Estado final esperado:** Sesión vigente; cerrarla al terminar.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
