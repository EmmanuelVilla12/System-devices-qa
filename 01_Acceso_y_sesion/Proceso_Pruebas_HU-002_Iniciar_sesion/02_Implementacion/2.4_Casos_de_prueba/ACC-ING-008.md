# ACC-ING-008 · No mostrar la contraseña en la respuesta de un ingreso aceptado ni de uno rechazado

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-ING-008.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-ING-008 |
| Nombre | No mostrar la contraseña en la respuesta de un ingreso aceptado ni de uno rechazado |
| Descripción | Verificar que la respuesta del ingreso y los datos de la cuenta no muestran la contraseña, tanto si el ingreso se acepta como si se rechaza. |
| Número de orden de ejecución | 8 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-002 · CA-HU-002-06 · RNF-001 · Criterio: **CA-HU-002-06** |
| Escenario | ESC-ACC-ING-008 · Contraseña ausente en las respuestas de ingreso aceptado y rechazado · Calidad |
| Tipo de prueba y técnica | No funcional (seguridad) · Caja negra · inspección de respuesta en el panel de red (dos clases: aceptada y rechazada) |
| RNF relacionado | RNF-001 |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); punto de control de [2.3](../2.3_Datos_de_prueba.md) cargado. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de ingreso desde este navegador (control del límite de 5 por minuto, RNF-006; ver PA-01).<br>3. Panel de red del navegador abierto y con la opción de conservar el registro activada. |
| Datos de entrada | D-008A aceptado: `ingreso.soporte@dsqa.test` / `Duna3Plata`. D-008B rechazado: `ingreso.soporte@dsqa.test` / `Duna3Bronce` (D-008A, D-008B; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | En ninguna de las dos respuestas aparece `Duna3Plata` ni `Duna3Bronce` ni un campo de contraseña; la pantalla tampoco los muestra. |
| Postcondición | Sin sesión al terminar (cerrar la sesión del envío aceptado). |
| Evidencia requerida | Capturas del panel de red con la búsqueda de cada valor. |
