# ACC-REG-020 · Identificar campos, condiciones y errores con lector de pantalla

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REG-020.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REG-020 |
| Nombre | Identificar campos, condiciones y errores con lector de pantalla |
| Descripción | Verificar que los campos se identifican y que avisos y errores se comunican de manera accesible. |
| Número de orden de ejecución | 20 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-001 · RNF-004 · Criterio: **CA-HU-001-03, CA-HU-001-04** |
| Escenario | ESC-ACC-REG-020 · Campos y errores identificables con lector de pantalla · Calidad |
| Tipo de prueba y técnica | No funcional (accesibilidad) · Caja negra · recorrido de accesibilidad con lector de pantalla |
| RNF relacionado | RNF-004 |
| Prioridad | Media |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../2.3_Datos_de_prueba.md) con la cuenta `existente.g1@dsqa.test`. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de registro desde este navegador (control del límite de 3 por minuto, RNF-006; ver PA-01).<br>3. Lector de pantalla NVDA (o equivalente) activo. |
| Datos de entrada | Nombre `Daniela Úsuga` · Correo `daniela.usugadsqa.test` (sin @) · Contraseña `Coral81x` · Rol `Usuario` (D-020; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Al enfocar cada campo el lector anuncia su nombre; anuncia el estado de las condiciones de contraseña; después del envío anuncia el error del campo Correo electrónico; no se crea cuenta. |
| Postcondición | No se crea ninguna cuenta. |
| Evidencia requerida | Transcripción o grabación del audio del lector. |
