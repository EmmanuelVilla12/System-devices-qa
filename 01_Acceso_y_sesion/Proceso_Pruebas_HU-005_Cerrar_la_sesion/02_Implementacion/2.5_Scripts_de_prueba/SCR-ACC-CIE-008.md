# SCR-ACC-CIE-008 · Utilizar Cerrar sesión en computador y teléfono móvil

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-CIE-008.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-CIE-008 |
| Descripción | Verificar que La acción Cerrar sesión se puede utilizar desde computador y teléfono móvil. |
| Caso asociado | [ACC-CIE-008](../2.4_Casos_de_prueba/ACC-CIE-008.md) · RNF-005 |
| Preparación | Confirmar estado inicial de D-008A, D-008B según 2.3 y ambiente; restaurar el punto de control entre variantes cuando aplique. |

| N.º | Tipo Paso/Verificación | Paso | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir una pantalla protegida en computador con sesión iniciada. | — |
| 2 | Paso | Utilizar Cerrar sesión en computador. | — |
| 3 | Paso | Restablecer la precondición de sesión en el punto de control para la variante móvil. | — |
| 4 | Paso | Abrir una pantalla protegida en teléfono móvil con sesión iniciada. | — |
| 5 | Paso | Utilizar Cerrar sesión en teléfono móvil. | — |
| 6 | Verificación | La acción está disponible en computador. | La acción está disponible en computador. |
| 7 | Verificación | La sesión finaliza en computador. | La sesión finaliza en computador. |
| 8 | Verificación | Se restaura el punto de control con sesión activa. | Se restaura el punto de control con sesión activa. |
| 9 | Verificación | La acción está disponible en teléfono móvil. | La acción está disponible en teléfono móvil. |
| 10 | Verificación | La sesión finaliza en teléfono móvil. | La sesión finaliza en teléfono móvil. |

**Estado final esperado:** En ambos dispositivos es posible utilizar Cerrar sesión y termina el acceso protegido.
