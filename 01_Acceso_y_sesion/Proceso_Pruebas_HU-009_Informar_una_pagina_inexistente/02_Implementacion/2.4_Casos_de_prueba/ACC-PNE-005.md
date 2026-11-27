# ACC-PNE-005 · Verificar que una URL inexistente no modifique registros

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-PNE-005.md)

**Estado del artefacto:** Borrador para revisión por pares
**Estado de ejecución:** No ejecutado

| Campo | Descripción |
|---|---|
| ID | ACC-PNE-005 |
| Nombre | Verificar que una URL inexistente no modifique registros |
| Descripción | Comprobar que solicitar una dirección inexistente no cree ni modifique registros de usuarios, equipos o préstamos. |
| Orden de ejecución | 5 |
| Requisito y criterio | RF-009 · CA-HU-009-04 |
| Escenario | ESC-ACC-PNE-005 · Integridad de registros |
| Tipo y técnica de prueba | Funcional · Caja negra · Comparación de estado inicial y final |
| RNF | No aplica |
| Prioridad | Alta |
| Precondición | El entorno de pruebas está disponible y se puede consultar el estado inicial de los registros mediante los mecanismos autorizados. |
| Datos de entrada | D-001A: URL ficticia inexistente. D-002A: visitante sin sesión. |
| Resultado esperado | La solicitud muestra «Página no encontrada» y no crea ni modifica registros de usuarios, equipos o préstamos. |
| Postcondición | Los registros conservan el mismo estado que tenían antes de la solicitud. |
| Evidencia requerida | Evidencia autorizada de la consulta de registros antes y después de la solicitud. |

## Observaciones

La comparación debe realizarse en un entorno de pruebas autorizado. Este caso no debe ejecutar operaciones de creación, edición o eliminación.
