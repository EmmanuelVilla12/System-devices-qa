# SCR-ACC-CIE-007 · Cerrar la sesión con teclado

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-CIE-007.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-CIE-007 |
| Descripción | Verificar que La acción Cerrar sesión se puede utilizar mediante teclado y se retira el acceso protegido después del cierre. |
| Caso asociado | [ACC-CIE-007](../2.4_Casos_de_prueba/ACC-CIE-007.md) · RNF-004 |
| Preparación | Confirmar estado inicial de D-007 según 2.3 y ambiente; restaurar el punto de control entre variantes cuando aplique. |

| N.º | Tipo Paso/Verificación | Paso | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir una pantalla protegida usando teclado. | — |
| 2 | Paso | Navegar con teclado hasta Cerrar sesión. | — |
| 3 | Paso | Activar Cerrar sesión con teclado. | — |
| 4 | Verificación | La pantalla protegida está disponible. | La pantalla protegida está disponible. |
| 5 | Verificación | El foco alcanza Cerrar sesión. | El foco alcanza Cerrar sesión. |
| 6 | Verificación | La sesión finaliza y deja de estar disponible el acceso protegido. | La sesión finaliza y deja de estar disponible el acceso protegido. |

**Estado final esperado:** Se puede seleccionar Cerrar sesión con teclado y finaliza la sesión.
