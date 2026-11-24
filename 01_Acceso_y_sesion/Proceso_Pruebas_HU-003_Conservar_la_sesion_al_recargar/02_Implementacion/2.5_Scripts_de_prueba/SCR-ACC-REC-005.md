# SCR-ACC-REC-005 · Cerrar la sesión y pedir un nuevo ingreso al recargar con la sesión caducada

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REC-005.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REC-005 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que, si la sesión caducó, recargar una pantalla que exige identificación no conserva el acceso, cierra la sesión y solicita un nuevo ingreso. |
| Caso asociado | [ACC-REC-005](../2.4_Casos_de_prueba/ACC-REC-005.md) · CA-HU-003-04 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-005 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Iniciar sesión (HU-002) con `sesion.usuario@dsqa.test` / `Brujula7Mar`. | Sesión iniciada como `Óscar Bedoya`, rol usuario. |
| 2 | Paso | Abrir **Perfil** y anotar el momento de caducidad. | Valor anotado. |
| 3 | Paso | Esperar a que pase el momento anotado (o aplicar el mecanismo de PA-01). | — |
| 4 | Paso | Recargar la página con F5. | La pantalla se vuelve a cargar. |
| 5 | Verificación | Revisar la pantalla. | No se muestran datos del perfil; se solicita iniciar sesión. |
| 6 | Verificación | Abrir de nuevo la dirección de Perfil. | Se sigue solicitando iniciar sesión. |

**Estado final esperado:** Sin sesión.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
