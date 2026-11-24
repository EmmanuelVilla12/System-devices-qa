# ACC-ING-003 · Abrir la pantalla protegida solicitada después de iniciar sesión

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-ING-003.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-ING-003 |
| Nombre | Abrir la pantalla protegida solicitada después de iniciar sesión |
| Descripción | Verificar que, si antes del ingreso se solicitó una pantalla protegida permitida para el rol, al iniciar sesión se abre esa pantalla. |
| Número de orden de ejecución | 3 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-002 · Flujo principal paso 6 · Criterio: **CA-HU-002-02** |
| Escenario | ESC-ACC-ING-003 · Retorno a la pantalla protegida solicitada antes del ingreso · Alterno |
| Tipo de prueba y técnica | Funcional · Caja negra · transición de estados (sin sesión con destino pendiente → con sesión en el destino) |
| RNF relacionado | — |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); punto de control de [2.3](../2.3_Datos_de_prueba.md) cargado. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de ingreso desde este navegador (control del límite de 5 por minuto, RNF-006; ver PA-01).<br>3. Se conoce la dirección de **Perfil**: se anota en la preparación abriendo Perfil con una sesión de la cuenta y copiando la dirección; luego se cierra la sesión. |
| Datos de entrada | Pantalla solicitada: **Perfil** (HU-004, permitida a cualquier persona autenticada). Credenciales `ingreso.usuario@dsqa.test` / `Llave8Norte` (D-003; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Al abrir la dirección de Perfil sin sesión se solicita iniciar sesión; tras el ingreso correcto se abre Perfil con los datos de Rocío Londoño, no el inicio. |
| Postcondición | Sesión abierta en Perfil; cerrarla al terminar. |
| Evidencia requerida | Captura de la solicitud de ingreso y de la pantalla abierta después. |
