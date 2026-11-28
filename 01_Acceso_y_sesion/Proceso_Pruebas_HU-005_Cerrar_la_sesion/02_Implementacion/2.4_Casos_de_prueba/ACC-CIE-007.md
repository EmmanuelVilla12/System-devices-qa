# ACC-CIE-007 · Cerrar la sesión con teclado

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-CIE-007.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-CIE-007 |
| Nombre | Cerrar la sesión con teclado |
| Descripción | La acción Cerrar sesión se puede utilizar mediante teclado y se retira el acceso protegido después del cierre. |
| Número de orden de ejecución | 7 · [3.1](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md) |
| Requerimiento y criterio asociados | RF-005 · RNF-004 |
| Escenario | ESC-ACC-CIE-007 · Cerrar la sesión con teclado · Calidad |
| Tipo de prueba y técnica | No funcional (accesibilidad) · Caja negra · Recorrido por teclado |
| RNF relacionado | RNF-004 |
| Prioridad | Media |
| Precondición | Cuenta A: Anaís Beltrán · anais.beltran@dsqa.test · contraseña Azulejo74Q · cuenta activa con sesión iniciada; cuenta e historial presentes en el punto de control. Computador de ensayo y teclado. |
| Datos de entrada | Cuenta A: Anaís Beltrán · anais.beltran@dsqa.test · contraseña Azulejo74Q · cuenta activa con sesión iniciada; cuenta e historial presentes en el punto de control. Computador de ensayo y teclado. (D-007; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado observable | Se puede seleccionar Cerrar sesión con teclado y finaliza la sesión. |
| Postcondición | La sesión cerrada no vuelve a conceder acceso. La cuenta y el historial permanecen; la cuenta no se desactiva. Tras reingreso solo cuenta la nueva sesión. |
| Evidencia requerida | Durante una futura corrida: captura del estado observable y registro de cuenta antes/después cuando corresponda. Aún no existe evidencia. |
