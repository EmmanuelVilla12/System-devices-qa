# ACC-CIE-002 · Solicitar ingreso en pantalla protegida después del cierre

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-CIE-002.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-CIE-002 |
| Nombre | Solicitar ingreso en pantalla protegida después del cierre |
| Descripción | Al solicitar una pantalla protegida después del cierre, no se muestra contenido protegido y se solicita un nuevo ingreso. |
| Número de orden de ejecución | 2 · [3.1](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md) |
| Requerimiento y criterio asociados | RF-005 · CA-HU-005-02 |
| Escenario | ESC-ACC-CIE-002 · Solicitar ingreso en pantalla protegida después del cierre · Alterno |
| Tipo de prueba y técnica | Funcional · Caja negra · Partición de equivalencia |
| RNF relacionado | RNF-002 |
| Prioridad | Alta |
| Precondición | Sin sesión activa; dirección de Perfil pendiente de confirmación; cuentas e historial conservados. |
| Datos de entrada | Sin sesión activa; dirección de Perfil pendiente de confirmación; cuentas e historial conservados. (D-002; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado observable | Se solicita iniciar sesión y no se presenta el contenido protegido. |
| Postcondición | La sesión cerrada no vuelve a conceder acceso. La cuenta y el historial permanecen; la cuenta no se desactiva. Tras reingreso solo cuenta la nueva sesión. |
| Evidencia requerida | Durante una futura corrida: captura del estado observable y registro de cuenta antes/después cuando corresponda. Aún no existe evidencia. |
