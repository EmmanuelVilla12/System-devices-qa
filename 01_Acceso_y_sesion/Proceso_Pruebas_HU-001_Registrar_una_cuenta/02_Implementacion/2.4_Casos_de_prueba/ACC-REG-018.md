# ACC-REG-018 · Proteger la contraseña en la respuesta y en el almacenamiento

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REG-018.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REG-018 |
| Nombre | Proteger la contraseña en la respuesta y en el almacenamiento |
| Descripción | Verificar que la contraseña no aparece en los datos de respuesta ni se guarda en texto legible. |
| Número de orden de ejecución | 18 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-001 · RNF-001 · Criterio: **CA-HU-001-01** |
| Escenario | ESC-ACC-REG-018 · Contraseña protegida en la respuesta y en el almacenamiento · Calidad |
| Tipo de prueba y técnica | No funcional (seguridad) · Caja negra · inspección de respuesta y de almacenamiento (recorrido no funcional) |
| RNF relacionado | RNF-001 |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../2.3_Datos_de_prueba.md) con la cuenta `existente.g1@dsqa.test`. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de registro desde este navegador (control del límite de 3 por minuto, RNF-006; ver PA-01).<br>3. Acceso de solo lectura a la base de ensayo (PA-05). Panel de red del navegador abierto.<br>4. El correo `natalia.pineda@dsqa.test` no existe. |
| Datos de entrada | Nombre `Natalia Pineda` · Correo `natalia.pineda@dsqa.test` · Contraseña `Faro2026Luz` · Rol `Usuario` (D-018; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | La respuesta del registro no contiene `Faro2026Luz` ni un campo con la contraseña; el registro almacenado de la cuenta no contiene `Faro2026Luz` en texto legible. |
| Postcondición | Existe la cuenta `natalia.pineda@dsqa.test`. |
| Evidencia requerida | Captura de la respuesta en el panel de red con búsqueda del valor; captura de la consulta de solo lectura. |
