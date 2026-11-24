# SCR-ACC-REG-011 · Actualizar la lista de condiciones mientras se escribe y corrige la contraseña

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-REG-011.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-REG-011 |
| Descripción | Pasos y puntos de verificación para comprobar: verificar que la lista de condiciones cambia con cada escritura o corrección, incluso cuando una condición deja de cumplirse. |
| Caso asociado | [ACC-REG-011](../2.4_Casos_de_prueba/ACC-REG-011.md) · CA-HU-001-04 |
| Preparación | Confirmar las precondiciones del caso. Datos: D-011 de [2.3 Datos](../2.3_Datos_de_prueba.md) (solo datos ficticios).  |

| N.º | Tipo | Paso o punto de verificación | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir **Registro** y escribir `Tomás Quiroga` en Nombre. | El campo muestra el valor. |
| 2 | Paso | Escribir `7` en Contraseña. | — |
| 3 | Verificación | Revisar la lista. | Cumplidas solo: número, sin espacios, sin el nombre. |
| 4 | Paso | Agregar `k` (`7k`). | — |
| 5 | Verificación | Revisar la lista. | Se agrega minúscula. |
| 6 | Paso | Agregar `R` (`7kR`). | — |
| 7 | Verificación | Revisar la lista. | Se agrega mayúscula; longitud sigue sin cumplirse. |
| 8 | Paso | Completar `7kRwpzqx` (8 caracteres). | — |
| 9 | Verificación | Revisar la lista. | Todas las condiciones cumplidas. |
| 10 | Paso | Insertar un espacio después de `7kRw` (`7kRw pzqx`). | — |
| 11 | Verificación | Revisar la lista. | «Sin espacios» pasa a no cumplida. |
| 12 | Paso | Borrar el espacio. | — |
| 13 | Verificación | Revisar la lista. | «Sin espacios» vuelve a cumplida. |
| 14 | Paso | Agregar `Quiroga` al final. | — |
| 15 | Verificación | Revisar la lista. | «Sin el nombre de la persona» pasa a no cumplida. |

**Estado final esperado:** No se crea ninguna cuenta.

**Al terminar:** registrar el estado (Pasó / Falló / Bloqueado), el primer paso divergente y la evidencia en [3.2 Registro de ejecución](../../03_Ejecucion/3.2_Registro_de_ejecucion.md).
