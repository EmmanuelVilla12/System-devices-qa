# ACC-REG-011 · Actualizar la lista de condiciones mientras se escribe y corrige la contraseña

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REG-011.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REG-011 |
| Nombre | Actualizar la lista de condiciones mientras se escribe y corrige la contraseña |
| Descripción | Verificar que la lista de condiciones cambia con cada escritura o corrección, incluso cuando una condición deja de cumplirse. |
| Número de orden de ejecución | 2 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-001 · Flujo principal paso 4 · Criterio: **CA-HU-001-04** |
| Escenario | ESC-ACC-REG-011 · Lista de condiciones de contraseña en tiempo real · Alterno |
| Tipo de prueba y técnica | Funcional · Caja negra · transición de estados (condición cumplida ↔ no cumplida) |
| RNF relacionado | — |
| Prioridad | Alta |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../2.3_Datos_de_prueba.md) con la cuenta `existente.g1@dsqa.test`. Navegador sin sesión iniciada. |
| Datos de entrada | Nombre `Tomás Quiroga`. Secuencia en Contraseña: `7` → `7k` → `7kR` → `7kRwpzqx` → `7kRw pzqx` → `7kRwpzqx` → `7kRwpzqxQuiroga`. No se envía (D-011; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Después de cada valor la lista coincide con la tabla de estados de [1.3](../../01_Preparacion/1.3_Tipos_y_tecnicas_de_prueba.md): al insertar el espacio o la palabra `Quiroga` la condición correspondiente vuelve a no cumplida. |
| Postcondición | No se crea ninguna cuenta. |
| Evidencia requerida | Captura de la lista tras cada valor (7 capturas o un video corto). |
