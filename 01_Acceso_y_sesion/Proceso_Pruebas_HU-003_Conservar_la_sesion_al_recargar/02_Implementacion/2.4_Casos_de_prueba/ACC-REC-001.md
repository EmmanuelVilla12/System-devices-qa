# ACC-REC-001 · Conservar la identidad al recargar una pantalla protegida con sesión vigente

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REC-001.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REC-001 |
| Nombre | Conservar la identidad al recargar una pantalla protegida con sesión vigente |
| Descripción | Verificar que, con una sesión vigente reconocida por el servicio, recargar una pantalla protegida permitida conserva la misma identidad y el acceso. |
| Número de orden de ejecución | 1 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-003 · Flujo principal pasos 1–4 · Criterio: **CA-HU-003-01** |
| Escenario | ESC-ACC-REC-001 · Recarga de Perfil con sesión vigente · Básico (happy path) |
| Tipo de prueba y técnica | Funcional · Caja negra · transición de estados (sesión vigente → recarga → sesión vigente) |
| RNF relacionado | RNF-002 |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); punto de control de [2.3](../2.3_Datos_de_prueba.md) cargado; HU-002 y HU-004 disponibles. Navegador sin sesión al empezar. |
| Datos de entrada | Cuenta `sesion.usuario@dsqa.test` / `Brujula7Mar` (rol usuario). Pantalla: **Perfil** (HU-004) (D-001; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Después de la recarga se muestra Perfil con los datos de `Óscar Bedoya`; no se solicita iniciar sesión. |
| Postcondición | Sesión vigente; cerrarla al terminar. |
| Evidencia requerida | Captura de Perfil antes y después de la recarga. |
