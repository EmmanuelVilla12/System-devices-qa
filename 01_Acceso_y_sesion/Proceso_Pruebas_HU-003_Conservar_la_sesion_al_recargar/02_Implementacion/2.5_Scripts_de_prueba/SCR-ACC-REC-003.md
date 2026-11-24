# SCR-ACC-REC-003 · No conceder permisos adicionales al recargar

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REC-003.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REC-003 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que la recarga no convierte una función no permitida en permitida para el rol de la sesión. |
| Caso asociado | [ACC-REC-003](../2.4_Casos_de_prueba/ACC-REC-003.md) · CA-HU-003-02 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-003 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Iniciar sesión (HU-002) con `sesion.usuario@dsqa.test` / `Brujula7Mar`. | Sesión iniciada como `Óscar Bedoya`, rol usuario. |
| 2 | Paso | Abrir la dirección de la función restringida (PA-04). | El sistema procesa la solicitud. |
| 3 | Verificación | Revisar la respuesta. | Acceso denegado. |
| 4 | Paso | Recargar la página con F5. | La pantalla se vuelve a cargar. |
| 5 | Verificación | Revisar la respuesta tras la recarga. | Sigue mostrando Acceso denegado; no aparece el contenido de la función. |

**Estado final esperado:** Sesión vigente; cerrarla al terminar.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
