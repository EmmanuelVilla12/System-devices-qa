# ACC-CIE-004 · Abrir dirección protegida desde historial o pegarla

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-CIE-004.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-CIE-004 |
| Nombre | Abrir dirección protegida desde historial o pegarla |
| Descripción | Tras el cierre, abrir nuevamente una dirección protegida desde el historial o pegándola no recupera la sesión finalizada. |
| Número de orden de ejecución | 4 · [3.1](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md) |
| Requerimiento y criterio asociados | RF-005 · CA-HU-005-03 |
| Escenario | ESC-ACC-CIE-004 · Abrir dirección protegida desde historial o pegarla · Excepción |
| Tipo de prueba y técnica | Funcional · Caja negra · Partición de equivalencia |
| RNF relacionado | RNF-002 |
| Prioridad | Alta |
| Precondición | Cuenta A: Anaís Beltrán · anais.beltran@dsqa.test · contraseña Azulejo74Q · cuenta activa con sesión iniciada; cuenta e historial presentes en el punto de control. Dirección protegida previa disponible en historial o para pegar. |
| Datos de entrada | Cuenta A: Anaís Beltrán · anais.beltran@dsqa.test · contraseña Azulejo74Q · cuenta activa con sesión iniciada; cuenta e historial presentes en el punto de control. Dirección protegida previa disponible en historial o para pegar. (D-004; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado observable | La dirección protegida requiere nuevo ingreso y no muestra su contenido. |
| Postcondición | La sesión cerrada no vuelve a conceder acceso. La cuenta y el historial permanecen; la cuenta no se desactiva. Tras reingreso solo cuenta la nueva sesión. |
| Evidencia requerida | Durante una futura corrida: captura del estado observable y registro de cuenta antes/después cuando corresponda. Aún no existe evidencia. |
