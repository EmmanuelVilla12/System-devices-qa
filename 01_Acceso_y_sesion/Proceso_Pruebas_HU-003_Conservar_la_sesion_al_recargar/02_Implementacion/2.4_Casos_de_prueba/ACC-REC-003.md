# ACC-REC-003 · No conceder permisos adicionales al recargar

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REC-003.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REC-003 |
| Nombre | No conceder permisos adicionales al recargar |
| Descripción | Verificar que la recarga no convierte una función no permitida en permitida para el rol de la sesión. |
| Número de orden de ejecución | 3 (independiente; requiere la respuesta de PA-04; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-003 · CA-HU-003-02 «sin conceder permisos adicionales» · RNF-002 · Criterio: **CA-HU-003-02** |
| Escenario | ESC-ACC-REC-003 · La recarga no concede permisos de otro rol · Alterno |
| Tipo de prueba y técnica | Funcional (permisos) · Caja negra · partición de equivalencia (función permitida / función de otro rol) tras la transición de recarga |
| RNF relacionado | RNF-002 |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); punto de control de [2.3](../2.3_Datos_de_prueba.md) cargado; HU-002 y HU-004 disponibles. Navegador sin sesión al empezar.<br>2. Se conoce una función existente restringida a un rol distinto de usuario (PA-04). |
| Datos de entrada | Cuenta `sesion.usuario@dsqa.test` / `Brujula7Mar`. Función restringida: por confirmar en PA-04 (D-003; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Antes y después de recargar, la función restringida responde con Acceso denegado; la sesión sigue vigente. |
| Postcondición | Sesión vigente; cerrarla al terminar. |
| Evidencia requerida | Captura de la respuesta antes y después de la recarga. |
