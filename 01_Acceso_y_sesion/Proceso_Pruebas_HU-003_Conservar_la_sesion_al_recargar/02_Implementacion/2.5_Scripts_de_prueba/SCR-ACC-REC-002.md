# SCR-ACC-REC-002 · Mantener las funciones permitidas del rol después de recargar

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REC-002.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REC-002 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que, al recargar una pantalla de la aplicación, se mantienen las funciones permitidas para el rol de la sesión. |
| Caso asociado | [ACC-REC-002](../2.4_Casos_de_prueba/ACC-REC-002.md) · CA-HU-003-02 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-002 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Iniciar sesión (HU-002) con `sesion.soporte@dsqa.test` / `Ancla2Rojo`. | Sesión iniciada como `Lina Cardozo`, rol soporte. |
| 2 | Paso | Anotar las opciones y accesos visibles en la pantalla presentada. | Lista anotada. |
| 3 | Paso | Recargar la página con F5. | La pantalla se vuelve a cargar. |
| 4 | Verificación | Comparar las opciones visibles con la lista anotada. | Son las mismas, sin opciones adicionales ni faltantes. |
| 5 | Verificación | Abrir **Perfil** y leer el rol. | Rol soporte. |

**Estado final esperado:** Sesión vigente; cerrarla al terminar.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
