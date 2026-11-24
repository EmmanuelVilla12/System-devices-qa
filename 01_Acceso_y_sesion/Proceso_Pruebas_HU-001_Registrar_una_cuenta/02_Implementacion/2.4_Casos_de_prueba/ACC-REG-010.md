# ACC-REG-010 · Rechazar correos con formato inválido

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REG-010.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REG-010 |
| Nombre | Rechazar correos con formato inválido |
| Descripción | Verificar que tres formatos de correo claramente inválidos se rechazan con el error junto al campo Correo. |
| Número de orden de ejecución | 11 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-001 · Descripción «el correo debe ser válido» · Criterio: **CA-HU-001-03** |
| Escenario | ESC-ACC-REG-010 · Correo con formato inválido · Excepción (error path) |
| Tipo de prueba y técnica | Funcional · Caja negra · partición de equivalencia (clases inválidas: sin @, con dos @, sin parte local) |
| RNF relacionado | — |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../2.3_Datos_de_prueba.md) con la cuenta `existente.g1@dsqa.test`. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de registro desde este navegador (control del límite de 3 por minuto, RNF-006; ver PA-01). |
| Datos de entrada | Nombre `Felipe Correa` · Contraseña `Bosque52` · Rol Usuario con: D-010A `felipe.correadsqa.test` · D-010B `felipe@@dsqa.test` · D-010C `@dsqa.test` (D-010A, D-010B, D-010C; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Los tres envíos se rechazan; el error aparece junto a Correo electrónico; no se crean cuentas. |
| Postcondición | No existe ninguna cuenta a nombre de `Felipe Correa`. |
| Evidencia requerida | Captura de cada error. |
