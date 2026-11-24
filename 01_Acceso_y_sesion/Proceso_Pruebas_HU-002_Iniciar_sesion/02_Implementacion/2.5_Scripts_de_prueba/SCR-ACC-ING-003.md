# SCR-ACC-ING-003 · Abrir la pantalla protegida solicitada después de iniciar sesión

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-ING-003.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-ING-003 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que, si antes del ingreso se solicitó una pantalla protegida permitida para el rol, al iniciar sesión se abre esa pantalla. |
| Caso asociado | [ACC-ING-003](../2.4_Casos_de_prueba/ACC-ING-003.md) · CA-HU-002-02 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-003 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios). Anotar la dirección de Perfil antes de cerrar la sesión de preparación. |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Sin sesión, pegar en la barra la dirección de **Perfil** anotada en la preparación. | Se solicita iniciar sesión. |
| 2 | Paso | Escribir `ingreso.usuario@dsqa.test` y `Llave8Norte`. | Los campos muestran los valores. |
| 3 | Paso | Enviar la solicitud de ingreso. | El sistema procesa la solicitud. |
| 4 | Verificación | Revisar la pantalla abierta. | Se abre **Perfil**, no el inicio. |
| 5 | Verificación | Leer los datos mostrados. | Corresponden a `Rocío Londoño`. |

**Estado final esperado:** Sesión abierta en Perfil; cerrarla al terminar.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
