# ACC-REG-004 · Consultar las opciones del campo Rol

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REG-004.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REG-004 |
| Nombre | Consultar las opciones del campo Rol |
| Descripción | Verificar que el campo Rol ofrece las tres opciones de la ficha y ninguna otra, sin enviar el formulario. |
| Número de orden de ejecución | 1 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-001 · Flujo principal paso 3 · Criterio: **CA-HU-001-06** |
| Escenario | ESC-ACC-REG-004 · Consulta de las opciones del campo Rol · Alterno |
| Tipo de prueba y técnica | Funcional · Caja negra · partición de equivalencia (dominio cerrado de tres valores) |
| RNF relacionado | — |
| Prioridad | Media |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../2.3_Datos_de_prueba.md) con la cuenta `existente.g1@dsqa.test`. Navegador sin sesión iniciada. |
| Datos de entrada | Sin envío. Opciones esperadas: `usuario`, `soporte`, `administrador` (D-004; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | La lista de Rol contiene usuario, soporte y administrador; no aparecen otras opciones ni indicaciones de aprobación posterior. |
| Postcondición | No se crea ninguna cuenta. |
| Evidencia requerida | Captura del campo Rol desplegado. |
