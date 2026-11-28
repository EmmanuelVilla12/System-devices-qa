# ACC-CIE-006 · Ingresar de nuevo con otra cuenta

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-CIE-006.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-CIE-006 |
| Nombre | Ingresar de nuevo con otra cuenta |
| Descripción | Después del cierre, un ingreso aceptado con otra cuenta establece una sesión que determina el acceso conforme a sus propios permisos. |
| Número de orden de ejecución | 6 · [3.1](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md) |
| Requerimiento y criterio asociados | RF-005 · CA-HU-005-04 |
| Escenario | ESC-ACC-CIE-006 · Ingresar de nuevo con otra cuenta · Alterno |
| Tipo de prueba y técnica | Funcional · Caja negra · Partición de equivalencia |
| RNF relacionado | RNF-002 |
| Prioridad | Alta |
| Precondición | Cuenta A: Anaís Beltrán · anais.beltran@dsqa.test · contraseña Azulejo74Q · cuenta activa con sesión iniciada; cuenta e historial presentes en el punto de control. Reingreso con dario.ospina@dsqa.test / Cedro62Viento. |
| Datos de entrada | Cuenta A: Anaís Beltrán · anais.beltran@dsqa.test · contraseña Azulejo74Q · cuenta activa con sesión iniciada; cuenta e historial presentes en el punto de control. Reingreso con dario.ospina@dsqa.test / Cedro62Viento. (D-006; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado observable | El acceso disponible corresponde a la nueva cuenta y sus permisos, no a la cuenta cuya sesión se cerró. |
| Postcondición | La sesión cerrada no vuelve a conceder acceso. La cuenta y el historial permanecen; la cuenta no se desactiva. Tras reingreso solo cuenta la nueva sesión. |
| Evidencia requerida | Durante una futura corrida: captura del estado observable y registro de cuenta antes/después cuando corresponda. Aún no existe evidencia. |
