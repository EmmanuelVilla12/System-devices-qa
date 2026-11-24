# ACC-ING-005 · Rechazar el ingreso con contraseña incorrecta y mostrar el mismo mensaje que con correo inexistente

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-ING-005.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-ING-005 |
| Nombre | Rechazar el ingreso con contraseña incorrecta y mostrar el mismo mensaje que con correo inexistente |
| Descripción | Verificar que una contraseña incorrecta de un correo registrado no inicia sesión y produce exactamente el mismo mensaje que un correo inexistente. |
| Número de orden de ejecución | 5 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-002 · CA-HU-002-03 «ambos casos presentan el mismo mensaje» · Criterio: **CA-HU-002-03** |
| Escenario | ESC-ACC-ING-005 · Contraseña incorrecta con correo existente · Excepción (error path) |
| Tipo de prueba y técnica | Funcional · Caja negra · partición de equivalencia (contraseña distinta y contraseña con otra capitalización) + comparación con la clase «correo inexistente» |
| RNF relacionado | — |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); punto de control de [2.3](../2.3_Datos_de_prueba.md) cargado. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de ingreso desde este navegador (control del límite de 5 por minuto, RNF-006; ver PA-01). |
| Datos de entrada | D-005A referencia: `no.existe.g1@dsqa.test` / `Llave8Norte`. D-005B: `ingreso.usuario@dsqa.test` / `Llave8Sur`. D-005C: `ingreso.usuario@dsqa.test` / `llave8norte` (D-005A, D-005B, D-005C; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Ninguno de los tres envíos inicia sesión; los tres mensajes son textualmente iguales y no indican cuál credencial falló. |
| Postcondición | Sin sesión; la cuenta `ingreso.usuario@dsqa.test` sigue activa. |
| Evidencia requerida | Capturas y transcripción literal de los tres mensajes. |
