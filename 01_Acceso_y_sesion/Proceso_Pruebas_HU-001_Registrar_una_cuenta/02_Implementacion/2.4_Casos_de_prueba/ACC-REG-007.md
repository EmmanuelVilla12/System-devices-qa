# ACC-REG-007 · Rechazar el registro con un correo que ya pertenece a una cuenta

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REG-007.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REG-007 |
| Nombre | Rechazar el registro con un correo que ya pertenece a una cuenta |
| Descripción | Verificar que un correo existente no genera una segunda cuenta y que se identifica como el dato a corregir. |
| Número de orden de ejecución | 8 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-001 · Regla «el correo no se repite entre cuentas» · Criterio: **CA-HU-001-02** |
| Escenario | ESC-ACC-REG-007 · Correo ya registrado · Excepción (error path) |
| Tipo de prueba y técnica | Funcional · Caja negra · partición de equivalencia (clase inválida «correo registrado») |
| RNF relacionado | — |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../2.3_Datos_de_prueba.md) con la cuenta `existente.g1@dsqa.test`. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de registro desde este navegador (control del límite de 3 por minuto, RNF-006; ver PA-01).<br>3. La cuenta base `existente.g1@dsqa.test` (nombre `Mariela Bustos`, rol usuario) existe. |
| Datos de entrada | Nombre `Mateo Salgado` · Correo `existente.g1@dsqa.test` · Contraseña `Bosque52` · Rol `Soporte` (D-007; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Se rechaza la solicitud; el correo se identifica como dato a corregir junto a su campo; no se crea otra cuenta y la existente conserva nombre `Mariela Bustos` y rol usuario. |
| Postcondición | Sigue existiendo una sola cuenta con `existente.g1@dsqa.test`, sin cambios. |
| Evidencia requerida | Captura del aviso junto al campo; consulta antes y después. |
