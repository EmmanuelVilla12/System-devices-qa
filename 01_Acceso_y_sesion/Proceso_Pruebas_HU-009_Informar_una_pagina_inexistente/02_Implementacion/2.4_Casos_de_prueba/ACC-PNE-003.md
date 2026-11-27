# ACC-PNE-003 · Solicitar inicio de sesión para acceder a una página restringida

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-PNE-003.md)

**Estado del artefacto:** Borrador para revisión por pares  
**Estado de ejecución:** No ejecutado

| Campo | Descripción |
|---|---|
| ID | ACC-PNE-003 |
| Nombre | Solicitar inicio de sesión para acceder a una página restringida |
| Descripción | Verificar que una persona sin sesión que intente acceder a una pantalla existente y protegida reciba la respuesta de autenticación correspondiente, sin mostrar «Página no encontrada». |
| Orden de ejecución | 3 |
| Requisito y criterio | RF-009 · CA-HU-009-03 · Dependencia HU-008 |
| Escenario | ESC-ACC-PNE-003 · Pantalla existente sin autenticación |
| Tipo y técnica de prueba | Funcional · Caja negra · Tabla de decisión |
| RNF | No aplica |
| Prioridad | Alta |
| Precondición | La aplicación está disponible. La persona no tiene una sesión iniciada y se dispone de una ruta existente y protegida, confirmada por el equipo responsable. |
| Datos de entrada | D-004A: ruta existente y protegida, pendiente de confirmar. D-002A: visitante sin sesión. |
| Resultado esperado | La aplicación solicita iniciar sesión según el comportamiento definido en HU-008. No presenta «Página no encontrada». |
| Postcondición | No se accede al contenido protegido ni se modifican registros. |
| Evidencia requerida | Captura de pantalla de la respuesta obtenida durante la ejecución autorizada. |

## Observaciones

La ruta protegida debe ser proporcionada o confirmada por el equipo responsable. No se debe inventar una ruta de la aplicación. Este caso verifica la integración con HU-008, sin diseñar ni probar sus funcionalidades internas.
