# ACC-REC-005 · Cerrar la sesión y pedir un nuevo ingreso al recargar con la sesión caducada

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REC-005.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REC-005 |
| Nombre | Cerrar la sesión y pedir un nuevo ingreso al recargar con la sesión caducada |
| Descripción | Verificar que, si la sesión caducó, recargar una pantalla que exige identificación no conserva el acceso, cierra la sesión y solicita un nuevo ingreso. |
| Número de orden de ejecución | 7 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-003 · CA-HU-003-04 · regla «una sesión rechazada sigue el tratamiento de HU-006» · Criterio: **CA-HU-003-04** |
| Escenario | ESC-ACC-REC-005 · Recarga con sesión caducada · Excepción (error path) |
| Tipo de prueba y técnica | Funcional · Caja negra · transición de estados (vigente → caducada → recarga) |
| RNF relacionado | RNF-002 |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); punto de control de [2.3](../2.3_Datos_de_prueba.md) cargado; HU-002 y HU-004 disponibles. Navegador sin sesión al empezar.<br>2. Se conoce cómo llevar una sesión a la caducidad en ensayo (PA-01). |
| Datos de entrada | Cuenta `sesion.usuario@dsqa.test` / `Brujula7Mar`. Pantalla: **Perfil** (D-005; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Al recargar Perfil después del momento de caducidad no se muestran sus datos, se cierra la sesión y se solicita iniciar sesión. |
| Postcondición | Sin sesión. |
| Evidencia requerida | Captura de la caducidad mostrada y de la pantalla tras la recarga, con la hora del sistema. |
