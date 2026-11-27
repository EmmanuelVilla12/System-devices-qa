# ACC-PNE-001 · Mostrar mensaje al ingresar a una URL inexistente como visitante

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-PNE-001.md)

**Estado del artefacto:** Borrador para revisión por pares  
**Estado de ejecución:** No ejecutado

| Campo | Descripción |
|---|---|
| ID | ACC-PNE-001 |
| Nombre | Mostrar mensaje al ingresar a una URL inexistente como visitante |
| Descripción | Verificar que una persona sin iniciar sesión reciba el mensaje de página no encontrada al ingresar a una dirección que no corresponde a una pantalla existente. |
| Orden de ejecución | 1 |
| Requisito y criterio | RF-009 · CA-HU-009-01 y CA-HU-009-02 |
| Escenario | ESC-ACC-PNE-001 · URL inexistente sin autenticación |
| Tipo y técnica de prueba | Funcional · Caja negra · Partición de equivalencia |
| RNF | RNF-004 |
| Prioridad | Alta |
| Precondición | La aplicación está disponible y el navegador no tiene una sesión autenticada. La dirección utilizada es un dato ficticio de prueba y debe comprobarse que no corresponda a una pantalla existente. |
| Datos de entrada | D-001A: `/g5-pruebas/pagina-inexistente-001`. D-002A: visitante sin sesión. |
| Resultado esperado | La aplicación presenta el mensaje «Página no encontrada» en lugar de mostrar una pantalla en blanco. No se ejecuta ninguna operación del negocio. |
| Postcondición | La persona permanece en la aplicación viendo la respuesta de página no encontrada. No se modifican registros. |
| Evidencia requerida | Captura de pantalla de la respuesta obtenida durante la ejecución autorizada. |

## Observaciones

La dirección indicada es un dato ficticio de prueba, no una ruta confirmada de la aplicación. Antes de ejecutar, se debe verificar que realmente no exista.
