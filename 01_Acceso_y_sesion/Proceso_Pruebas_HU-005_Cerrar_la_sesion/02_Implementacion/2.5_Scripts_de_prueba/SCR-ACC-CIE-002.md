# SCR-ACC-CIE-002 · Solicitar ingreso en pantalla protegida después del cierre

[Índice de casos](../2.4_Casos_de_prueba/00_Indice_de_casos.md) · [Caso asociado](../2.4_Casos_de_prueba/ACC-CIE-002.md) · [Matriz](../2.2_Matriz_de_trazabilidad.md)

**Estado del artefacto:** borrador para revisión por pares · script manual.

| Elemento | Contenido |
|---|---|
| Nombre | SCR-ACC-CIE-002 |
| Descripción | Verificar que Al solicitar una pantalla protegida después del cierre, no se muestra contenido protegido y se solicita un nuevo ingreso. |
| Caso asociado | [ACC-CIE-002](../2.4_Casos_de_prueba/ACC-CIE-002.md) · CA-HU-005-02 |
| Preparación | Confirmar estado inicial de D-002 según 2.3 y ambiente; restaurar el punto de control entre variantes cuando aplique. |

| N.º | Tipo Paso/Verificación | Paso | Resultado esperado |
|---:|---|---|---|
| 1 | Paso | Abrir una pantalla protegida sin sesión iniciada. | — |
| 2 | Verificación | Se solicita un nuevo ingreso y no se muestra contenido protegido. | Se solicita un nuevo ingreso y no se muestra contenido protegido. |

**Estado final esperado:** Se solicita iniciar sesión y no se presenta el contenido protegido.
