# ACC-CIE-001 · Cerrar la sesión solicitada

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-CIE-001.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-CIE-001 |
| Nombre | Cerrar la sesión solicitada |
| Descripción | Al seleccionar Cerrar sesión la identificación termina y la sesión ya no dispone de pantallas protegidas. |
| Número de orden de ejecución | 1 · [3.1](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md) |
| Requerimiento y criterio asociados | RF-005 · CA-HU-005-01 |
| Escenario | ESC-ACC-CIE-001 · Cerrar la sesión solicitada · Básico |
| Tipo de prueba y técnica | Funcional · Caja negra · Transición de estados |
| RNF relacionado | RNF-002 |
| Prioridad | Alta |
| Precondición | Cuenta A: Anaís Beltrán · anais.beltran@dsqa.test · contraseña Azulejo74Q · cuenta activa con sesión iniciada; cuenta e historial presentes en el punto de control. |
| Datos de entrada | Cuenta A: Anaís Beltrán · anais.beltran@dsqa.test · contraseña Azulejo74Q · cuenta activa con sesión iniciada; cuenta e historial presentes en el punto de control. (D-001; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado observable | La acción termina la sesión activa; deja de existir acceso protegido en ella. |
| Postcondición | La sesión cerrada no vuelve a conceder acceso. La cuenta y el historial permanecen; la cuenta no se desactiva. Tras reingreso solo cuenta la nueva sesión. |
| Evidencia requerida | Durante una futura corrida: captura del estado observable y registro de cuenta antes/después cuando corresponda. Aún no existe evidencia. |
