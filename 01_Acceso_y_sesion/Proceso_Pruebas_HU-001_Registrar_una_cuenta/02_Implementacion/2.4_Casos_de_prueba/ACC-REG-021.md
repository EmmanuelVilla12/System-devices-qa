# ACC-REG-021 · Leer y operar el registro en computador y teléfono

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REG-021.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REG-021 |
| Nombre | Leer y operar el registro en computador y teléfono |
| Descripción | Verificar que campos, lista de condiciones y acciones se mantienen utilizables en computador y teléfono móvil. |
| Número de orden de ejecución | 21 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-001 · RNF-005 · Criterio: **CA-HU-001-01, CA-HU-001-04** |
| Escenario | ESC-ACC-REG-021 · Formulario utilizable en computador y teléfono móvil · Calidad |
| Tipo de prueba y técnica | No funcional (adaptación) · Caja negra · recorrido en dos tamaños de pantalla (1366×768 y 390×844) |
| RNF relacionado | RNF-005 |
| Prioridad | Media |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../2.3_Datos_de_prueba.md) con la cuenta `existente.g1@dsqa.test`. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de registro desde este navegador (control del límite de 3 por minuto, RNF-006; ver PA-01).<br>3. Los correos `martin.gaviria@dsqa.test` y `sara.gaviria@dsqa.test` no existen. |
| Datos de entrada | D-021A computador: `Martín Gaviria` · `martin.gaviria@dsqa.test` · `Selva37Sol` · Usuario. D-021B móvil: `Sara Gaviria` · `sara.gaviria@dsqa.test` · `Selva37Sol` · Usuario (D-021A, D-021B; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | En 1366×768 y en 390×844 las etiquetas, la lista de condiciones y los mensajes se leen completos y el botón de envío es visible y utilizable; ambos registros se aceptan. |
| Postcondición | Existen las dos cuentas. |
| Evidencia requerida | Captura de pantalla completa en cada tamaño. |
