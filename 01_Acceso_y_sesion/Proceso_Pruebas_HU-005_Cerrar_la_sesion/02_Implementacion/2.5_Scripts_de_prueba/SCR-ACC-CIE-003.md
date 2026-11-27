# SCR-ACC-CIE-003 · Volver con el botón Atrás a la pantalla protegida anterior

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-CIE-003.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-CIE-003 |
| Descripción | Verificar que Tras cerrar la sesión desde una pantalla protegida, usar Atrás no restablece el acceso. |
| Caso asociado | [ACC-CIE-003](../2.4_Casos_de_prueba/ACC-CIE-003.md) · CA-HU-005-03 |
| Preparación | Confirmar estado inicial de D-003 según 2.3 y ambiente; restaurar el punto de control entre variantes cuando aplique. |

| N.º | Tipo Paso/Verificación | Paso | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir una pantalla protegida con la sesión iniciada. | — |
| 2 | Paso | Seleccionar Cerrar sesión. | — |
| 3 | Paso | Usar el botón Atrás del navegador. | — |
| 4 | Verificación | La pantalla protegida fue usada antes del cierre. | La pantalla protegida fue usada antes del cierre. |
| 5 | Verificación | La sesión termina. | La sesión termina. |
| 6 | Verificación | El acceso anterior no se restablece; no se muestra contenido protegido y se requiere nuevo ingreso. | El acceso anterior no se restablece; no se muestra contenido protegido y se requiere nuevo ingreso. |

**Estado final esperado:** No se restablece el acceso anterior; la pantalla protegida no muestra su contenido y requiere nuevo ingreso.
