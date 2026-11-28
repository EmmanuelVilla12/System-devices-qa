# SCR-ACC-CIE-001 · Cerrar la sesión solicitada

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-CIE-001.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-CIE-001 |
| Descripción | Verificar que Al seleccionar Cerrar sesión la identificación termina y la sesión ya no dispone de pantallas protegidas. |
| Caso asociado | [ACC-CIE-001](../2.4_Casos_de_prueba/ACC-CIE-001.md) · CA-HU-005-01 |
| Preparación | Confirmar estado inicial de D-001 según 2.3 y ambiente; restaurar el punto de control entre variantes cuando aplique. |

| N.º | Tipo Paso/Verificación | Paso | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir una pantalla protegida con la sesión iniciada. | — |
| 2 | Paso | Seleccionar la acción Cerrar sesión. | — |
| 3 | Paso | Solicitar una pantalla protegida dentro de la misma sesión. | — |
| 4 | Verificación | La pantalla protegida está disponible antes del cierre. | La pantalla protegida está disponible antes del cierre. |
| 5 | Verificación | La acción se procesa. | La acción se procesa. |
| 6 | Verificación | La sesión finalizó y la pantalla protegida no está disponible para esa sesión; se solicita un nuevo ingreso. | La sesión finalizó y la pantalla protegida no está disponible para esa sesión; se solicita un nuevo ingreso. |

**Estado final esperado:** La acción termina la sesión activa; deja de existir acceso protegido en ella.
