# ACC-ING-002 · Iniciar sesión con una cuenta activa de rol administrador

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-ING-002.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-ING-002 |
| Nombre | Iniciar sesión con una cuenta activa de rol administrador |
| Descripción | Verificar que el ingreso reconoce el rol administrador de la cuenta en la sesión iniciada. |
| Número de orden de ejecución | 2 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-002 · Descripción «un ingreso aceptado identifica a la persona y su rol» · Criterio: **CA-HU-002-01** |
| Escenario | ESC-ACC-ING-002 · Ingreso aceptado con cuenta activa de rol administrador · Alterno (happy path) |
| Tipo de prueba y técnica | Funcional · Caja negra · partición de equivalencia (otra clase válida de rol) |
| RNF relacionado | RNF-002 |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); punto de control de [2.3](../2.3_Datos_de_prueba.md) cargado. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de ingreso desde este navegador (control del límite de 5 por minuto, RNF-006; ver PA-01). |
| Datos de entrada | Correo `ingreso.admin@dsqa.test` · Contraseña `Torre5Oeste` (D-002; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Se inicia sesión de `Germán Toro` con rol administrador y se presenta el inicio. |
| Postcondición | Sesión abierta de `ingreso.admin@dsqa.test`; cerrarla al terminar. |
| Evidencia requerida | Captura del inicio y del perfil. |
