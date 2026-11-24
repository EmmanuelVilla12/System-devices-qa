# ACC-ING-007 · Rechazar la sexta solicitud de ingreso dentro del mismo minuto

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-ING-007.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-ING-007 |
| Nombre | Rechazar la sexta solicitud de ingreso dentro del mismo minuto |
| Descripción | Verificar que hasta 5 solicitudes de ingreso por minuto se atienden y que la sexta, en el mismo minuto, se rechaza por exceso sin iniciar sesión. |
| Número de orden de ejecución | 7 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-002 · RNF-006 «limitar el ingreso a 5 solicitudes por minuto» · Criterio: **CA-HU-002-05** |
| Escenario | ESC-ACC-ING-007 · Sexta solicitud de ingreso en el mismo minuto · Excepción (error path) |
| Tipo de prueba y técnica | No funcional (límite de uso) con efecto funcional · Caja negra · análisis de valores límite (5.ª y 6.ª solicitud) y transición de estados de la ventana |
| RNF relacionado | RNF-006 |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); punto de control de [2.3](../2.3_Datos_de_prueba.md) cargado. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de ingreso desde este navegador (control del límite de 5 por minuto, RNF-006; ver PA-01).<br>3. Cronómetro disponible. La opción Cerrar sesión (HU-005) está disponible. |
| Datos de entrada | Seis envíos con `limite.ingreso@dsqa.test` / `Ritmo4Seis` (D-007A a D-007F) (D-007A, D-007B, D-007C, D-007D, D-007E, D-007F; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Los envíos 1 a 5 inician sesión (se cierra la sesión entre uno y otro). El 6.º, dentro del mismo minuto, se rechaza por exceso de solicitudes (aviso distinto del de credenciales) y no inicia sesión. |
| Postcondición | Sin sesión al terminar. |
| Evidencia requerida | Hora de cada envío; captura de cada resultado. |
