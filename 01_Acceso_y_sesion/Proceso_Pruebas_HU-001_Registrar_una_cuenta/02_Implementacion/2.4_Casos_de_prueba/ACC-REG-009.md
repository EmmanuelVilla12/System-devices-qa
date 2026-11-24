# ACC-REG-009 · Rechazar nombres de 2 y de 51 caracteres

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REG-009.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REG-009 |
| Nombre | Rechazar nombres de 2 y de 51 caracteres |
| Descripción | Verificar que nombres de 2 y 51 caracteres se rechazan con el error junto a Nombre y sin crear cuenta. |
| Número de orden de ejecución | 10 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-001 · CA-HU-001-03 «el nombre tiene menos de 3 o más de 50 caracteres» · Criterio: **CA-HU-001-03** |
| Escenario | ESC-ACC-REG-009 · Nombre fuera de los valores límite (2 y 51) · Excepción (error path) |
| Tipo de prueba y técnica | Funcional · Caja negra · análisis de valores límite (2 y 51) |
| RNF relacionado | — |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../2.3_Datos_de_prueba.md) con la cuenta `existente.g1@dsqa.test`. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de registro desde este navegador (control del límite de 3 por minuto, RNF-006; ver PA-01).<br>3. Los correos `bo.limite2@dsqa.test` y `nombre.cincuentayuno@dsqa.test` no existen. |
| Datos de entrada | D-009A: `Bo` (2) · `bo.limite2@dsqa.test` · `Bosque52` · Usuario. D-009B: `Ximena Alejandra Giraldo Cárdenas de Montoyas Henao` (51) · `nombre.cincuentayuno@dsqa.test` · `Bosque52` · Usuario (D-009A, D-009B; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Ambos envíos se rechazan; el error aparece junto a Nombre; no se crean cuentas. |
| Postcondición | No existen las cuentas de D-009A ni D-009B. |
| Evidencia requerida | Captura de cada error; consulta final. |
