# ACC-REG-006 · Aceptar contraseñas de 8 y de 72 caracteres

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REG-006.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REG-006 |
| Nombre | Aceptar contraseñas de 8 y de 72 caracteres |
| Descripción | Verificar que contraseñas de exactamente 8 y 72 caracteres que cumplen las demás condiciones se aceptan. |
| Número de orden de ejecución | 7 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-001 · CA-HU-001-04 «exige de 8 a 72 caracteres» · Criterio: **CA-HU-001-01, CA-HU-001-04** |
| Escenario | ESC-ACC-REG-006 · Contraseña en los valores límite válidos (8 y 72) · Alterno (happy path) |
| Tipo de prueba y técnica | Funcional · Caja negra · análisis de valores límite (8 y 72) |
| RNF relacionado | — |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../2.3_Datos_de_prueba.md) con la cuenta `existente.g1@dsqa.test`. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de registro desde este navegador (control del límite de 3 por minuto, RNF-006; ver PA-01).<br>3. Los correos `wilson.ocho@dsqa.test` y `wilson.setentaydos@dsqa.test` no existen. |
| Datos de entrada | D-006A: `Wilson Tabares` · `wilson.ocho@dsqa.test` · `Lago7Fri` (8) · Usuario. D-006B: `Wilson Tabares` · `wilson.setentaydos@dsqa.test` · PWD-72 · Usuario (D-006A, D-006B; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Antes de cada envío la lista marca todas las condiciones como cumplidas; ambos registros se aceptan. |
| Postcondición | Existen las dos cuentas de Wilson Tabares. |
| Evidencia requerida | Captura de la lista de condiciones antes de enviar y de cada confirmación. |
