# ACC-REG-016 · Rechazar la cuarta solicitud de registro dentro del mismo minuto

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REG-016.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REG-016 |
| Nombre | Rechazar la cuarta solicitud de registro dentro del mismo minuto |
| Descripción | Verificar que hasta 3 solicitudes por minuto se atienden y que la cuarta, en el mismo minuto, se rechaza por exceso de solicitudes sin crear la cuenta. |
| Número de orden de ejecución | 16 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-001 · RNF-006 «máximo 3 solicitudes de registro por minuto» · Criterio: **CA-HU-001-07** |
| Escenario | ESC-ACC-REG-016 · Cuarta solicitud de registro en el mismo minuto · Excepción (error path) |
| Tipo de prueba y técnica | No funcional (límite de uso) con efecto funcional · Caja negra · análisis de valores límite (3.ª y 4.ª solicitud) y transición de estados de la ventana de un minuto |
| RNF relacionado | RNF-006 |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../2.3_Datos_de_prueba.md) con la cuenta `existente.g1@dsqa.test`. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de registro desde este navegador (control del límite de 3 por minuto, RNF-006; ver PA-01).<br>3. Los correos `ventana.a@dsqa.test` a `ventana.d@dsqa.test` no existen. Cronómetro disponible. |
| Datos de entrada | Contraseña `Brisa2025`, rol Usuario: D-016A `Ivonne Primera`/`ventana.a@dsqa.test` · D-016B `Ivonne Segunda`/`ventana.b@…` · D-016C `Ivonne Tercera`/`ventana.c@…` · D-016D `Ivonne Cuarta`/`ventana.d@…` (D-016A, D-016B, D-016C, D-016D; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Las solicitudes 1 a 3 se aceptan. La 4.ª, dentro del mismo minuto, se rechaza por exceso de solicitudes (aviso distinto de un error de datos) y no crea `ventana.d@dsqa.test`. |
| Postcondición | Existen `ventana.a`, `ventana.b` y `ventana.c`; `ventana.d` solo existe después del paso de control 8. |
| Evidencia requerida | Hora de cada envío; captura de cada respuesta; consulta de solo lectura. |
