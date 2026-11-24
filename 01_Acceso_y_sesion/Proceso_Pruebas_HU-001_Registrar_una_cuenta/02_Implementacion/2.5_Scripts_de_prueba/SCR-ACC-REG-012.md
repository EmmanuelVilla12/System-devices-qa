# SCR-ACC-REG-012 · Rechazar contraseñas de 7 y de 73 caracteres

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REG-012.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REG-012 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que contraseñas de 7 y 73 caracteres se rechazan e indican que debe corregirse la longitud. |
| Caso asociado | [ACC-REG-012](../2.4_Casos_de_prueba/ACC-REG-012.md) · CA-HU-001-05 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-012A, D-012B de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Registro** sin sesión iniciada. | Se muestra el formulario con Nombre, Correo electrónico, Contraseña y Rol. |
| 2 | Paso | Escribir `Renata Vargas` en Nombre. | El campo muestra el valor escrito. |
| 3 | Paso | Escribir `renata.siete@dsqa.test` en Correo electrónico. | El campo muestra el valor escrito. |
| 4 | Paso | Escribir `Rio4Mar` en Contraseña. | El campo oculta los caracteres. |
| 5 | Paso | Seleccionar `Usuario` en Rol. | El rol queda seleccionado. |
| 6 | Paso | Enviar el formulario. | El sistema procesa la solicitud. |
| 7 | Verificación | Revisar la respuesta. | Se rechaza; se indica la condición de longitud. |
| 8 | Paso | Repetir los pasos 1 a 6 con D-012B (pegar PWD-73 desde 2.3). | El sistema procesa la solicitud. |
| 9 | Verificación | Revisar la respuesta. | Se rechaza; se indica la condición de longitud. |
| 10 | Verificación | Buscar ambos correos mediante consulta de solo lectura a la base de ensayo (ver PA-05). | No existen. |

**Estado final esperado:** No existen las cuentas de D-012A ni D-012B.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
