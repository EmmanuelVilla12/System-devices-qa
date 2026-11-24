# ACC-REG-002 · Registrar una cuenta válida con rol soporte

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REG-002.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REG-002 |
| Nombre | Registrar una cuenta válida con rol soporte |
| Descripción | Verificar que el registro con rol soporte crea una cuenta activa con ese rol, sin pasos de aprobación. |
| Número de orden de ejecución | 4 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-001 · Flujo principal paso 3 · regla «sin aprobación adicional del rol» · Criterio: **CA-HU-001-01, CA-HU-001-06** |
| Escenario | ESC-ACC-REG-002 · Registro válido con rol soporte · Alterno (happy path) |
| Tipo de prueba y técnica | Funcional · Caja negra · partición de equivalencia (clase válida «soporte» del campo Rol) |
| RNF relacionado | — |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../2.3_Datos_de_prueba.md) con la cuenta `existente.g1@dsqa.test`. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de registro desde este navegador (control del límite de 3 por minuto, RNF-006; ver PA-01).<br>3. El correo `esteban.quintero@dsqa.test` no existe en la base. |
| Datos de entrada | Nombre `Esteban Quintero` · Correo `esteban.quintero@dsqa.test` · Contraseña `Nevado2031` · Rol `Soporte` (D-002; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Se acepta el registro; los datos mostrados indican rol soporte; no se pide aprobación ni confirmación por correo; la cuenta queda activa. |
| Postcondición | Existe una cuenta activa `esteban.quintero@dsqa.test` con rol soporte. |
| Evidencia requerida | Captura de la confirmación; resultado de la consulta de solo lectura. |
