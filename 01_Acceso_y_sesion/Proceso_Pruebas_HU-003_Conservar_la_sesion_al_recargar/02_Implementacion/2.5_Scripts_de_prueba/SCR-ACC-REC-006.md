# SCR-ACC-REC-006 · Cerrar la sesión al recargar cuando el servicio la rechaza como inválida

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REC-006.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REC-006 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que una sesión que el servicio rechaza como inválida no se convierte en autorizada al recargar. |
| Caso asociado | [ACC-REC-006](../2.4_Casos_de_prueba/ACC-REC-006.md) · CA-HU-003-04 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-006 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Iniciar sesión (HU-002) con `sesion.soporte@dsqa.test` / `Ancla2Rojo`. | Sesión iniciada como `Lina Cardozo`, rol soporte. |
| 2 | Paso | Abrir **Perfil**. | Datos de `Lina Cardozo`. |
| 3 | Paso | Invalidar la sesión con el mecanismo de PA-02. | — |
| 4 | Paso | Recargar la página con F5. | La pantalla se vuelve a cargar. |
| 5 | Verificación | Revisar la pantalla. | No se muestran datos del perfil; se solicita iniciar sesión. |
| 6 | Verificación | Revisar si la aplicación sigue mostrando a la persona como identificada. | No la muestra como identificada. |

**Estado final esperado:** Sin sesión.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
