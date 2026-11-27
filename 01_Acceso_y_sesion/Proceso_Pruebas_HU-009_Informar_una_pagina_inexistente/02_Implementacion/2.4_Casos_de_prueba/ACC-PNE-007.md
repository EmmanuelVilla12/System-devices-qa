# ACC-PNE-007 · Verificar la legibilidad del mensaje en computador y móvil

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-PNE-007.md)

**Estado del artefacto:** Borrador para revisión por pares
**Estado de ejecución:** No ejecutado

| Campo | Descripción |
|---|---|
| ID | ACC-PNE-007 |
| Nombre | Verificar la legibilidad del mensaje en computador y móvil |
| Descripción | Comprobar que el mensaje de página inexistente se visualice correctamente en diferentes tamaños de pantalla. |
| Orden de ejecución | 7 |
| Requisito y criterio | RF-009 · RNF-005 |
| Escenario | ESC-ACC-PNE-007 · Visualización adaptable |
| Tipo y técnica de prueba | No funcional · Inspección visual |
| RNF | RNF-005 |
| Prioridad | Media |
| Precondición | La aplicación está disponible y se puede acceder a una dirección inexistente desde el entorno de pruebas. |
| Datos de entrada | D-001A: URL ficticia inexistente. D-006A: resolución 1366x768. D-006B: resolución 390x844. |
| Resultado esperado | El mensaje se visualiza de forma legible en computador y móvil, sin que el texto quede cortado. |
| Postcondición | La respuesta de página no encontrada permanece visible y no se modifican registros. |
| Evidencia requerida | Capturas de pantalla de la visualización en ambas resoluciones durante la ejecución autorizada. |

## Observaciones

Las resoluciones indicadas son datos de prueba. La verificación debe realizarse en el entorno autorizado y no se considera ejecutada todavía.
