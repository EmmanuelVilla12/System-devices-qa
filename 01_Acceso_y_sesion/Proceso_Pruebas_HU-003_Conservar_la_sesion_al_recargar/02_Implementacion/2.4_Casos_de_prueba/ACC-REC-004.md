# ACC-REC-004 · Conservar la sesión al recargar sin ampliar su momento de caducidad

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REC-004.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REC-004 |
| Nombre | Conservar la sesión al recargar sin ampliar su momento de caducidad |
| Descripción | Verificar que recargar antes de la caducidad conserva la sesión y no cambia su momento de vencimiento. |
| Número de orden de ejecución | 4 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-003 · CA-HU-003-03 · regla «conservar sesión no significa habilitar una sesión de duración indefinida» · Criterio: **CA-HU-003-03** |
| Escenario | ESC-ACC-REC-004 · Recargas antes de la caducidad sin ampliar la vigencia · Alterno |
| Tipo de prueba y técnica | Funcional · Caja negra · comparación de estado antes/después; valor observado en Perfil (HU-004) |
| RNF relacionado | RNF-002 |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); punto de control de [2.3](../2.3_Datos_de_prueba.md) cargado; HU-002 y HU-004 disponibles. Navegador sin sesión al empezar.<br>2. HU-004 Perfil muestra el momento de caducidad de la sesión. |
| Datos de entrada | Cuenta `sesion.usuario@dsqa.test` / `Brujula7Mar`. Tres recargas separadas por 2 minutos (D-004; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | La sesión se conserva tras cada recarga y el momento de caducidad mostrado en Perfil no cambia. |
| Postcondición | Sesión vigente; cerrarla al terminar. |
| Evidencia requerida | Captura de la caducidad mostrada antes y después de cada recarga, con la hora del sistema. |
