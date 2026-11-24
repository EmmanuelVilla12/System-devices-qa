# SCR-ACC-REC-001 · Conservar la identidad al recargar una pantalla protegida con sesión vigente

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REC-001.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REC-001 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que, con una sesión vigente reconocida por el servicio, recargar una pantalla protegida permitida conserva la misma identidad y el acceso. |
| Caso asociado | [ACC-REC-001](../2.4_Casos_de_prueba/ACC-REC-001.md) · CA-HU-003-01 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-001 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Iniciar sesión (HU-002) con `sesion.usuario@dsqa.test` / `Brujula7Mar`. | Sesión iniciada como `Óscar Bedoya`, rol usuario. |
| 2 | Paso | Abrir **Perfil**. | Se muestran los datos de `Óscar Bedoya`. |
| 3 | Paso | Recargar la página con F5. | La pantalla se vuelve a cargar. |
| 4 | Verificación | Revisar la pantalla. | Sigue abierta Perfil; no se pide iniciar sesión. |
| 5 | Verificación | Leer nombre y correo. | `Óscar Bedoya` · `sesion.usuario@dsqa.test`. |

**Estado final esperado:** Sesión vigente; cerrarla al terminar.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
