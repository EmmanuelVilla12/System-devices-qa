# ACC-CIE-008 · Utilizar Cerrar sesión en computador y teléfono móvil

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-CIE-008.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-CIE-008 |
| Nombre | Utilizar Cerrar sesión en computador y teléfono móvil |
| Descripción | La acción Cerrar sesión se puede utilizar desde computador y teléfono móvil. |
| Número de orden de ejecución | 8 · [3.1](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md) |
| Requerimiento y criterio asociados | RF-005 · RNF-005 |
| Escenario | ESC-ACC-CIE-008 · Utilizar Cerrar sesión en computador y teléfono móvil · Calidad |
| Tipo de prueba y técnica | No funcional (adaptación) · Caja negra · Recorrido comparativo por dispositivo |
| RNF relacionado | RNF-005 |
| Prioridad | Media |
| Precondición | Cuenta A: Anaís Beltrán · anais.beltran@dsqa.test · contraseña Azulejo74Q · cuenta activa con sesión iniciada; cuenta e historial presentes en el punto de control. Variante A: computador. Variante B: teléfono móvil. Restaurar punto de control entre variantes. |
| Datos de entrada | Cuenta A: Anaís Beltrán · anais.beltran@dsqa.test · contraseña Azulejo74Q · cuenta activa con sesión iniciada; cuenta e historial presentes en el punto de control. Variante A: computador. Variante B: teléfono móvil. Restaurar punto de control entre variantes. (D-008A, D-008B; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado observable | En ambos dispositivos es posible utilizar Cerrar sesión y termina el acceso protegido. |
| Postcondición | La sesión cerrada no vuelve a conceder acceso. La cuenta y el historial permanecen; la cuenta no se desactiva. Tras reingreso solo cuenta la nueva sesión. |
| Evidencia requerida | Durante una futura corrida: captura del estado observable y registro de cuenta antes/después cuando corresponda. Aún no existe evidencia. |
