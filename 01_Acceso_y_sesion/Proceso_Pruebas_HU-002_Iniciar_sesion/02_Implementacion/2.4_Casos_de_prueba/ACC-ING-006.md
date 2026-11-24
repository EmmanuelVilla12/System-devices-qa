# ACC-ING-006 · Rechazar el ingreso de una cuenta inactiva aunque las credenciales sean correctas

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-ING-006.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-ING-006 |
| Nombre | Rechazar el ingreso de una cuenta inactiva aunque las credenciales sean correctas |
| Descripción | Verificar que una cuenta inactiva no puede iniciar sesión aunque use sus credenciales correctas. |
| Número de orden de ejecución | 6 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-002 · Regla «una cuenta inactiva no puede iniciar sesión» · Criterio: **CA-HU-002-04** |
| Escenario | ESC-ACC-ING-006 · Cuenta inactiva con credenciales correctas · Excepción (error path) |
| Tipo de prueba y técnica | Funcional · Caja negra · partición de equivalencia (clase inválida «cuenta inactiva») |
| RNF relacionado | — |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); punto de control de [2.3](../2.3_Datos_de_prueba.md) cargado. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de ingreso desde este navegador (control del límite de 5 por minuto, RNF-006; ver PA-01).<br>3. La cuenta `cuenta.inactiva@dsqa.test` está en estado inactivo en el punto de control (preparación según PA-03). |
| Datos de entrada | Correo `cuenta.inactiva@dsqa.test` · Contraseña `Pausa6Gris` (correcta) (D-006; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Se rechaza el ingreso y no se habilita una sesión; al abrir Perfil se solicita iniciar sesión. |
| Postcondición | Sin sesión; la cuenta sigue inactiva. |
| Evidencia requerida | Captura del rechazo y de la solicitud de ingreso al abrir Perfil. |
