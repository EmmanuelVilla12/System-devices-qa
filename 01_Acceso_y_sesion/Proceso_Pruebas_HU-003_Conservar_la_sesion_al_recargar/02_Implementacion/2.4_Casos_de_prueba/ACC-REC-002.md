# ACC-REC-002 · Mantener las funciones permitidas del rol después de recargar

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REC-002.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REC-002 |
| Nombre | Mantener las funciones permitidas del rol después de recargar |
| Descripción | Verificar que, al recargar una pantalla de la aplicación, se mantienen las funciones permitidas para el rol de la sesión. |
| Número de orden de ejecución | 2 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-003 · CA-HU-003-02 · Criterio: **CA-HU-003-02** |
| Escenario | ESC-ACC-REC-002 · Funciones del rol iguales antes y después de recargar · Alterno |
| Tipo de prueba y técnica | Funcional · Caja negra · comparación de estado antes/después (transición de estados) |
| RNF relacionado | RNF-002 |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); punto de control de [2.3](../2.3_Datos_de_prueba.md) cargado; HU-002 y HU-004 disponibles. Navegador sin sesión al empezar. |
| Datos de entrada | Cuenta `sesion.soporte@dsqa.test` / `Ancla2Rojo` (rol soporte). Pantalla: la que se presenta después del ingreso (D-002; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | La lista de opciones y accesos visibles anotada antes de la recarga es idéntica a la observada después; no aparecen opciones nuevas ni desaparecen las permitidas. |
| Postcondición | Sesión vigente; cerrarla al terminar. |
| Evidencia requerida | Captura del menú u opciones antes y después. |
