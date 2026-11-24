# ACC-REG-015 · Rechazar una contraseña que contiene el nombre

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REG-015.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REG-015 |
| Nombre | Rechazar una contraseña que contiene el nombre |
| Descripción | Verificar que una contraseña que contiene una palabra del nombre, escrita igual, se rechaza indicando esa condición. |
| Número de orden de ejecución | 15 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-001 · CA-HU-001-04 y CA-HU-001-05 · Criterio: **CA-HU-001-05** |
| Escenario | ESC-ACC-REG-015 · Contraseña que contiene el nombre de la persona · Excepción (error path) |
| Tipo de prueba y técnica | Funcional · Caja negra · partición de equivalencia (clase inválida «contiene el nombre»; alcance según PA-02) |
| RNF relacionado | — |
| Prioridad | Media |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../2.3_Datos_de_prueba.md) con la cuenta `existente.g1@dsqa.test`. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de registro desde este navegador (control del límite de 3 por minuto, RNF-006; ver PA-01).<br>3. El correo `gonzalo.pardo@dsqa.test` no existe. |
| Datos de entrada | Nombre `Gonzalo Pardo` · Correo `gonzalo.pardo@dsqa.test` · Contraseña `Pardo2026` · Rol Usuario (D-015; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Se rechaza; se indica la condición «sin el nombre de la persona»; no se crea la cuenta. |
| Postcondición | No existe `gonzalo.pardo@dsqa.test`. |
| Evidencia requerida | Captura del rechazo y de la lista de condiciones. |
