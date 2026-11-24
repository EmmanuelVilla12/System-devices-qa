# SCR-ACC-REG-019 · Completar el registro solo con teclado

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REG-019.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REG-019 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que el formulario se diligencia y envía sin ratón, con foco visible y sin trampas de foco. |
| Caso asociado | [ACC-REG-019](../2.4_Casos_de_prueba/ACC-REG-019.md) · CA-HU-001-01 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-019 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Registro** y pulsar Tab hasta Nombre. | El foco visible está en Nombre. |
| 2 | Paso | Escribir `Kevin Arias` y pulsar Tab. | El foco pasa a Correo electrónico. |
| 3 | Paso | Escribir `kevin.arias@dsqa.test` y pulsar Tab. | El foco pasa a Contraseña. |
| 4 | Paso | Escribir `Arce4Verde` y pulsar Tab. | El foco pasa a Rol. |
| 5 | Paso | Elegir `Administrador` con las flechas. | El rol cambia sin usar ratón. |
| 6 | Paso | Pulsar Tab hasta el botón de envío y pulsar Enter. | El sistema procesa la solicitud. |
| 7 | Verificación | Revisar el resultado. | Registro aceptado; en ningún momento el foco quedó atrapado ni invisible. |

**Estado final esperado:** Existe la cuenta `kevin.arias@dsqa.test`.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
