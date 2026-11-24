# SCR-ACC-REC-004 · Conservar la sesión al recargar sin ampliar su momento de caducidad

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REC-004.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REC-004 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que recargar antes de la caducidad conserva la sesión y no cambia su momento de vencimiento. |
| Caso asociado | [ACC-REC-004](../2.4_Casos_de_prueba/ACC-REC-004.md) · CA-HU-003-03 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-004 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Iniciar sesión (HU-002) con `sesion.usuario@dsqa.test` / `Brujula7Mar`. | Sesión iniciada como `Óscar Bedoya`, rol usuario. |
| 2 | Paso | Abrir **Perfil** y anotar el momento de caducidad. | Valor anotado (T₀). |
| 3 | Paso | Esperar 2 minutos y recargar. | Perfil se vuelve a cargar. |
| 4 | Verificación | Leer la caducidad. | Igual a T₀. |
| 5 | Paso | Esperar 2 minutos y recargar. | Perfil se vuelve a cargar. |
| 6 | Paso | Esperar 2 minutos y recargar. | Perfil se vuelve a cargar. |
| 7 | Verificación | Leer la caducidad. | Igual a T₀; la sesión sigue vigente. |

**Estado final esperado:** Sesión vigente; cerrarla al terminar.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
