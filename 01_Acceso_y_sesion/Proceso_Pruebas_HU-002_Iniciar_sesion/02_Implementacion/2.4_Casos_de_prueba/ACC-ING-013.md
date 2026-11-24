# ACC-ING-013 · Iniciar sesión en computador y en teléfono

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-ING-013.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-ING-013 |
| Nombre | Iniciar sesión en computador y en teléfono |
| Descripción | Verificar que el formulario de ingreso y sus errores se leen y usan en computador y en teléfono. |
| Número de orden de ejecución | 13 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-002 · RNF-005 · Criterio: **CA-HU-002-01** |
| Escenario | ESC-ACC-ING-013 · Ingreso utilizable en computador y teléfono móvil · Calidad |
| Tipo de prueba y técnica | No funcional (adaptación) · Caja negra · recorrido en dos tamaños de pantalla (1366×768 y 390×844) |
| RNF relacionado | RNF-005 |
| Prioridad | Media |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); punto de control de [2.3](../2.3_Datos_de_prueba.md) cargado. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de ingreso desde este navegador (control del límite de 5 por minuto, RNF-006; ver PA-01). |
| Datos de entrada | D-013A computador: `ingreso.usuario@dsqa.test` / `Llave8Norte`. D-013B móvil (rechazo y luego ingreso): `ingreso.usuario@dsqa.test` / `Llave8Oeste`, después `Llave8Norte` (D-013A, D-013B; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | En 1366×768 se inicia sesión. En 390×844 el mensaje de rechazo se lee completo, sin texto cortado, y luego se inicia sesión; el botón es visible en ambos. |
| Postcondición | Sesión abierta en móvil; cerrarla al terminar. |
| Evidencia requerida | Capturas de pantalla completa en cada tamaño. |
