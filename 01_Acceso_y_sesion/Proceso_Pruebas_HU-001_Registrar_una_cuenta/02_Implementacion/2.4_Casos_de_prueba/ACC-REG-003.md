# ACC-REG-003 · Registrar una cuenta de administrador sin aprobación adicional

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REG-003.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REG-003 |
| Nombre | Registrar una cuenta de administrador sin aprobación adicional |
| Descripción | Verificar que el rol administrador se asigna en el registro sin aprobación adicional y que la cuenta queda activa. |
| Número de orden de ejecución | 5 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-001 · Regla «no se exige verificación por correo ni aprobación adicional del rol» · Criterio: **CA-HU-001-01, CA-HU-001-06** |
| Escenario | ESC-ACC-REG-003 · Registro válido con rol administrador · Alterno (happy path) |
| Tipo de prueba y técnica | Funcional · Caja negra · partición de equivalencia (clase válida «administrador» del campo Rol) |
| RNF relacionado | — |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../2.3_Datos_de_prueba.md) con la cuenta `existente.g1@dsqa.test`. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de registro desde este navegador (control del límite de 3 por minuto, RNF-006; ver PA-01).<br>3. El correo `lucia.betancur@dsqa.test` no existe en la base. |
| Datos de entrada | Nombre `Lucía Betancur` · Correo `lucia.betancur@dsqa.test` · Contraseña `Puerto8Azul` · Rol `Administrador` (D-003; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Se acepta el registro; se muestra rol administrador y estado activo; no se pide aprobación. |
| Postcondición | Existe una cuenta activa `lucia.betancur@dsqa.test` con rol administrador. |
| Evidencia requerida | Captura de la confirmación; resultado de la consulta de solo lectura. |
