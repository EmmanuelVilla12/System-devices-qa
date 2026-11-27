# ACC-PNE-004 · Denegar acceso a una pantalla restringida sin permiso

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-PNE-004.md)

**Estado del artefacto:** Borrador para revisión por pares
**Estado de ejecución:** No ejecutado

| Campo | Descripción |
|---|---|
| ID | ACC-PNE-004 |
| Nombre | Denegar acceso a una pantalla restringida sin permiso |
| Descripción | Verificar que una persona autenticada sin los permisos necesarios reciba la respuesta de acceso denegado y no una respuesta de página inexistente. |
| Orden de ejecución | 4 |
| Requisito y criterio | RF-009 · CA-HU-009-03 · Dependencia HU-008 |
| Escenario | ESC-ACC-PNE-004 · Pantalla existente con usuario sin permiso |
| Tipo y técnica de prueba | Funcional · Caja negra · Tabla de decisión |
| RNF | No aplica |
| Prioridad | Alta |
| Precondición | Existe una sesión autenticada con un usuario que no tiene permiso para acceder a una pantalla existente y protegida. |
| Datos de entrada | D-004A: ruta protegida confirmada. D-005A: usuario de prueba sin permiso. |
| Resultado esperado | La aplicación presenta la respuesta «Acceso denegado», según HU-008. No presenta «Página no encontrada». |
| Postcondición | No se accede al contenido restringido ni se modifican registros. |
| Evidencia requerida | Captura de pantalla de la respuesta obtenida durante la ejecución autorizada. |

## Observaciones

La ruta y los permisos deben ser confirmados por el equipo responsable. Este caso verifica la integración con HU-008.
