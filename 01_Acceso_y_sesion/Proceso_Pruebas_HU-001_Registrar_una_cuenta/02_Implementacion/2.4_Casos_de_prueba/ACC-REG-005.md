# ACC-REG-005 · Aceptar nombres de 3 y de 50 caracteres

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REG-005.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REG-005 |
| Nombre | Aceptar nombres de 3 y de 50 caracteres |
| Descripción | Verificar que los nombres de exactamente 3 y 50 caracteres se aceptan y se muestran completos. |
| Número de orden de ejecución | 6 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-001 · Descripción «el nombre admite de 3 a 50 caracteres» · Criterio: **CA-HU-001-01** |
| Escenario | ESC-ACC-REG-005 · Nombre en los valores límite válidos (3 y 50) · Alterno (happy path) |
| Tipo de prueba y técnica | Funcional · Caja negra · análisis de valores límite (3 y 50) |
| RNF relacionado | — |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../2.3_Datos_de_prueba.md) con la cuenta `existente.g1@dsqa.test`. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de registro desde este navegador (control del límite de 3 por minuto, RNF-006; ver PA-01).<br>3. Los correos `teo.limite3@dsqa.test` y `nombre.cincuenta@dsqa.test` no existen. |
| Datos de entrada | D-005A: `Teo` (3) · `teo.limite3@dsqa.test` · `Bosque52` · Usuario. D-005B: `Ximena Alejandra Giraldo Cárdenas de Montoya Henao` (50) · `nombre.cincuenta@dsqa.test` · `Bosque52` · Usuario (D-005A, D-005B; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Los dos registros se aceptan; el nombre de 50 caracteres se muestra completo, con tildes y sin recortes. |
| Postcondición | Existen las cuentas `teo.limite3@dsqa.test` y `nombre.cincuenta@dsqa.test`. |
| Evidencia requerida | Captura de cada confirmación. |
