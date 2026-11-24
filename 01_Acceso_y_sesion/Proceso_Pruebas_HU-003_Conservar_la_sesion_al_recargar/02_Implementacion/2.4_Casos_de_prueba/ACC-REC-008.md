# ACC-REC-008 · Mantener legible y utilizable la pantalla recargada en computador y teléfono

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REC-008.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REC-008 |
| Nombre | Mantener legible y utilizable la pantalla recargada en computador y teléfono |
| Descripción | Verificar que la pantalla recargada conserva sus controles utilizables en computador y teléfono móvil. |
| Número de orden de ejecución | 8 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-003 · RNF-005 · Criterio: **CA-HU-003-01** |
| Escenario | ESC-ACC-REC-008 · Pantalla recargada legible en computador y teléfono · Calidad |
| Tipo de prueba y técnica | No funcional (adaptación) · Caja negra · recorrido en dos tamaños (1366×768 y 390×844) |
| RNF relacionado | RNF-005 |
| Prioridad | Media |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); punto de control de [2.3](../2.3_Datos_de_prueba.md) cargado; HU-002 y HU-004 disponibles. Navegador sin sesión al empezar. |
| Datos de entrada | D-008A computador y D-008B móvil con `sesion.soporte@dsqa.test` / `Ancla2Rojo`. Pantalla: **Perfil** (D-008A, D-008B; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | En 1366×768 y en 390×844, tras la recarga, Perfil se muestra completo, sin texto cortado ni desplazamiento horizontal, y con la misma identidad. |
| Postcondición | Sesión vigente; cerrarla al terminar. |
| Evidencia requerida | Capturas de pantalla completa en cada tamaño. |
