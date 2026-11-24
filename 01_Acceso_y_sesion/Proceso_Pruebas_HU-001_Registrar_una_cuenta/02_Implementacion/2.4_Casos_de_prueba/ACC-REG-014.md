# ACC-REG-014 · Rechazar contraseñas que contienen espacios

[Índice de casos](00_Indice_de_casos.md) · [Matriz de trazabilidad](../2.2_Matriz_de_trazabilidad.md) · [Script asociado](../2.5_Scripts_de_prueba/SCR-ACC-REG-014.md)

**Estado del artefacto:** borrador para revisión por pares · **Estado de ejecución:** no ejecutado.

| Elemento | Contenido |
|---|---|
| Identificador | ACC-REG-014 |
| Nombre | Rechazar contraseñas que contienen espacios |
| Descripción | Verificar que una contraseña con un espacio intermedio o inicial se rechaza indicando la condición «sin espacios». |
| Número de orden de ejecución | 14 (independiente; ver [3.1 Preparación de la ejecución](../../03_Ejecucion/3.1_Preparacion_de_la_ejecucion.md)) |
| Requerimiento y criterio asociados | RF-001 · CA-HU-001-04 y CA-HU-001-05 · Criterio: **CA-HU-001-05** |
| Escenario | ESC-ACC-REG-014 · Contraseña con espacios · Excepción (error path) |
| Tipo de prueba y técnica | Funcional · Caja negra · partición de equivalencia (espacio intermedio y espacio inicial) |
| RNF relacionado | — |
| Prioridad | Media |
| Precondición | 1. Ambiente de ensayo preparado (ver [2.6 Ambiente](../2.6_Ambiente_de_pruebas.md)); base restaurada al punto de control de [2.3](../2.3_Datos_de_prueba.md) con la cuenta `existente.g1@dsqa.test`. Navegador sin sesión iniciada.<br>2. Han pasado al menos 65 s sin solicitudes de registro desde este navegador (control del límite de 3 por minuto, RNF-006; ver PA-01).<br>3. El correo `paula.cifuentes@dsqa.test` no existe. |
| Datos de entrada | `Paula Cifuentes` · `paula.cifuentes@dsqa.test` · Usuario con: D-014A `Bosque␠52` · D-014B `␠Bosque52` (D-014A, D-014B; ver [2.3 Datos](../2.3_Datos_de_prueba.md)) |
| Resultado esperado | Ambos envíos se rechazan indicando «sin espacios»; no se crea la cuenta. |
| Postcondición | No existe `paula.cifuentes@dsqa.test`. |
| Evidencia requerida | Captura de cada rechazo. |
