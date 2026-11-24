# SCR-ACC-REC-007 · Usar con teclado los controles de la pantalla recargada

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REC-007.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REC-007 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que, tras la recarga, los controles de la pantalla siguen identificables y utilizables con teclado. |
| Caso asociado | [ACC-REC-007](../2.4_Casos_de_prueba/ACC-REC-007.md) · CA-HU-003-01 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-007 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Iniciar sesión (HU-002) con `sesion.usuario@dsqa.test` / `Brujula7Mar`. | Sesión iniciada como `Óscar Bedoya`, rol usuario. |
| 2 | Paso | Abrir **Perfil** usando solo el teclado. | Perfil abierto. |
| 3 | Paso | Recargar con Ctrl+R. | La pantalla se vuelve a cargar. |
| 4 | Paso | Recorrer los controles con Tab. | El foco avanza control por control. |
| 5 | Verificación | Revisar foco y nombres de los controles. | Foco visible; cada control tiene un nombre identificable. |

**Estado final esperado:** Sesión vigente; cerrarla al terminar.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
