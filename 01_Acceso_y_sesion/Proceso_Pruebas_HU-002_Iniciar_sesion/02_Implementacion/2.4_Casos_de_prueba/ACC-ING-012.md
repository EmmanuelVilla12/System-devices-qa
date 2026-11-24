# ACC-ING-012 · Anunciar los campos y el error de ingreso con lector de pantalla

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-ING-012.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-ING-012 |
| Nombre | Anunciar los campos y el error de ingreso con lector de pantalla |
| Descripción | Verificar que los campos se identifican y que el mensaje de rechazo se comunica de manera accesible. |
| Número de orden de ejecución | 12 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-002 · RNF-004 · Criterio: **CA-HU-002-03** |
| Escenario | ESC-ACC-ING-012 · Error de ingreso identificable con lector de pantalla · Calidad |
| Tipo de prueba y técnica | No funcional (accesibilidad) · Caja negra · recorrido con lector de pantalla |
| RNF relacionado | RNF-004 |
| Prioridad | Media |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); punto de control de [2.3](../2.3_Datos_de_prueba.md) cargado. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de ingreso desde este navegador (control del límite de 5 por minuto, RNF-006; ver PA-01).<br>3. NVDA (o equivalente) activo. |
| Datos de entrada | Correo `ingreso.usuario@dsqa.test` · Contraseña `Llave8Este` (incorrecta) (D-012; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | El lector anuncia «Correo electrónico» y «Contraseña» al enfocarlos y, tras el envío, anuncia el mensaje de rechazo. |
| Postcondición | Sin sesión. |
| Evidencia requerida | Transcripción o grabación del audio del lector. |
