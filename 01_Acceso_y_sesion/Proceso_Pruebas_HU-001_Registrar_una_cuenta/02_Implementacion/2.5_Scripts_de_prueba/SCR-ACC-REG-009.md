# SCR-ACC-REG-009 · Rechazar nombres de 2 y de 51 caracteres

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REG-009.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REG-009 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que nombres de 2 y 51 caracteres se rechazan con el error junto a Nombre y sin crear cuenta. |
| Caso asociado | [ACC-REG-009](../2.4_Casos_de_prueba/ACC-REG-009.md) · CA-HU-001-03 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-009A, D-009B de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Registro** sin sesión iniciada. | Se muestra el formulario con Nombre, Correo electrónico, Contraseña y Rol. |
| 2 | Paso | Escribir `Bo` en Nombre. | El campo muestra el valor escrito. |
| 3 | Paso | Escribir `bo.limite2@dsqa.test` en Correo electrónico. | El campo muestra el valor escrito. |
| 4 | Paso | Escribir `Bosque52` en Contraseña. | El campo oculta los caracteres. |
| 5 | Paso | Seleccionar `Usuario` en Rol. | El rol queda seleccionado. |
| 6 | Paso | Enviar el formulario. | El sistema procesa la solicitud. |
| 7 | Verificación | Revisar la respuesta. | Se rechaza; error junto a Nombre. |
| 8 | Paso | Repetir los pasos 1 a 6 con D-009B. | El sistema procesa la solicitud. |
| 9 | Verificación | Revisar la respuesta. | Se rechaza; error junto a Nombre. |
| 10 | Verificación | Buscar ambos correos mediante consulta de solo lectura a la base de ensayo (ver PA-05). | No existen. |

**Estado final esperado:** No existen las cuentas de D-009A ni D-009B.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
