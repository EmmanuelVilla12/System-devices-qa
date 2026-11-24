# ACC-REG-017 · Iniciar sesión con la cuenta recién registrada

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REG-017.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REG-017 |
| Nombre | Iniciar sesión con la cuenta recién registrada |
| Descripción | Verificar que la cuenta aceptada queda activa y puede usarse para iniciar sesión mediante HU-002. |
| Número de orden de ejecución | 17 (independiente; requiere HU-002 disponible; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-001 · Descripción «crea una cuenta activa que puede utilizarse para iniciar sesión» · regla «el inicio de sesión se realiza mediante HU-002» · Criterio: **CA-HU-001-01** |
| Escenario | ESC-ACC-REG-017 · Inicio de sesión con la cuenta recién registrada · Alterno (integración) |
| Tipo de prueba y técnica | Funcional (integración con HU-002) · Caja negra · partición de equivalencia (clase válida) en recorrido de integración |
| RNF relacionado | — |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../2.3_Datos_de_prueba.md) con la cuenta `existente.g1@dsqa.test`. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de registro desde este navegador (control del límite de 3 por minuto, RNF-006; ver PA-01).<br>3. HU-002 Iniciar sesión está disponible en la misma versión.<br>4. El correo `fernando.lozada@dsqa.test` no existe. |
| Datos de entrada | Nombre `Fernando Lozada` · Correo `fernando.lozada@dsqa.test` · Contraseña `Cometa63` · Rol `Soporte` (D-017; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | El registro se acepta y, al iniciar sesión con `fernando.lozada@dsqa.test` / `Cometa63`, se establece una sesión de Fernando Lozada con rol soporte. |
| Postcondición | Cuenta activa con una sesión abierta; cerrar sesión al terminar. |
| Evidencia requerida | Captura del registro y del inicio de sesión. |
