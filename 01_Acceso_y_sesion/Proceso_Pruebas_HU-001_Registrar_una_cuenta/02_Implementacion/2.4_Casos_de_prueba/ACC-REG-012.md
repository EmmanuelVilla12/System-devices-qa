# ACC-REG-012 · Rechazar contraseñas de 7 y de 73 caracteres

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REG-012.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REG-012 |
| Nombre | Rechazar contraseñas de 7 y de 73 caracteres |
| Descripción | Verificar que contraseñas de 7 y 73 caracteres se rechazan e indican que debe corregirse la longitud. |
| Número de orden de ejecución | 12 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-001 · CA-HU-001-04 y CA-HU-001-05 · Criterio: **CA-HU-001-05** |
| Escenario | ESC-ACC-REG-012 · Contraseña fuera de los valores límite (7 y 73) · Excepción (error path) |
| Tipo de prueba y técnica | Funcional · Caja negra · análisis de valores límite (7 y 73) |
| RNF relacionado | — |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../2.3_Datos_de_prueba.md) con la cuenta `existente.g1@dsqa.test`. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de registro desde este navegador (control del límite de 3 por minuto, RNF-006; ver PA-01).<br>3. Los correos `renata.siete@dsqa.test` y `renata.setentaytres@dsqa.test` no existen. |
| Datos de entrada | D-012A: `Renata Vargas` · `renata.siete@dsqa.test` · `Rio4Mar` (7) · Usuario. D-012B: `Renata Vargas` · `renata.setentaytres@dsqa.test` · PWD-73 · Usuario (D-012A, D-012B; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Ambos envíos se rechazan; se indica que la condición de longitud (8 a 72) debe corregirse; no se crean cuentas. |
| Postcondición | No existen las cuentas de D-012A ni D-012B. |
| Evidencia requerida | Captura de cada rechazo; consulta final. |
