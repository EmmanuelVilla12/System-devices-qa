# ACC-ING-011 · Iniciar sesión usando solo el teclado

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-ING-011.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-ING-011 |
| Nombre | Iniciar sesión usando solo el teclado |
| Descripción | Verificar que el ingreso se realiza sin ratón, en orden lógico y con foco visible. |
| Número de orden de ejecución | 11 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-002 · RNF-004 · Criterio: **CA-HU-002-01** |
| Escenario | ESC-ACC-ING-011 · Ingreso completo con teclado · Calidad |
| Tipo de prueba y técnica | No funcional (accesibilidad) · Caja negra · recorrido de accesibilidad por teclado |
| RNF relacionado | RNF-004 |
| Prioridad | Media |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); punto de control de [2.3](../2.3_Datos_de_prueba.md) cargado. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de ingreso desde este navegador (control del límite de 5 por minuto, RNF-006; ver PA-01).<br>3. Ratón sin uso. |
| Datos de entrada | Correo `ingreso.admin@dsqa.test` · Contraseña `Torre5Oeste` (D-011; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Con Tab se recorren Correo electrónico, Contraseña y el botón de ingreso en ese orden con foco visible; Enter envía; se inicia sesión. |
| Postcondición | Sesión abierta; cerrarla al terminar. |
| Evidencia requerida | Video corto o capturas del foco. |
