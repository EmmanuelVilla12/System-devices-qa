# ACC-ING-001 · Iniciar sesión con credenciales válidas de una cuenta activa

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-ING-001.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-ING-001 |
| Nombre | Iniciar sesión con credenciales válidas de una cuenta activa |
| Descripción | Verificar que una cuenta activa con credenciales válidas inicia una sesión con su identidad y su rol y presenta el inicio. |
| Número de orden de ejecución | 1 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-002 · Flujo principal pasos 1–6 · Criterio: **CA-HU-002-01** |
| Escenario | ESC-ACC-ING-001 · Ingreso aceptado con cuenta activa de rol usuario · Básico (happy path) |
| Tipo de prueba y técnica | Funcional · Caja negra · partición de equivalencia (clase válida: cuenta activa + credenciales correctas) |
| RNF relacionado | RNF-002 |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); punto de control de [2.3](../2.3_Datos_de_prueba.md) cargado. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de ingreso desde este navegador (control del límite de 5 por minuto, RNF-006; ver PA-01). |
| Datos de entrada | Correo `ingreso.usuario@dsqa.test` · Contraseña `Llave8Norte` (D-001; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Se inicia sesión; la aplicación identifica a `Rocío Londoño` con rol usuario y presenta el inicio. |
| Postcondición | Sesión abierta de `ingreso.usuario@dsqa.test`; cerrarla al terminar (HU-005). |
| Evidencia requerida | Captura del inicio con la identidad visible. |
