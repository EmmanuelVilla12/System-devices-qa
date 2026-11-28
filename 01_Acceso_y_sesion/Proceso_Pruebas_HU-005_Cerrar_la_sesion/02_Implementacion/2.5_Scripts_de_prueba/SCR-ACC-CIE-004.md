# SCR-ACC-CIE-004 · Abrir dirección protegida desde historial o pegarla

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-CIE-004.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-CIE-004 |
| Descripción | Verificar que Tras el cierre, abrir nuevamente una dirección protegida desde el historial o pegándola no recupera la sesión finalizada. |
| Caso asociado | [ACC-CIE-004](../2.4_Casos_de_prueba/ACC-CIE-004.md) · CA-HU-005-03 |
| Preparación | Confirmar estado inicial de D-004 según 2.3 y ambiente; restaurar el punto de control entre variantes cuando aplique. |

| N.º | Tipo Paso/Verificación | Paso | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir una pantalla protegida con la sesión iniciada. | — |
| 2 | Paso | Seleccionar Cerrar sesión. | — |
| 3 | Paso | Abrir la dirección protegida anterior desde el historial o pegándola en la barra de direcciones. | — |
| 4 | Verificación | La pantalla se usó antes del cierre. | La pantalla se usó antes del cierre. |
| 5 | Verificación | La sesión termina. | La sesión termina. |
| 6 | Verificación | La dirección protegida requiere nuevo ingreso y no presenta su contenido. | La dirección protegida requiere nuevo ingreso y no presenta su contenido. |

**Estado final esperado:** La dirección protegida requiere nuevo ingreso y no muestra su contenido.
