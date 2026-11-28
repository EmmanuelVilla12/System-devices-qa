# ACC-CIE-005 · Ingresar de nuevo con la misma cuenta

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-CIE-005.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-CIE-005 |
| Nombre | Ingresar de nuevo con la misma cuenta |
| Descripción | Después del cierre, un ingreso aceptado con la misma cuenta establece una sesión nueva para determinar el acceso. |
| Número de orden de ejecución | 5 · [3.1](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md) |
| Requerimiento y criterio asociados | RF-005 · CA-HU-005-04 |
| Escenario | ESC-ACC-CIE-005 · Ingresar de nuevo con la misma cuenta · Alterno |
| Tipo de prueba y técnica | Funcional · Caja negra · Transición de estados |
| RNF relacionado | RNF-002 |
| Prioridad | Alta |
| Precondición | Cuenta A: Anaís Beltrán · anais.beltran@dsqa.test · contraseña Azulejo74Q · cuenta activa con sesión iniciada; cuenta e historial presentes en el punto de control. Reingreso con anais.beltran@dsqa.test / Azulejo74Q. |
| Datos de entrada | Cuenta A: Anaís Beltrán · anais.beltran@dsqa.test · contraseña Azulejo74Q · cuenta activa con sesión iniciada; cuenta e historial presentes en el punto de control. Reingreso con anais.beltran@dsqa.test / Azulejo74Q. (D-005; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado observable | El acceso disponible corresponde a la nueva sesión y sus permisos; el acceso anterior no se reutiliza. |
| Postcondición | La sesión cerrada no vuelve a conceder acceso. La cuenta y el historial permanecen; la cuenta no se desactiva. Tras reingreso solo cuenta la nueva sesión. |
| Evidencia requerida | Durante una futura corrida: captura del estado observable y registro de cuenta antes/después cuando corresponda. Aún no existe evidencia. |
