# ACC-INV-003 · Sin continuidad protegida

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-INV-003.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-INV-003 |
| Nombre | Sin continuidad protegida |
| Descripción | Verificar que, después de que la sesión fue cerrada por invalidez, al intentar volver a una pantalla protegida, no se recupera el acceso y se requiere iniciar sesión nuevamente. |
| Número de orden de ejecución | 3 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-006 · Flujo principal pasos 1–5 · Criterio: **CA-HU-006-03** |
| Escenario | ESC-ACC-INV-003 · Sin continuidad protegida · Excepción (error path) |
| Tipo de prueba y técnica | Funcional · Caja negra · partición de equivalencia (recuperación de pantalla) |
| RNF relacionado | — |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../../02_Implementacion/2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../../02_Implementacion/2.3_Datos_de_prueba.md) con la cuenta `sesion.caducada@dsqa.test`. Navegador sin sesión iniciada.<br>2. La sesión `sesion.caducada@dsqa.test` fue cerrada previamente por invalidez.<br>3. El usuario intenta acceder directamente a una pantalla protegida (sin pasar por el flujo de nuevo ingreso).<br>4. El correo `luis.garcia@dsqa.test` no existe en la base excepto la cuenta base. |
| Datos de entrada | Nombre `Luis García` · Correo `luis.garcia@dsqa.test` · Contexto: pantalla protegida después de cierre (D-003; ver [2.3 Datos](../../02_Implementacion/2.3_Datos_de_prueba.md)) |
| Resultado esperado | No se recupera el acceso a la pantalla protegida. Se muestra el mensaje «Inicie sesión nuevamente» y se requiere identificación nueva. La sesión no se restaura automáticamente. |
| Postcondición | No existe acceso a la pantalla protegida sin nueva sesión. El mensaje de necesidad de nuevo ingreso está presente. |
| Evidencia requerida | Captura de la pantalla bloqueada o del mensaje «Inicie sesión nuevamente»; resultado de la verificación de que no se accede a la pantalla protegida. |