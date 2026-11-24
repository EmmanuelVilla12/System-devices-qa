# SCR-ACC-REG-021 · Leer y operar el registro en computador y teléfono

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REG-021.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REG-021 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que campos, lista de condiciones y acciones se mantienen utilizables en computador y teléfono móvil. |
| Caso asociado | [ACC-REG-021](../2.4_Casos_de_prueba/ACC-REG-021.md) · CA-HU-001-01, CA-HU-001-04 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-021A, D-021B de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Registro** en ventana de 1366×768. | Se muestra el formulario completo. |
| 2 | Verificación | Revisar etiquetas, lista de condiciones y botón. | Se leen completos y sin superposición. |
| 3 | Paso | Registrar D-021A. | Registro aceptado. |
| 4 | Paso | Cambiar a 390×844 (teléfono o emulación) y abrir **Registro**. | Se muestra el formulario. |
| 5 | Verificación | Revisar etiquetas, lista de condiciones y botón sin desplazamiento horizontal. | Se leen completos; el botón es visible. |
| 6 | Paso | Registrar D-021B. | Registro aceptado. |

**Estado final esperado:** Existen las dos cuentas.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
