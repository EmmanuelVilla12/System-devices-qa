# ACC-REC-006 · Cerrar la sesión al recargar cuando el servicio la rechaza como inválida

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REC-006.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REC-006 |
| Nombre | Cerrar la sesión al recargar cuando el servicio la rechaza como inválida |
| Descripción | Verificar que una sesión que el servicio rechaza como inválida no se convierte en autorizada al recargar. |
| Número de orden de ejecución | 6 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-003 · Descripción «la operación no convierte una sesión inválida en una sesión autorizada» · Criterio: **CA-HU-003-04** |
| Escenario | ESC-ACC-REC-006 · Recarga con sesión rechazada como inválida · Excepción (error path) |
| Tipo de prueba y técnica | Funcional (seguridad) · Caja negra · partición de equivalencia (sesión válida / sesión inválida) + transición de estados |
| RNF relacionado | RNF-002 |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); punto de control de [2.3](../2.3_Datos_de_prueba.md) cargado; HU-002 y HU-004 disponibles. Navegador sin sesión al empezar.<br>2. Se conoce el mecanismo para invalidar una sesión en ensayo (PA-02). |
| Datos de entrada | Cuenta `sesion.soporte@dsqa.test` / `Ancla2Rojo`. Invalidación: según PA-02 (provisional: alterar el último carácter de la credencial de sesión guardada en el navegador) (D-006; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Después de invalidar la sesión y recargar Perfil no se muestran datos protegidos, se cierra la sesión y se solicita iniciar sesión. |
| Postcondición | Sin sesión. |
| Evidencia requerida | Captura de la alteración y de la pantalla tras la recarga. |
