# ACC-REG-008 · Rechazar el registro cuando falta un dato obligatorio

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REG-008.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REG-008 |
| Nombre | Rechazar el registro cuando falta un dato obligatorio |
| Descripción | Verificar que la falta de cada dato obligatorio (nombre, correo, contraseña, rol) rechaza la solicitud con el error junto al campo correspondiente. |
| Número de orden de ejecución | 9 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-001 · Descripción «el registro solicita nombre, correo electrónico, contraseña y rol» · Criterio: **CA-HU-001-03** |
| Escenario | ESC-ACC-REG-008 · Dato obligatorio faltante · Excepción (error path) |
| Tipo de prueba y técnica | Funcional · Caja negra · partición de equivalencia (una clase inválida «vacío» por campo, una a la vez) |
| RNF relacionado | — |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../2.3_Datos_de_prueba.md) con la cuenta `existente.g1@dsqa.test`. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de registro desde este navegador (control del límite de 3 por minuto, RNF-006; ver PA-01).<br>3. Los correos `sin.nombre@dsqa.test` y `camila.herrera@dsqa.test` no existen. |
| Datos de entrada | D-008A nombre vacío · D-008B correo vacío · D-008C contraseña vacía · D-008D rol sin seleccionar (resto de campos válidos; ver 2.3) (D-008A, D-008B, D-008C, D-008D; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Los cuatro envíos se rechazan; en cada uno el error aparece junto al campo vacío (Nombre, Correo electrónico, Contraseña o Rol); no se crean cuentas. |
| Postcondición | No existen `sin.nombre@dsqa.test` ni `camila.herrera@dsqa.test`. |
| Evidencia requerida | Captura de cada rechazo; consulta final. |
