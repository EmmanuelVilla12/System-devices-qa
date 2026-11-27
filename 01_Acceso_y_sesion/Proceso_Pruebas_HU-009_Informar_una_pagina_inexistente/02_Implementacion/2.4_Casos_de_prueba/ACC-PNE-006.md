# ACC-PNE-006 · Verificar que el mensaje de página inexistente sea identificable

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-PNE-006.md)

**Estado del artefacto:** Borrador para revisión por pares
**Estado de ejecución:** No ejecutado

| Campo | Descripción |
|---|---|
| ID | ACC-PNE-006 |
| Nombre | Verificar que el mensaje de página inexistente sea identificable |
| Descripción | Comprobar que la respuesta permita reconocer que la dirección solicitada no corresponde a una página existente. |
| Orden de ejecución | 6 |
| Requisito y criterio | RF-009 · CA-HU-009-01 · RNF-004 |
| Escenario | ESC-ACC-PNE-006 · Identificación del mensaje |
| Tipo y técnica de prueba | No funcional · Inspección de interfaz |
| RNF | RNF-004 |
| Prioridad | Media |
| Precondición | La aplicación está disponible y se puede consultar una dirección inexistente en el entorno de pruebas. |
| Datos de entrada | D-001A: URL ficticia inexistente. |
| Resultado esperado | La respuesta permite identificar el mensaje «Página no encontrada» y distinguirlo de una pantalla en blanco. |
| Postcondición | La respuesta de página no encontrada permanece visible. No se modifican registros. |
| Evidencia requerida | Captura de pantalla de la respuesta obtenida durante la ejecución autorizada. |

## Observaciones

No se exige un texto adicional que no esté definido en la historia de usuario.
