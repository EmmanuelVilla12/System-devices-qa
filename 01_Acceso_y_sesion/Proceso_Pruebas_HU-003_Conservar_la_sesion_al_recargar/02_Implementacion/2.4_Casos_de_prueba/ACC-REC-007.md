# ACC-REC-007 · Usar con teclado los controles de la pantalla recargada

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REC-007.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REC-007 |
| Nombre | Usar con teclado los controles de la pantalla recargada |
| Descripción | Verificar que, tras la recarga, los controles de la pantalla siguen identificables y utilizables con teclado. |
| Número de orden de ejecución | 5 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-003 · RNF-004 · Criterio: **CA-HU-003-01** |
| Escenario | ESC-ACC-REC-007 · Controles de la pantalla recargada utilizables con teclado · Calidad |
| Tipo de prueba y técnica | No funcional (accesibilidad) · Caja negra · recorrido de accesibilidad por teclado |
| RNF relacionado | RNF-004 |
| Prioridad | Media |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); punto de control de [2.3](../2.3_Datos_de_prueba.md) cargado; HU-002 y HU-004 disponibles. Navegador sin sesión al empezar.<br>2. Ratón sin uso. |
| Datos de entrada | Cuenta `sesion.usuario@dsqa.test` / `Brujula7Mar`. Pantalla: **Perfil** (D-007; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Tras recargar (Ctrl+R) se recorren con Tab los controles de la pantalla en orden lógico, con foco visible; ninguno queda inaccesible. |
| Postcondición | Sesión vigente; cerrarla al terminar. |
| Evidencia requerida | Video corto del recorrido con Tab. |
