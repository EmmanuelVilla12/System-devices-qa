# SCR-ACC-ING-001 · Iniciar sesión con credenciales válidas de una cuenta activa

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-ING-001.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-ING-001 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que una cuenta activa con credenciales válidas inicia una sesión con su identidad y su rol y presenta el inicio. |
| Caso asociado | [ACC-ING-001](../2.4_Casos_de_prueba/ACC-ING-001.md) · CA-HU-002-01 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-001 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Iniciar sesión** sin sesión iniciada. | Se muestra el formulario con Correo electrónico y Contraseña. |
| 2 | Paso | Escribir `ingreso.usuario@dsqa.test` en Correo electrónico. | El campo muestra el valor. |
| 3 | Paso | Escribir `Llave8Norte` en Contraseña. | El campo oculta los caracteres. |
| 4 | Paso | Enviar la solicitud de ingreso. | El sistema procesa la solicitud. |
| 5 | Verificación | Revisar la pantalla presentada. | Se muestra el inicio de la aplicación. |
| 6 | Verificación | Abrir **Perfil** (HU-004) y leer nombre y rol. | Nombre `Rocío Londoño`, rol usuario. |

**Estado final esperado:** Sesión abierta de `ingreso.usuario@dsqa.test`; cerrarla al terminar (HU-005).

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
