# ACC-PNE-002 · Mostrar mensaje al ingresar a una URL inexistente como usuario autenticado

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-PNE-002.md)

**Estado del artefacto:** Borrador para revisión por pares  
**Estado de ejecución:** No ejecutado

| Campo | Descripción |
|---|---|
| ID | ACC-PNE-002 |
| Nombre | Mostrar mensaje al ingresar a una URL inexistente como usuario autenticado |
| Descripción | Verificar que una persona con sesión iniciada reciba el mensaje de página no encontrada al ingresar a una dirección que no corresponde a una pantalla existente. |
| Orden de ejecución | 2 |
| Requisito y criterio | RF-009 · CA-HU-009-01 y CA-HU-009-02 |
| Escenario | ESC-ACC-PNE-002 · URL inexistente con autenticación |
| Tipo y técnica de prueba | Funcional · Caja negra · Partición de equivalencia |
| RNF | RNF-004 |
| Prioridad | Alta |
| Precondición | La aplicación está disponible y existe una sesión autenticada válida en el entorno de pruebas. La dirección utilizada debe comprobarse como inexistente. |
| Datos de entrada | D-001A: `/g5-pruebas/pagina-inexistente-001`. D-003A: usuario de prueba autenticado. |
| Resultado esperado | La aplicación presenta el mensaje «Página no encontrada» en lugar de mostrar una pantalla en blanco. No se ejecuta ninguna operación del negocio. |
| Postcondición | La persona permanece en la aplicación viendo la respuesta de página no encontrada. No se modifican registros. |
| Evidencia requerida | Captura de pantalla de la respuesta obtenida durante la ejecución autorizada. |

## Observaciones

La dirección indicada es un dato ficticio de prueba, no una ruta confirmada de la aplicación. Antes de ejecutar, se debe verificar que realmente no exista.
