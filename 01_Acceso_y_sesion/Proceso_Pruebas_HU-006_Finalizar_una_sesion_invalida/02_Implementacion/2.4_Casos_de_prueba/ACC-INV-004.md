# ACC-INV-004 · Rol insuficiente con sesión válida

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-INV-004.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-INV-004 |
| Nombre | Rol insuficiente con sesión válida |
| Descripción | Verificar que, cuando la sesión es válida pero el rol no tiene permiso para una función, se muestra "Acceso denegado" y no se ejecuta la operación, sin cerrar la sesión por considerarla inválida. |
| Número de orden de ejecución | 4 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-006 · Flujo principal paso 5 · Criterio: **CA-HU-006-04** |
| Escenario | ESC-ACC-INV-004 · Rol insuficiente con sesión válida · Alterno (diferencial) |
| Tipo de prueba y técnica | Funcional · Caja negra · partición de equivalencia (rol con/ sin permiso) |
| RNF relacionado | — |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../../02_Implementacion/2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../../02_Implementacion/2.3_Datos_de_prueba.md) con la cuenta `sesion.vigente@dsqa.test`. Navegador con sesión iniciada `sesion.vigente@dsqa.test`.<br>2. El usuario tiene rol `Soporte` que no tiene permiso para la función administrativa solicitada.<br>3. La función protegida solicitada requiere rol `Administrador` o permiso específico.<br>4. El correo `fernando.lozada@dsqa.test` no está asociado a una sesión inválida. |
| Datos de entrada | Nombre `Fernando Lozada` · Correo `fernando.lozada@dsqa.test` · Contexto: sesión válida, rol soporte sin permiso (D-004; ver [2.3 Datos](../../02_Implementacion/2.3_Datos_de_prueba.md)) |
| Resultado esperado | Se muestra el mensaje "Acceso denegado". La operación no se ejecuta. La sesión `sesion.vigente@dsqa.test` permanece activa y no se cierra. No se muestra el mensaje "Inicie sesión nuevamente". |
| Postcondición | La sesión `sesion.vigente@dsqa.test` sigue activa con rol `Soporte`. No se ha modificado el estado de la sesión. |
| Evidencia requerida | Captura de la respuesta con el mensaje "Acceso denegado"; captura de que la sesión sigue activa (ej. consulta de perfil); resultado de la verificación de que la operación no se ejecutó y la sesión no se cerró. |