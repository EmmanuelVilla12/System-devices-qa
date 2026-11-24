# ACC-ING-004 · Rechazar el ingreso con un correo que no pertenece a ninguna cuenta

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-ING-004.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-ING-004 |
| Nombre | Rechazar el ingreso con un correo que no pertenece a ninguna cuenta |
| Descripción | Verificar que un correo no registrado no inicia sesión y que el mensaje no revela cuál credencial falló. |
| Número de orden de ejecución | 4 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-002 · Descripción «un correo inexistente y una contraseña incorrecta producen el mismo mensaje» · Criterio: **CA-HU-002-03** |
| Escenario | ESC-ACC-ING-004 · Correo inexistente · Excepción (error path) |
| Tipo de prueba y técnica | Funcional · Caja negra · partición de equivalencia (clase inválida «correo no registrado») |
| RNF relacionado | — |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); punto de control de [2.3](../2.3_Datos_de_prueba.md) cargado. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de ingreso desde este navegador (control del límite de 5 por minuto, RNF-006; ver PA-01).<br>3. El correo `no.existe.g1@dsqa.test` no pertenece a ninguna cuenta. |
| Datos de entrada | Correo `no.existe.g1@dsqa.test` · Contraseña `Llave8Norte` (D-004; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | No se inicia sesión. El mensaje de rechazo no menciona que el correo no exista ni que la contraseña sea la errada. Se copia el texto exacto para compararlo en ACC-ING-005. |
| Postcondición | Sin sesión. |
| Evidencia requerida | Captura y transcripción literal del mensaje. |
