# SCR-ACC-REG-008 · Rechazar el registro cuando falta un dato obligatorio

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REG-008.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REG-008 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que la falta de cada dato obligatorio (nombre, correo, contraseña, rol) rechaza la solicitud con el error junto al campo correspondiente. |
| Caso asociado | [ACC-REG-008](../2.4_Casos_de_prueba/ACC-REG-008.md) · CA-HU-001-03 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-008A, D-008B, D-008C, D-008D de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios). Tiene cuatro envíos: después del tercero se esperan 65 s para no mezclar el rechazo por datos con el límite por minuto. |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Registro** y diligenciar D-008A (Nombre vacío). | Formulario con Nombre vacío. |
| 2 | Paso | Enviar. | El sistema procesa la solicitud. |
| 3 | Verificación | Revisar el error. | Se rechaza; el error aparece junto a Nombre. |
| 4 | Paso | Diligenciar D-008B (Correo vacío) y enviar. | El sistema procesa la solicitud. |
| 5 | Verificación | Revisar el error. | Se rechaza; el error aparece junto a Correo electrónico. |
| 6 | Paso | Diligenciar D-008C (Contraseña vacía) y enviar. | El sistema procesa la solicitud. |
| 7 | Verificación | Revisar el error. | Se rechaza; el error aparece junto a Contraseña. |
| 8 | Paso | Esperar 65 s. | — |
| 9 | Paso | Diligenciar D-008D (sin rol) y enviar. | El sistema procesa la solicitud. |
| 10 | Verificación | Revisar el error. | Se rechaza; el error aparece junto a Rol. |
| 11 | Verificación | Buscar ambos correos mediante consulta de solo lectura a la base de ensayo (ver PA-05). | No existe ninguna de las dos cuentas. |

**Estado final esperado:** No existen `sin.nombre@dsqa.test` ni `camila.herrera@dsqa.test`.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
